# djangoproject SETUP with PyCharm as IDE
hi, it's to remember how to set up django project! and practice some stuff!

START: 
create requirements.yaml file with all desired dependencies 
create a .gitignore file

   * $ conda env create -f requirements.yml
creates a conda env

$pip install what-you-want-to-install and it's version
   in case of manuall installations of dependencies, frameworks use pip

> $ conda activate nameofyourprojectorisitenv 
this will be advised by terminal itself

`django-admin startproject your-wished-name . `
   (dot at the end so that it's created in a directory you're in 

    * Add Pycharm interpreter locally:
File > Settings > Project: yourprojectname  > Conda Environment > tick Existing environemnt -> select env created on previous step & apply&ok

  * Add configuration: edit: + python:
Name: makemigrations, migrate, runserver
parameters makemigrations, migrate, runserver (separately copy paste first one and adjust for two remaining) after $
Script path: the one to manage.py
parameters makemigrations, migrate, runserver (separately copy paste first one and adjust for two remaining) after $


    - MAKEMIGRATIONS
    $ python manage.py makemigrations 

    - MIGRATE
    $ python manage.py migrate

    - RUNSERVER
    $ python manage.py runserver

above three commands are your best friends, need to be run once in the same directory as manage.py

if you want a custom user profile, best is to set it up before running migrations for the first time (AUTH_USER_MODEL in settings & more) 

CREATE SUPER USER: 
$ python manage.py createsuperuser

ADD NEW APP
$ python manage.py startapp yourappname or $django-admin startapp yourappname 

upon created new app, go to settings.py, do updates of what apps are installed (do it each time you create a new app)

ADMIN PAGE:
To display apps in the admin page on local server: add to the app.py 
from django.apps import AppConfig
class Your-App_nameConfig(AppConfig):
    name = 'yourappname'
    
    
    Other commands that might be needed when setting up Django project: 
    $ conda env list 

