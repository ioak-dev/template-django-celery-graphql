# Start Server locally

## First time

- pip install virtualenv
- pip install virtualenvwrapper-win
- mkvirtualenv appnamehere
- pip install -r requirements.txt
- python manage.py runserver

## Every time

- workon appnamehere
- python manage.py runserver

## Procfile Honcho for celery

web: gunicorn appnamehere.wsgi --log-file
worker1: celery -A appnamehere beat -l info
worker2: celery -A appnamehere worker -l info
