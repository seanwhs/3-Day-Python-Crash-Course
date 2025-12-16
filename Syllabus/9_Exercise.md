# Exercises - OOP

1. Create a class called **`Rectangle`** with attributes **`length`** and **`width`**. Create a method called **`area`** that returns the area of the rectangle.

```
pythonCopy code
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

```

1. Create a class called **`Circle`** with attribute **`radius`**. Create a method called **`area`** that returns the area of the circle and a method called **`perimeter`** that returns the perimeter of the circle.

```
pythonCopy code
import math

class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return math.pi * self.radius ** 2

    def perimeter(self):
        return 2 * math.pi * self.radius

```

1. Create a class called **`Employee`** with attributes **`name`** and **`salary`**. Create a method called **`raise_salary`** that increases the salary of the employee by a certain percentage.

```
pythonCopy code
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def raise_salary(self, percentage):
        self.salary += self.salary * percentage / 100

```

1. Create a class called **`BankAccount`** with attributes **`balance`** and **`interest_rate`**. Create methods called **`deposit`** and **`withdraw`** that update the balance attribute accordingly.

```
pythonCopy code
class BankAccount:
    def __init__(self, balance, interest_rate):
        self.balance = balance
        self.interest_rate = interest_rate

    def deposit(self, amount):
        self.balance += amount

    def withdraw(self, amount):
        self.balance -= amount

```

1. Create a class called **`Book`** with attributes **`title`**, **`author`**, and **`year`**. Create a method called **`get_age`** that returns the age of the book in years.

```
pythonCopy code
import datetime

class Book:
    def __init__(self, title, author, year):
        self.title = title
        self.author = author
        self.year = year

    def get_age(self):
        current_year = datetime.datetime.now().year
        return current_year - self.year

```
