# python-blog
C:\Windows\SysWOW64
-------------------

pip install virtualenv

virtualenv my_env 
-------------------------

my_env\Scripts\activate
my_env\Scripts\deactivate
---------------------------
pip install Django==1.8.6
python
import django
django.VERSION
____________________________
Start Project
____________________________

django-admin startproject mysite
cd mysite
python manage.py migrate
python manage.py runserver
----------------------------------------------------------
/* python manage.py runserver 127.0.0.1:8001 */
    go to django wsgi to learn to deploy for production
from the root directory mysite
---------------------------------------------------------------
python manage.py startapp blog
--------------------------------------------------------------
pip install pytz
python manage.py makemigrations blog
python manage.py sqlmigrate blog 0001
python manage.py migrate