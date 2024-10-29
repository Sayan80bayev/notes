
**Резюме: Как настроить сервис инструкторов**

В данном проекте была разработана клиентская часть для взаимодействия с сервисом инструкторов. Основные шаги для его реализации включают следующие моменты:

1. **Выбор технологий**:

• Использовался HttpClient для выполнения HTTP-запросов.

• Для работы с JSON была выбрана библиотека Gson.

2. **Настройка класса** InstructorClient:

• Создан класс InstructorClient, который содержит методы для выполнения запросов к API.

• Класс аннотирован @Component, чтобы его можно было использовать в контексте Spring.

3. **Работа с API**:

• Добавлен метод findInstructorsByListIds, который принимает список идентификаторов инструкторов (UUID) и возвращает список объектов InstructorDTO.

```java
public List<InstructorDTO> findInstructorsByListIds(List<UUID> ids) {
    try {
        log.info("API Key: {}", userServiceApiKey);

        // Преобразование списка UUID в JSON-строку
        String requestBody = gson.toJson(ids);
        log.info("Request Body: {}", requestBody);

        String url = "https://localhost:8081/api/instructors/getInstructors/byIdList";  // Поддержка как HTTP, так и HTTPS

        // Создание HTTP-запроса
        HttpRequest request = HttpRequest.newBuilder()
                .uri(URI.create(url))
                .header("Content-Type", "application/json")
                .header("API-Key", userServiceApiKey) // Передача API ключа в заголовках
                .POST(HttpRequest.BodyPublishers.ofString(requestBody))
                .build();

        // Отправка запроса асинхронно и получение CompletableFuture для ответа
        CompletableFuture<HttpResponse<String>> responseFuture = httpClient.sendAsync(request, HttpResponse.BodyHandlers.ofString());

        // Обработка ответа, когда он будет доступен
        HttpResponse<String> response = responseFuture.join();

        // Проверка статуса ответа
        if (response.statusCode() != 200) {
            String responseBody = response.body();
            log.error("Unexpected status code: {}. Response body: {}", response.statusCode(), responseBody);
            throw new RuntimeException("Unexpected status code: " + response.statusCode());
        }

        // Логирование тела ответа
        String responseBody = response.body();
        log.info("Response Body: {}", responseBody);

        // Десериализация тела ответа в список объектов InstructorDTO
        return gson.fromJson(responseBody, new TypeToken<List<InstructorDTO>>() {}.getType());

    } catch (Exception e) {
        log.error("Error while fetching instructors", e);
        throw new RuntimeException("Error while fetching instructors", e);
    }
}
```

4. **Поддержка HTTPS**:

• Настроен HttpClient для поддержки как HTTP, так и HTTPS. Это позволяет выполнять запросы к API, использующему защищенные соединения.

• При необходимости была добавлена возможность настройки пользовательских сертификатов для работы с самоподписанными сертификатами.

5. **Обработка ошибок**:

• Включена обработка исключений для управления возможными ошибками при выполнении запросов к API.

• Добавлено логирование для отслеживания неожиданных кодов состояния и других ошибок.

**Заключение**

Данный сервис теперь эффективно взаимодействует с API инструкторов, обеспечивая безопасные и асинхронные запросы, а также удобную обработку данных с использованием Gson.

#java #http #client #microservices