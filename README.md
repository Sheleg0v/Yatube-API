### Yatube_api:

Yatube - это проект где каждый может поделиться постом с другими людьми.

Посты могут содержать текст и картинки. 
Посты можно комментировать.
Также посты могут принадлежать какой-то группе.
Любой человек может подписаться на интересующего его автора.


### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:Sheleg0v/api_final_yatube.git
```

```
cd yatube_api
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

### Примеры запросов к api:

Получение публикаций
GET /api/v1/posts/

Response:
    {
        "count": 123,
        "next": "http://api.example.org/accounts/?offset=400&limit=100",
        "previous": "http://api.example.org/accounts/?offset=200&limit=100",
        "results": [
            {
                "id": 0,
                "author": "string",
                "text": "string",
                "pub_date": "2021-10-14T20:41:29.648Z",
                "image": "string",
                "group": 0
            }
        ]
    }

Добавление комментария
POST /api/v1/posts/{post_id}/comments/

Request:
    {
        "text": "string"
    }

Response:
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }