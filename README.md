# Django ORM Web Application

## AIM

To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:

Create django application

### STEP 2:

Write code in models.py and admin.py

### STEP 3:

End of the program

## PROGRAM

### models.py
```python
from django.db import models
from django.contrib import admin

# Create your models here.

class Student (models.Model):
    referencenumber=models.CharField(max_length=20,primary_key=True,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    department=models.CharField(max_length=30)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','department')
```

### admin.py
```python
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```

## OUTPUT

### serveroutput
![so (2)](https://user-images.githubusercontent.com/91368803/233094322-425f520d-d551-4dc4-bf3b-3f76b1bb2ca6.png)

### clientoutput
![co](https://user-images.githubusercontent.com/91368803/233094423-311d5aa5-454d-497c-a947-c85beb26881b.png)



## RESULT
Thus the program has been executed successfully
