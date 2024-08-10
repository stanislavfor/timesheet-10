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