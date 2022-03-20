Проект MsfoStockBot - это сервис для инвесторов российского фондового рынка.
Перед тем как запустить проект, нужно установить все библиотеки из файла requirements.txt (набрать команду в терминале pip install -r requirements.txt).
<b>Запустить файл main.py.</b>

Версия python 3.8.6+ (на более ранних версиях не проверял).
Проект рабочий(https://msfostockweb.pythonanywhere.com/user/), прошу не снижать балл если Вы столкнулись с проблемами запуска. 
Воспользуйтесь зарегистрированными мной аккаунтами для тестирования функционала:
1. Администратор - логин: admin@gmail.com пароль: admin 
2. Редактор - логин: editor@gmail.com пароль: editor 
3. Обычный пользователь - логин: user@gmail.com пароль: user  

По заданию из мини проекта по wtforms:

  1. Базовый шаблон находится templates/base.html он применён к каждой странице сайта. 
  2. css стили полностью на bootstrap. 
  3. Flask-WTF используется в проекте многократно, это создание тестового пользователя(user_profile\user_profile.py) под учёткой админа(без подтверждения почты и с упрощённым паролем), форма регистрации нового пользователя(user_profile\registration_form.py), добавление компании если Вы с правами администратора или редактора(msfo_records\forms). 
  4. При создании тестового пользователя применяются различные поля: EmailField, PasswordField, StringField, SelectField, DateField прочитать о них можно в документации библиотеки flask-wtf. К полям пароля применены валидаторы InputRequired(обязательное поле), EqualTo(схожесть поля с подтвержением пароля), Length(длина мин. и макс.)
  5. В проекте множество функций представления со статическими маршрутами, а так же динамическим(```python
    <input type="text">
msfo_records\content_blueprint.py  http://192.168.1.229:5000/msfo_records/</slug/>/edit/)```. Функции представления обрабатывают GET и POST запросы.
