# Django Basics
Django is a Python-based web framework which allows you to quickly create web application without all of the installation or dependency problems that you normally will find with other frameworks.

# Why Django?

<pre>
01. Django is a rapid web development framework that can be used to develop fully fleshed web applications in a short period of time.
02. It’s very easy to switch database in Django framework.
03. It has built-in admin interface which makes easy to work with it.
04. Django is fully functional framework that requires nothing else.
05 .It has thousands of additional packages available.
06. It is very scalable
</pre>

# Python & Django Install 
<pre>
01. Python Install & check python --version
02. Check pip & Check django => python -m django --version
03. IDE Install
04. pip install django / py -m pip install Django
</pre>

# Create django project
<pre> django-admin startproject #project nme# </pre>  
# Create App
<pre> python manage.py startapp #appName# </pre> 

# The development server
<pre> python manage.py runserver </pre>

# Application definition
<pre>
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'myapp', //Ur app name
]
</pre>

# Template Directory Path
<pre>
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR, 'templates')], // Custome setting
        'APP_DIRS': True,
        ...
    },
]
</pre>
# Create database
python manage.py migrate

python manage.py makemigrations

Python manage.py makemigrations a

# Creating an admin user
python manage.py createsuperuser

# Django URL patterns
# Project Urls :
<pre>
from django.contrib import admin 
from django.urls import path, include 

urlpatterns = [
  path('admin/', admin.site.urls),
  path('', include('books.urls')), 
] 
</pre>
# App Urls :
<pre>
from django.urls import path 
from . import views 

urlpatterns = [ 
	path('', views.home, name="home"), 
	path('about/', views.about, name="about"),
] 
</pre>

# Django View
# Types of Views
<pre>
01. Function Based Views
02. Class Based Views
</pre>

# Managing static files (e.g. images, JavaScript, CSS)



https://www.geeksforgeeks.org/django-tutorial/

