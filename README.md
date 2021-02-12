# Django User Database Template

A Django project template that has a working user system with [django-rest-auth](https://django-rest-auth.readthedocs.io/en/latest/) and [allauth](https://django-allauth.readthedocs.io/en/latest/)

## Using the template

The template is fully functional as is.

However if you wanted to change the project name from `myproject` to something else, you'll have to tweak a few things first:

### Project directory

Change `myproject` directory to whatever you like (e.g. `yourproject`)

### Manage, ASGI, and WSGI files

In `./yourproject/manage.py`, `./yourproject/asgi.py`, and `./yourproject/wsgi.py`, change

```
os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'myproject.settings')
```

to

```
os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'yourproject.settings')
```

### Settings

In `./yourproject/settings.py`, change

```
ROOT_URLCONF = 'myproject.urls'

...

WSGI_APPLICATION = 'myproject.wsgi.application'
```

to

```
ROOT_URLCONF = 'yourproject.urls'

...

WSGI_APPLICATION = 'yourproject.wsgi.application'
```

### Database name (technically optional)

If you want to use a different database name than `myproject`, change your database settings from

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'myproject',
        'USER': 'postgres',
        'PASSWORD': 'root',
        'HOST': os.environ.get('POSTGRES_HOST', 'localhost'),
        'PORT': '5432',
    }
}
```

to

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'yourproject',
        'USER': 'postgres',
        'PASSWORD': 'root',
        'HOST': os.environ.get('POSTGRES_HOST', 'localhost'),
        'PORT': '5432',
    }
}
```