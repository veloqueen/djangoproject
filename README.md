# djangoproject
hi, it's to remember how to set up django project! and practice some stuff!

START: 
requirements.yaml file

conda env create -f requirements.yml

django-admin startproject xxxx . 

    * Add Pycharm interpreter locally:
File > Settings > Project: xxx  > select env created on previous step

add configuration: edit: + python:
makemigrations
migrate
runserver

Create .gitignore
python manage.py startapp yourappname
django-admin startapp yourappname 

Go to settings.py, do updates of what apps are installed (do it each time you create a new app)
