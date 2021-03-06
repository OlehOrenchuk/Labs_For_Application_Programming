# Імплементація REST API

В даній лабораторній роботі потрібно реалізувати REST API спроектоване в другій лабораторній використовуючи моделі створені у третій лабораторній. Дана лабораторна не включає авторизацію користувачів та перевірку прав доступів до тих чи інших ресурсів чи операцій.
 
## Рекомендації

* Під час розробки зручно використовувати `flask run` в дебаг режимі, тоді сервіс автоматично буде перезавантажуватись при зміні коду
* Для валідації даних можна використати пакет [marshmallow](https://marshmallow.readthedocs.io/en/stable/)
* Для хешування паролів користувачів можна використати пакет [Flask-Bcrypt](https://flask-bcrypt.readthedocs.io/en/latest/)

## Хід роботи

1. Реалізувати логіку кожної з адрес з валідацією даних
3. Реалізувати коректну поведінку при різних помилках (повернення коректного контенту та HTTP статус кодів)
4. Перевірити коректність реалізації за допомогою Postman, curl чи інших засобів

## Критерії оцінювання

1. Реалізовані всі операції описані в `swagger.yaml` в другій лабораторній
2. Паролі користувачів зберігаються у захешованому виді
    > Показати як паролі шифруються або зробити запит на створення користувача та показати що, користувач збережений в базі даних з захешованим паролем
3. Вхідні дані валідуються по типу полів на інших параметрах залежно від варіанту
    > Показати валідацію вхідних даних в коді
4. При помилках повертається JSON-відповідь зі HTTP статус кодом відповідно до помилки
    > Показати код відповідальний за відповіді при помилках
5. Продемонструвати кілька запитів до розробленого API (один з них має демонструвати поведінгку при помилках) за допомогодю Postman, curl чи інших засобів