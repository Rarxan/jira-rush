## [REST API](http://localhost:8080/doc)

## Концепция:

- Spring Modulith
    - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
    - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
    - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

- Есть 2 общие таблицы, на которых не fk
    - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
    - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем
      проверять

## Аналоги

- https://java-source.net/open-source/issue-trackers

## Тестирование

- https://habr.com/ru/articles/259055/

Completed tasks:

- [x] 1. Onboarding
- [x] 2. Removed VK and Yandex OAuth providers
- [x] 3. Moved sensitive configuration to a separate properties file with environment variables
- [x] 4. Switched tests to H2 in-memory database with Spring profiles
- [x] 5. Added tests for all public methods of ProfileRestController
- [x] 6. Refactored FileUtil#upload to use modern java.nio.file API
- [x] 7. Added task tags support (REST API + service layer)
- [x] 8. Added service methods to calculate task work and testing duration
- [x] 9. Added Dockerfile for the main server