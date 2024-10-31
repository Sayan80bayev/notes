---
tags:
  - patterns
  - solid
  - filters
  - Java/ООП
---

В этой статье мы рассмотрим, как реализовать механизм фильтрации и сортировки пользователей в приложении на Spring. Мы также обсудим, как мы применяем принципы SOLID (читайте в статье [[Принципы SOLID]])  и используем шаблоны проектирования для достижения гибкости и масштабируемости кода.
  
### **1. Общая Архитектура**

В нашем приложении мы будем использовать следующие компоненты:
	• **Контроллер** : обрабатывает HTTP-запросы и отправляет ответы.
	• **Сервис**: содержит бизнес-логику для фильтрации и сортировки.
	• **Спецификации**: используются для создания динамических запросов к базе данных.
	• **DTO**: объект передачи данных для получения параметров фильтрации и сортировки от клиента.


### **2. DTO для Фильтрации и Сортировки**

Мы создадим класс UserFilterRequest, который будет содержать поля для фильтрации и сортировки.

```java
public class UserFilterRequest {

    private Integer minAge;

    private Integer maxAge;

    private String name;

    private String email;

    private String sortBy; 
    
}
```

**Применение SOLID**

• **S (Single Responsibility Principle)**: Класс UserFilterRequest имеет единую ответственность - хранить параметры для фильтрации и сортировки.

### **3. Спецификации для Фильтрации**

Для фильтрации пользователей мы создадим UserSpecificationBuilder, который будет формировать спецификации на основе входящих параметров.

```java
import org.springframework.data.jpa.domain.Specification;

public class UserSpecificationBuilder {
    private final UserFilterRequest filterRequest;

    public UserSpecificationBuilder(UserFilterRequest filterRequest) {
        this.filterRequest = filterRequest;
    }

    public Specification<User> build() {
        List<Specification<User>> specifications = new ArrayList<>();

        if (filterRequest.getMinAge() != null || filterRequest.getMaxAge() != null) {
            specifications.add(new AgeSpecification(filterRequest.getMinAge(), filterRequest.getMaxAge()));
        }
        if (filterRequest.getName() != null && !filterRequest.getName().isEmpty()) {
            specifications.add(new NameSpecification(filterRequest.getName()));
        }
        // Добавление других спецификаций (например, EmailSpecification)

        return specifications.stream()
                .reduce(Specification::and)
                .orElse(null); // Если спецификации нет, возвращаем null
    }
}
```

**Применение SOLID**
	• **O (Open/Closed Principle)**: Мы можем добавлять новые спецификации, не изменяя код UserSpecificationBuilder.

  

### **4. Реализация Спецификаций**

Каждая спецификация будет отвечать за фильтрацию по определённому критерию. Например, спецификация по возрасту:
```java
import org.springframework.data.jpa.domain.Specification;

public class AgeSpecification implements Specification<User> {
    private final Integer minAge;
    private final Integer maxAge;

    public AgeSpecification(Integer minAge, Integer maxAge) {
        this.minAge = minAge;
        this.maxAge = maxAge;
    }

    @Override
    public Predicate toPredicate(Root<User> root, CriteriaQuery<?> query, CriteriaBuilder criteriaBuilder) {
        Predicate predicate = criteriaBuilder.conjunction();
        if (minAge != null) {
            predicate = criteriaBuilder.and(predicate, criteriaBuilder.greaterThanOrEqualTo(root.get("age"), minAge));
        }
        if (maxAge != null) {
            predicate = criteriaBuilder.and(predicate, criteriaBuilder.lessThanOrEqualTo(root.get("age"), maxAge));
        }
        return predicate;
    }
}
```

**Применение SOLID**

• **I (Interface Segregation Principle)**: Каждая спецификация реализует интерфейс Specification, что позволяет разделять различные фильтры.

### **5. Реализация Сортировки**
  Создадим интерфейс UserSort, который будет реализовывать разные стратегии сортировки.
```java
import org.springframework.data.jpa.domain.Specification;

public interface UserSort {
    Specification<User> toSort();
}

public class NameSort implements UserSort {
    @Override
    public Specification<User> toSort() {
        return (root, query, criteriaBuilder) -> {
            query.orderBy(criteriaBuilder.asc(root.get("name")));
            return criteriaBuilder.conjunction(); // Пустое условие
        };
    }
}
```  

**Применение SOLID**
	• **D (Dependency Inversion Principle)**: UserSort позволяет использовать абстракции для определения конкретных стратегий сортировки.  

### **6. Сервис Пользователей**
Сервис будет обрабатывать запросы на фильтрацию и сортировку пользователей.

```java
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.data.jpa.domain.Specification;
import org.springframework.stereotype.Service;

import java.util.List;

@Service
public class UserService {
    private final UserRepository userRepository;

    @Autowired
    public UserService(UserRepository userRepository) {
        this.userRepository = userRepository;
    }

    public List<User> filterUsers(UserFilterRequest filterRequest) {
        UserSpecificationBuilder builder = new UserSpecificationBuilder(filterRequest);
        Specification<User> combinedSpec = builder.build();

        UserSort sortStrategy = getSortStrategy(filterRequest.getSortBy());
        Specification<User> sortSpec = sortStrategy != null ? sortStrategy.toSort() : null;

        return userRepository.findAll(combinedSpec, sortSpec);
    }

    private UserSort getSortStrategy(String sortBy) {
        switch (sortBy) {
            case "name":
                return new NameSort();
            case "age":
                return new AgeSort();
            case "email":
                return new EmailSort();
            default:
                return null; // Возвращаем null, если не задана сортировка
        }
    }
}
```

**Применение SOLID**
	• **L (Liskov Substitution Principle)**: Мы можем легко заменять и расширять сортировки, просто добавляя новые классы, реализующие интерфейс UserSort.
  
## **Заключение**

В данной статье мы подробно рассмотрели процесс реализации фильтрации и сортировки пользователей в приложении на Spring. Мы использовали принципы SOLID для создания гибкой и расширяемой архитектуры, а также применяли шаблоны проектирования, чтобы обеспечить чистоту и поддержку кода.

Благодаря такому подходу вы можете легко добавлять новые спецификации фильтрации и стратегии сортировки, минимизируя изменения в существующем коде и улучшая его поддержку.