# Фреймворк Spring (семинары)

## Урок 10. Spring Testing. JUnit и Mockito для написания тестов.
#### Задание:<br> Напишите тесты для основной логики вашего приложения с использованием Spring Testing, JUnit и Mockito.<br><br>
### Описание<br>
- Написание юнит-тестов для сервисного слоя приложения с использованием JUnit и Mockito.<br>
  Написание интеграционных тестов с использованием Spring Test.<br>
  Практика тестирования основных аспектов приложения, включая тестирование данных, служб, контроллеров и т.д.<br>
<br>

### Домашнее задание
<br>

1. Протестировать TimesheetController с использованием JUnit и Mockito, а именно:<br>
```
   GET /timesheets/{id}
   GET /timesheets
   POST /timesheets
   DELETE /timesheets
   PUT /timesheets/{id}
```
<br>

### Решение

#### Определения

[Официальный сайт JUnit5: https://junit.org/junit5/ ](https://junit.org/junit5/)<br>
**JUnit** - это основная библиотека для юнит-тестирования в Java.<br>
Данная библиотека помогает обеспечить качество кода, проверяя отдельные модули программы на соответствие ожидаемому поведению.<br>
[Официальный сайт Mockito: https://site.mockito.org/ ](https://site.mockito.org/)<br>
**Mockito** - это библиотека для создания и управления объектами-заменителями (моками) в Java.<br> 
Такая библиотека позволяет имитировать зависимости и проверять их взаимодействие с тестируемыми модулями.<br>

#### Интеграция Mockito и junit 5 в проект

Необходимо добавить в файл pom.xml следующую зависимость:
```xml
<dependency>
    <groupId>org.mockito</groupId>
    <artifactId>mockito-core</artifactId>
    <version>5.12.0</version>
    <scope>test</scope>
</dependency>
```
и добавить в файл pom.xml следующие зависимости:

```xml
<!-- junit 5 -->
<dependency>
  <groupId>org.junit.jupiter</groupId>
  <artifactId>junit-jupiter-engine</artifactId>
  <version>5.10.3</version>
  <scope>test</scope>
</dependency>

```
```xml
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.10.3</version>
    <scope>test</scope>
</dependency>
```

Чтобы протестировать ```TimesheetController``` с помощью JUnit и Mockito,<br> 
необходимо создать тестовый класс ```TimesheetControllerTest``` (в соответствующей директории в папке ```src/test/```, в котором можно<br> 
имитировать зависимости и определять тестовые случаи для каждой конечной точки данного класса в проекте.

1. Аннотации (Annotations:):

- **@@Mock** создает фиктивные объекты для зависимостей (в данном случае для службы расписания);<br>
- **@InjectMocks** автоматически вводит фиктивные зависимости в экземпляр ```TimesheetController```;<br>
- **@beforeEach** инициализирует макеты перед каждым тестом.

2. Тестовые примеры (Test Cases):

- **testGetTimesheetById** проверяет конечную точку ```@GET("/timesheets/{id}")``` на предмет успешного ответа;<br>
- **testGetTimesheetById_NotFound** проверяет конечную точку ```@GET("/timesheets/{id}")``` на наличие ответа 404 "Не найдено";<br>
- **testGetAllTimesheets** проверяет конечную точку ```@GET("/timesheets")``` на получение списка расписаний;<br>
- **testCreateTimesheet** проверяет конечную точку ```@POST(/timesheets")``` на предмет создания нового расписания;<br>
- **testDeleteTimesheet** проверяет конечную точку ```@DELETE("/timesheets/{id}")``` на предмет успешного удаления;<br>
- **testHandleNoSuchElementException** проверяет обработчик исключений на наличие исключения NoSuchElementException;<br>
- **testUpdateTimesheet** проверяет конечную точку ```@PUT{"/timesheets/{id}")```.

<br><br>
## Дополнительная информация
<br><br>
- Начальная страница локального сервера (Таблицы)<br><br>

    http://localhost:8080/login<br><br>
    или<br><br>
    http://localhost:8080/home/timesheets<br>

```
http://localhost:8080/home/timesheets

```

- Страница проекта, например :

```
http://localhost:8080/home/projects/1

```

- Страница записи, например :

```
http://localhost:8080/home/timesheets/1

```
<br>

### Автоматическое форматирование кода в Intellij IDEA<br><br>

- В настройках IDE для автоматического переформатирования кода необходимо проверить наличие форматирования java-файла,<br> 
для этого нажать сочетание клавиш **Ctrl + Alt + S**, чтобы открыть настройки IDE, и выбрать **Tools | Actions on Save**, далее включить параметр **Reformat code**, отметив чекбокс 'Reformat code'.<br><br>

- Для форматирования содержимого java-файла, нажать сочетание клавиш
**Ctrl + Alt + L** - Reformat code

<br><br><br>