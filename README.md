# Steps

## Create the project directory

mkdir DjangoExample

cd DjangoExample

## Create a virtual environment to isolate our package dependencies locally

python -m venv env

env\Scripts\activate

## Install Django and Django REST framework into the virtual environment

pip install django

pip install djangorestframework

## Set up a new project with a single application

django-admin startproject djangocrud .  # Note the trailing '.' character

cd tutorial

django-admin startapp api

cd ..


python manage.py migrate

python manage.py createsuperuser

/** Follow code **/

1. Create Serializers
2. Create view
3. create url
4. create model

python manage.py makemigrations

python manage.py migrate

//Register model to admin. Keep below code in admin.py

from django.contrib import admin

from .models import Movie

admin.site.register(Movie)

//allow cors

pip install django-cors-headers

//keep this code in settings.py

CORS_ORIGIN_WHITELIST = (
    'localhost:4200'  //url which u try to access
)
