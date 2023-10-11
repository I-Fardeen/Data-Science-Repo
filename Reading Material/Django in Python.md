# Django in Python Cheat Sheet 🌐🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Django cheat sheet! Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Whether you're a beginner or an experienced developer, this cheat sheet will help you understand and use Django for web application development.

## Installation

You can install Django using pip:

```python
pip install Django
```

## Code Examples

### Creating a Django Project

To create a new Django project, run:

```python
django-admin startproject projectname
```

### Creating a Django App

To create a new Django app, run:

```python
python manage.py startapp appname
```

### Define Models

```python
from django.db import models

class MyModel(models.Model):
    field1 = models.CharField(max_length=100)
    field2 = models.IntegerField()
    # Add more fields

    def __str__(self):
        return self.field1
```

### Create Migrations

To create database migrations for your models:

```python
python manage.py makemigrations
```

### Apply Migrations

To apply migrations and create database tables:

```python
python manage.py migrate
```

### Create a Superuser

To create an admin superuser:

```python
python manage.py createsuperuser
```

### Create Views

```python
from django.http import HttpResponse
from django.shortcuts import render

def my_view(request):
    return HttpResponse("Hello, Django!")

def my_template_view(request):
    return render(request, 'template.html', context={'data': 'Django is cool!'})
```

### Create URLs

```python
from django.urls import path
from . import views

urlpatterns = [
    path('myview/', views.my_view),
    path('mytemplateview/', views.my_template_view),
]
```

### Template Rendering

Create an HTML template and render it using the `render` function in views.

### Admin Panel

Django provides an admin panel to manage data. Access it at `/admin` and log in with the superuser credentials.

### Forms

Django simplifies form handling, including form creation and validation.

### Authentication

Django includes user authentication views and functionality.

### Static Files

Manage and serve static files (CSS, JavaScript, etc.) with ease.

This cheat sheet provides a glimpse into Django's capabilities and code examples to get you started. Django is a powerful framework for web application development, and its comprehensive documentation is a valuable resource.

📖 Django Documentation: [Django Documentation](https://docs.djangoproject.com/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and web development content. Enjoy your journey with Django! 🚀🌐📝

Made with :heart: by **Fardeen Ahmad Khan**
