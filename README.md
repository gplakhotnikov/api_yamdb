# YaMDb

Проект YaMDb собирает отзывы (Review) пользователей на произведения (Title). Произведения делятся на категории: "Книги", "Фильмы", "Музыка". Список категорий (Category) может быть расширен. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.

## Особенности / Features

- Раз в 10 минут бот делает запрос к API сервису Yandex.Practicum и проверяет статус отправленной на ревью домашней работы
- При обновлении статуса анализирует ответ API и отправляет соответствующее уведомление в Telegram
- Логирует работу и сообщает о проблемах сообщением в Telegram

## Стек технологий / Tech

- [Python](https://www.python.org/)
- [Django](https://www.djangoproject.com/)
- [Django REST framework](https://www.django-rest-framework.org/)
- [Simple JWT](https://django-rest-framework-simplejwt.readthedocs.io/) - a JSON Web Token authentication backend for the Django REST Framework
- [PyJWT](https://pyjwt.readthedocs.io/) - a Python library which allows you to encode and decode JSON Web Tokens (JWT)
- [requests 2.26.0](https://pypi.org/project/requests/2.6.0/) - an Apache2 Licensed HTTP library, written in Python, that allows you to send HTTP/1.1 requests easily

### Примеры эндпоинтов / Endpoints

Регистрация нового пользователя. Права доступа: Доступно без токена.
```
http://127.0.0.1:8000/api/v1/auth/signup/
```
Получение JWT-токена. Права доступа: Доступно без токена.
```
http://127.0.0.1:8000/api/v1/auth/signup/
```
Получение списка всех категорий. Права доступа: Доступно без токена
```
http://127.0.0.1:8000/api/v1/categories/
```
Добавление новой категории. Права доступа: Администратор.
```
http://127.0.0.1:8000/api/v1/categories/
```
Удаление категории. Права доступа: Администратор.
```
http://127.0.0.1:8000/api/v1/categories/{slug}/
```
Подробнее можно посмотреть в документации Redoc после старта сервера по адресу:
```
http://127.0.0.1:8000/redoc/
```

## Как запустить проект / Installation

Cоздать и активировать виртуальное окружение, скачать Pip:
```
python3 -m venv env
source env/bin/activate
python3 -m pip install --upgrade pip
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```

## О разработчике / Development
Валерий Юрченко - Тимлид
Михаил Басков
Grigory Plakhotnikov
