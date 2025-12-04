# Weekend Python Crash Course 🐍  
## Day 3 Slides Outline – OOP, Libraries & Mini Projects

---

## Slide 1: Title Slide
- **Title:** Weekend Python Crash Course 🐍  
- **Subtitle:** Day 3 – Object-Oriented Programming, Libraries & Mini Projects  
- **Instructor Name / Date**  
- Optional: Python / coding illustration  

---

## Slide 2: Day 3 Objectives
- Understand OOP basics: classes, objects, attributes, methods  
- Create and use simple classes in Python  
- Explore Python libraries: `random`, `datetime`, `math`, `pandas`, `requests`  
- Complete mini projects combining all concepts  

---

## Slide 3: Object-Oriented Programming (OOP) – Introduction
- Programming paradigm using **objects** and **classes**  
- Encourages modular, reusable code  
- Example class:
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
````

---

## Slide 4: Objects & Methods

* Objects are instances of classes
* Methods define behavior of objects

```python
def greet(self):
    print(f"Hello, my name is {self.name}.")
```

* Create objects and call methods:

```python
person1 = Person("Alice", 25)
person1.greet()
```

---

## Slide 5: OOP Exercises

* Create a `Car` class with `make`, `model`, `year`
* Add method `display_info()`
* Optional: add `age()` method to calculate car age
* Optional challenge: `BankAccount` class with deposit/withdraw

---

## Slide 6: Python Libraries – Standard Libraries

* **random**: generate random numbers, shuffle, pick random item
* **datetime**: current date and time, formatting
* **math**: sqrt, power, factorial

```python
import random
print(random.randint(1,6))
```

---

## Slide 7: Python Libraries – Optional Libraries

* **pandas**: create and manipulate tables (DataFrames)
* **requests**: fetch web data via APIs

```python
import pandas as pd
data = {"Name": ["Alice", "Bob"], "Age": [25, 30]}
df = pd.DataFrame(data)
print(df)
```

---

## Slide 8: Library Exercises

* Use `random` to roll two dice
* Use `datetime` to print current date/time
* Use `math` for sqrt, factorial, power
* Optional: create a `pandas` DataFrame

---

## Slide 9: Mini Projects – Overview

* **Project 1:** Text-Based Adventure / Quiz Game

  * Functions + loops + optional OOP
  * Track score or progress
* **Project 2:** Small Utility Program

  * Budget tracker, contact manager, log analyzer
  * Extend concepts from Day 2

---

## Slide 10: Mini Project Tips

* Break projects into **functions** and **classes**
* Test each component individually
* Use libraries where helpful (`random`, `datetime`, `pandas`)
* Add optional enhancements for advanced learners

---

## Slide 11: End-of-Day Challenge

* Combine **OOP**, **functions**, and **libraries** in a single project
* Example: Quiz Game using Question objects, random selection, and scoring displayed with `pandas` or formatted print

---

## Slide 12: Resources

* [Python Official Documentation – Classes](https://docs.python.org/3/tutorial/classes.html)
* [Automate the Boring Stuff with Python – Classes & Modules](https://automatetheboringstuff.com/)
* [Python Standard Library Documentation](https://docs.python.org/3/library/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)

---

## Slide 13: Wrap-Up & Next Steps

* Recap OOP concepts, libraries, and mini-projects
* Encourage completing optional exercises
* Tips for continuing learning: automation, web dev, or data science
* Q&A

---

```

---

This **Day 3 Slides Outline**:  
- Covers OOP basics with examples  
- Includes library demos and exercises  
- Guides learners through mini-projects and challenges  

