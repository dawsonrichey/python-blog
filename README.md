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
-----------------------------------------------
python manage.py createsuperuser
python manage.py runserver
-----------------------------
python manage.py shell
    from django.contrib.auth.models import User
    from blog.models import Post
    user = User.objects.get(username='admin')
    Post.objects.create(title='One more post',slug='one-more-post',body='Post body.',author=user)
    <Post: One more post>
----------------------------------
Post.title="New Title"
all_posts = Post.objects.all()
Post.objects.all()
--query set
Post.objects.filter(publish__year=2018)
Post.object.filter(publish__year=2018, author__username='admin')
Post.object.filter(publish__year)=2016)\
.filter(author__username='admin')
.exclude(title__startswith='why')
Post.objects.order_by('-title')
post = Post.objects.get(id=1)
post.delete()
---------------------------------------------------------------
