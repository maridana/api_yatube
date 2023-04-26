# api_yatube - CRUD для Yatube

## Спринт 8 - CRUD для Yatube

### api_yatube - CRUD для Yatube

Для взаимодействия с ресурсами опиcаны и настроены такие эндпоинты:
- api/v1/api-token-auth/ (POST): передаём логин и пароль, получаем токен.
- api/v1/posts/ (GET, POST): получаем список всех постов или создаём новый пост.
- api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост по id.
- api/v1/groups/ (GET): получаем список всех групп.
- api/v1/groups/{group_id}/ (GET): получаем информацию о группе по id.
- api/v1/posts/{post_id}/comments/ (GET, POST): получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать.
- api/v1/posts/{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий по id у поста с id=post_id.

### Настройка и запуск на ПК

Клонировать репозиторий:

```bash
git clone 
```

Перейти в него в командной строке:

```bash
cd api_yatube
```

Установить виртуальное окружение:

```bash
python -m venv venv
```

Активировать виртуальное окружение:

```bash
source venv/Scripts/activate
```

Установить зависимости:

```bash
python -m pip install --upgrade pip
```
```bash
pip install -r requirements.txt
```

Применить миграции:

```bash
python yatube_api/manage.py makemigrations
```
```bash
python yatube_api/manage.py migrate
```

Создать супер пользователя:

```bash
python yatube_api/manage.py createsuperuser
```


Запустить проект:

```bash
python yatube_api/manage.py runserver
```

Ваш проект запустится на http://127.0.0.1:8000/

С помощью команды pytest можно запустить тесты и проверить работу модулей.
