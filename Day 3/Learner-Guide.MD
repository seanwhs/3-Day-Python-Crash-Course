# Weekend Python Crash Course 🐍  
## Day 3: Learner Guide – OOP, Libraries & Mini Projects

---

## 📚 Objectives
By the end of Day 3, you will be able to:

1. Understand Object-Oriented Programming (OOP) basics: classes, objects, attributes, and methods.  
2. Create simple classes and use them in Python programs.  
3. Explore useful Python libraries (`random`, `datetime`, `math`, `requests`, `pandas`).  
4. Complete mini projects using Python fundamentals, OOP, and libraries.  

---

## 🏁 1. Object-Oriented Programming (OOP)

### What is OOP?
- A programming paradigm using **objects** and **classes** to model real-world entities.  
- Encourages modular, reusable code.

### Class and Object Example
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

# Create objects
person1 = Person("Alice", 25)
person2 = Person("Bob", 30)

person1.greet()
person2.greet()
````

### Exercises

1. Create a `Car` class with `make`, `model`, and `year` attributes.
2. Add a method `display_info()` that prints the car details.
3. Create 2 car objects and call `display_info()` for each.

---

## ➕ 2. Python Libraries

### Standard Libraries

* **random**: generate random numbers, shuffle lists
* **datetime**: work with dates and times
* **math**: mathematical functions

```python
import random
print(random.randint(1, 10))

from datetime import datetime
print(datetime.now())

import math
print(math.sqrt(16))
```

### Optional Libraries

* **requests**: access web APIs
* **pandas**: handle data in tables (DataFrames)

```python
import pandas as pd

data = {"Name": ["Alice", "Bob"], "Age": [25, 30]}
df = pd.DataFrame(data)
print(df)
```

### Exercises

1. Use `random` to simulate rolling two dice and print the sum.
2. Use `datetime` to print current date and time in `YYYY-MM-DD HH:MM` format.
3. Create a simple `pandas` DataFrame with 3 rows of data and display it.

---

## 🛠 3. Mini Projects

### Project 1: Text-Based Adventure Game

* Create a game using **functions**, **loops**, and **OOP** concepts.
* Examples:

  * Quiz game with points
  * Adventure game with choices

### Project 2: Simple Utility Program

* Create a small Python tool, such as:

  * Budget tracker
  * Contact manager (extend Day 2)
  * Log analyzer

### Tips for Mini Projects

* Break tasks into functions and classes.
* Test each part before combining.
* Use libraries where appropriate (e.g., `random` for game events).

---

## 💡 Tips for Day 3

* Encourage creativity and experimentation in mini projects.
* Guide learners on structuring code with OOP principles.
* Demonstrate library usage with small, real-world examples.
* Offer optional challenges for advanced learners (e.g., API access using `requests`).

---

## 📚 Resources

* [Python Official Documentation – Classes](https://docs.python.org/3/tutorial/classes.html)
* [Automate the Boring Stuff with Python – Classes & Modules](https://automatetheboringstuff.com/)
* [Python Standard Library Documentation](https://docs.python.org/3/library/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)

---

## 🎯 Outcome

By the end of Day 3, participants will be able to:

* Understand and apply OOP basics in Python
* Use Python standard and optional libraries effectively
* Build fun, small Python projects independently
* Plan and organize Python code for real-world tasks

---

```

---

This **Day 3 Learner Guide** covers:  
- OOP fundamentals (classes, objects, attributes, methods)  
- Python libraries (`random`, `datetime`, `math`, optional `requests` and `pandas`)  
- Mini projects to consolidate learning  

