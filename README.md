# Python & Django Install 
01. Python Install & check python --version
02. Check pip & Check django => python -m django --version
03. IDE Install
04. pip install django

# Create django project
django-admin startproject #project nme#
  
# Create App
projectName>> python manage.py startapp #appName#  

# The development server
projectName>> python manage.py runserver

# Migrate database
python manage.py migrate

python manage.py makemigrations

Python manage.py makemigrations a

# Creating an admin user
python manage.py createsuperuser

# Django URL patterns
# Project Urls :
from django.contrib import admin 
from django.urls import path, include 

urlpatterns = [
  path('admin/', admin.site.urls),
  path('', include('books.urls')), 
] 

# App Urls :
from django.urls import path 
from . import views 

urlpatterns = [ 
	path('books/<int:pk>/', views.book_detail, name="book_detail"), 
	path('books/<str:genre>/', views.books_by_genre, name="books_by_genre"), 
	path('books/', views.book_index, name="book_index"), 
] 




