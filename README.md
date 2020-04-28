# Python & Django Install 
<pre>
01. Python Install & check python --version
02. Check pip & Check django => python -m django --version
03. IDE Install
04. pip install django
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
	path('books/"<"int:pk">"/', views.book_detail, name="book_detail"), 
	path('books/<str:genre>/', views.books_by_genre, name="books_by_genre"), 
	path('books/', views.book_index, name="book_index"), 
] 
</pre>

# Django View\
# Types of Views
<pre>
01. Function Based Views
02. Class Based Views
</pre>

# Managing static files (e.g. images, JavaScript, CSS)

