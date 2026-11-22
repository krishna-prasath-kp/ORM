# Ex02 Django ORM Web Application

## Date: 22-11-2026

## AIM
To develop a Django application to store and retrieve data from an online food delivery database using Object Relational Mapping (ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM

### models.py
```python
from django.db import models

class Food(models.Model):
    food_id = models.AutoField(primary_key=True)
    name = models.CharField(max_length=100)
    restaurant = models.CharField(max_length=100)
    category = models.CharField(max_length=50)
    price = models.IntegerField()
    rating = models.FloatField()

    class Meta:
        db_table = "food_items"

    def __str__(self):
        return self.name
```

### admin.py
```python
from django.contrib import admin
from .models import Food

admin.site.register(Food)
```

## OUTPUT

![Uploading Screenshot 2026-11-22 195229.png…]()


## RESULT
Thus the program for creating a food delivery database using ORM has been executed successfully.
