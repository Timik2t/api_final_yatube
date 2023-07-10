# API для Yatube

API для ![Yatube](https://github.com/Timik2t/yatube_project) - это RESTful API для социальной сети Yatube, предоставляющий функционал для работы с пользователями, постами, комментариями и группами.

## Описание проекта

API для Yatube позволяет выполнять следующие операции:

- Регистрация новых пользователей
- Аутентификация пользователей и получение токена доступа
- Создание, чтение, обновление и удаление постов
- Создание, чтение, обновление и удаление комментариев к постам
- Подписка и отписка от пользователей
- Создание, чтение, обновление и удаление групп

## Технологии

- Python
- Django
- Django REST Framework

## Возможности

- Регистрация новых пользователей
- Аутентификация пользователей и получение токена доступа
- Получение списка всех пользователей или конкретного пользователя
- Создание, чтение, обновление и удаление постов
- Создание, чтение, обновление и удаление комментариев к постам
- Получение списка всех групп или конкретной группы
- Подписка и отписка от пользователей
- Фильтрация и сортировка данных

## Как запустить проект

1. Склонируйте репозиторий на локальную машину:

    ```bash
    git@github.com:Timik2t/api_final_yatube.git
    ```

2. Создайте и активируйте виртуальное окружение:

    ```bash
    python -m venv venv
    ```

    Активация окружения
    ```bash
    # Windows
    source venv/Scripts/activate
    ```
    ```bash
    # Linux
    source venv/bin/activate
    ```
3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```
4. Выполните миграции:
   ```bash
   python3 manage.py migrate
   ```
5. В папке с файлом `manage.py` выполните команду:
   ```bash
   python3 manage.py runserver
   ```
6. Создание суперпользователя:
   ```bash
   python yatube_api/manage.py createsuperuser
   ```
## API Справочник

#### Получить токен аутентификации

```http
  POST api/v1/api-token-auth/
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `username` | `string` | **Required**. Your superuser name |
| `password` | `string` | **Required**. Your superuser password |

#### Управление постами:

```http
  GET, POST, PUT, PATCH, DELETE /api/v1/posts/
  GET, POST, PUT, PATCH, DELETE /api/v1/posts/$id/
```

| Headers | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Authorization`      | `string` | Token <YOUR_TOKEN> |

#### Управление группами:

```http
  GET, POST, PUT, PATCH, DELETE /api/v1/groups/
  GET, POST, PUT, PATCH, DELETE /api/v1/groups/$id/
```

| Headers | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Authorization`      | `string` | Token <YOUR_TOKEN> |

### Автор
[Tim](https://github.com/Timik2t)
