# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:

An Django application is created inside dataproject folder.

### STEP 2:

A python program is written to create a table to store and retrieve data.

### STEP 3:

The table is created with 5 fields in which the username field is made as PrimaryKey.

### STEP 4:

Then the project files migrated. A superuser is also created.

### STEP 5:

Now the server side program is executed.

### STEP 6:

The admin page of our website is accessed using username and password.

### STEP 7:

Records are added and saved in the table inside the database.


## PROGRAM

```Model.py

from django.db import models
from django.contrib import admin
# Create your models here.


class Student (models.Model):
    Refno=models.CharField(primary_key=True,max_length=10,help_text='Refno')
    Sname=models.CharField(max_length=50)
    department=models.CharField(max_length=20)
    pnumber=models.IntegerField()
    email=models.EmailField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('Refno','Sname','department','pnumber','email')


Admin.py

from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)```



## OUTPUT
![Screenshot 2023-04-13 092205](https://user-images.githubusercontent.com/121165938/232828450-545b054a-3873-4643-a442-0111ce91a3f2.png)




## RESULT

Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).
