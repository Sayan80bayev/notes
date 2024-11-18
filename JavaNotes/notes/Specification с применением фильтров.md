---
tags:
  - Паттерны
  - Programming
---

```java
public interface FilterSpecification<T> {  
    Specification<T> toSpecification(AdvertisementFilterRequest advertisementFilterRequest);  
    boolean isApplicable(AdvertisementFilterRequest advertisementFilterRequest);  
}```

```java
@Component  
public class CategorySpecification implements FilterSpecification<Advertisement> {  
    @Override  
    public Specification<Advertisement> toSpecification(AdvertisementFilterRequest advertisementFilterRequest) {  
        return (root, query, criteriaBuilder) ->  
                criteriaBuilder.equal(root.get("category").get("id"), advertisementFilterRequest.getCategoryId());  
    }  
    @Override  
    public boolean isApplicable(AdvertisementFilterRequest advertisementFilterRequest) {  
        return advertisementFilterRequest.getCategoryId() != null;  
    }
}
```

```java
@Component  
public class DateSpecification implements FilterSpecification<Advertisement> {  
  
    @Override  
    public Specification<Advertisement> toSpecification(AdvertisementFilterRequest advertisementFilterRequest) {  
        return (root, query, criteriaBuilder) -> {  
            LocalDateTime createdAfter = advertisementFilterRequest.getCreatedAfter();  
            LocalDateTime createdBefore = advertisementFilterRequest.getCreatedBefore();  
  
            if (createdAfter != null && createdBefore != null) {  
                return criteriaBuilder.between(root.get("date"), createdAfter, createdBefore);  
            } else if (createdAfter != null) {  
                return criteriaBuilder.greaterThanOrEqualTo(root.get("date"), createdAfter);  
            } else if (createdBefore != null) {  
                return criteriaBuilder.lessThanOrEqualTo(root.get("date"), createdBefore);  
            }            return null; // No filtering condition if both dates are null  
        };  
    }  
    @Override  
    public boolean isApplicable(AdvertisementFilterRequest advertisementFilterRequest) {  
        return advertisementFilterRequest.getCreatedAfter() != null  
                || advertisementFilterRequest.getCreatedBefore() != null;  
    }
}
```

```java
@Component  
public class PriceRangeSpecification implements FilterSpecification<Advertisement> {  
  
    @Override  
    public Specification<Advertisement> toSpecification(AdvertisementFilterRequest advertisementFilterRequest) {  
        return (root, query, criteriaBuilder) -> {  
            Double minPrice = advertisementFilterRequest.getMinPrice();  
            Double maxPrice = advertisementFilterRequest.getMaxPrice();  
  
            if (minPrice != null && maxPrice != null) {  
                return criteriaBuilder.between(root.get("price"), minPrice, maxPrice);  
            } else if (minPrice != null) {  
                return criteriaBuilder.greaterThanOrEqualTo(root.get("price"), minPrice);  
            } else if (maxPrice != null) {  
                return criteriaBuilder.lessThanOrEqualTo(root.get("price"), maxPrice);  
            }            return null;  
        };    }  
    @Override  
    public boolean isApplicable(AdvertisementFilterRequest advertisementFilterRequest) {  
        return advertisementFilterRequest.getMinPrice() != null || advertisementFilterRequest.getMaxPrice() != null;  
    }
}
```


```java
@Service  
@Slf4j  
public class AdvertisementServiceImpl implements AdvertisementService {
	private final List<FilterSpecification<Advertisement>> filterSpecifications;
	
	@Override  
	public List<AdvertisementResponse> findByFiler(AdvertisementFilterRequest filterRequest) {  
	        Specification<Advertisement> finalSpec = filterSpecifications.stream()  
	                .filter(spec -> spec.isApplicable(filterRequest))  
	                .map(spec -> spec.toSpecification(filterRequest))  
	                .reduce(Specification.where(null), Specification::and);  
	  
	        List<Advertisement> advertisements = advertisementRepository.findAll(finalSpec);  
	  
	        return advertisements.stream().map(mapper::toResponse).toList();  
	}
}
```