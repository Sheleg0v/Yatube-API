# Yatube_api:

Yatube is a project where everyone can share a post with other people.

Posts can contain text and pictures. 
Posts can be commented.
Posts may belong to some group.
Anyone can subscribe to the author they are interested in.

### Stack:
- Django 3.2.16
- djangorestframework 3.12.4
- djangorestframework-simplejwt 4.7.2
- Pillow 9.3.0
- PyJWT 2.1.0
- djoser 2.1.0


## Project launch:

Clone the repository and change directory on the command line:

```
git clone git@github.com:Sheleg0v/api_final_yatube.git
```

```
cd yatube_api
```

Create and activate a virtual environment:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Install dependencies from a file requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Apply migrations:

```
python manage.py migrate
```

Launch project:

```
python manage.py runserver
```

## Examples of api requests:

Get posts
```
GET /api/v1/posts/
```

Response:
```
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
```

Add comment
```
POST /api/v1/posts/{post_id}/comments/
```

Request:
```
    {
        "text": "string"
    }
```

Response:
```
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }
```

### Author:
- https://github.com/Sheleg0v - Ivan Shelegov
