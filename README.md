# Дипломый проект профессии "Тестировщик"

## Запуск SUT, автотестов и генерация отчета:

Необходимое ПО:
* Docker Desktop;
* IntelliJ IDEA;
* Git.


### Подключение SUT к БД MySQL, запуск тестов и создание отчета:

1. Открыть окно терминала и в командной строке набрать команду:

    `docker-compose up -d`
     
2. Запустить проект командой:

   `java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar`
     
3. Запустить тесты командой: 

   `./gradlew clean test "-Ddb.url=jdbc:mysql://localhost:3306/app"`
  
4. Закрыть приложения в консоли с помощью комбинации:

   **Ctrl + C**
   
5. Остановить контейнер в консоли командной:

     `docker-compose down`


### Подключение SUT к БД PostgreSQL, запуск тестов и создание репорта:

1. Открыть окно терминала и в командной строке набрать команду:

    `docker-compose up -d`
  
2. Запустить проект командой:

   `java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar`
   
3. Запустить тесты командой:

   `./gradlew clean test "-Ddb.url=jdbc:postgresql://localhost:5432/app"`
   
4. Закрыть приложения в консоли с помощью комбинации:

   **Ctrl + C**
   
5. Остановить контейнер в консоли командной:

     `docker-compose down`

## Документация:

* [Задание](https://github.com/netology-code/qa-diploma)
* [План]()