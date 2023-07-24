### О проекте

#### [Дипломное задание](https://github.com/netology-code/qa-diploma)

Данный учебный проект представляет собой дипломную работу, предполагающую автоматизацию тестирования сервиса,
взаимодействующего с СУБД и API Банка.

Цель проекта — автоматизировать позитивные и негативные сценарии покупки тура.

План:

- Спланировать автоматизацию тестирования
- Провести автоматизированное тестирование
- Составить баг-репорты на найденные баги
- Подготовить отчётные документы по итогам автоматизированного тестирования
- Подготовить отчётные документы по итогам автоматизации.

## Для запуска авто-тестов на Вашем компьютере, после клонирования проект с github, следует выполнить следующие шаги:

1. Проверьте наличие на Вашем компьютере сл. программам:
     
   -Java: JDK 11;

   -Docker (для подключения и запуска через него следующих приложений: MySQL, PostgreSQL)

2. Запустите docker-контейнеры, используя команду в терминале:
   **docker-compose up**

3. Запустить приложение командой в консоли

*для MySQL*:


**java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" "-Dspring.datasource.username=app" "
-Dspring.datasource.password=pass" -jar artifacts/aqa-shop.jar**

*для PostgreSQL*:


**java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" "-Dspring.datasource.username=app" "
-Dspring.datasource.password=pass" -jar artifacts/aqa-shop.jar**

4. Запустить авто-тесты командой в консоли

*для MySQL*:
**./gradlew test "-Ddb.url=jdbc:mysql://localhost:3306/app" "-Ddb.username=app" "-Ddb.password=pass"**

*для PostgreSQL*:
**./gradlew test "-Ddb.url=jdbc:postgresql://localhost:5432/app" "-Ddb.username=app" "-Ddb.password=pass"**

5. Для получения отчёта( репорт Allure) по проведению автоматизированных тестов, после запуска тестов, введите в
   терминале команду:
   **./gradlew allureReport** - формирование отчёта

**./gradlew allureServe** - отображение отчёта в браузере

#### [Отчётные документы по итогам тестирования](https://github.com/Lukinsg/Diploma-project/blob/main/Documentation/Report.md)

#### [Отчётные документы по итогам автоматизации](https://github.com/Lukinsg/Diploma-project/blob/main/Documentation/Summary.md)
