# Weekend Python Crash Course 🐍  
## Day 2 Slides Outline – Functions, Data Structures & File Handling

---

## Slide 1: Title Slide
- **Title:** Weekend Python Crash Course 🐍  
- **Subtitle:** Day 2 – Functions, Data Structures & File Handling  
- **Instructor Name / Date**  
- Optional: Python logo or fun illustration  

---

## Slide 2: Day 2 Objectives
- Define and use functions with arguments and return values  
- Understand variable scope: local vs global  
- Work with lists, tuples, sets, dictionaries  
- Manipulate strings with methods and f-strings  
- Read and write text and CSV files  

---

## Slide 3: Functions – Introduction
- Reusable block of code for a specific task  
- Organizes code and avoids repetition  
- Example:
```python
def greet(name):
    print(f"Hello, {name}!")
````

---

## Slide 4: Functions – Return Values

* Functions can return a value:

```python
def add(a, b):
    return a + b
```

* Local vs Global variables

---

## Slide 5: Function Exercises

* `square(number)` – return the square
* `is_even(number)` – return True/False
* `greet_user()` – ask name, print greeting
* Bonus: `roll_dice()` – random dice roll

---

## Slide 6: Lists

* Ordered, mutable collection
* Example:

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits[0])
```

* Common methods: `append()`, `remove()`, `pop()`

---

## Slide 7: Tuples, Sets, Dictionaries

* **Tuples:** immutable ordered collection
* **Sets:** unordered, unique elements
* **Dictionaries:** key-value pairs

```python
person = {"name": "Alice", "age": 25}
print(person["name"])
```

---

## Slide 8: Data Structure Exercises

* List of movies: add and print first/last
* Tuple of cities: try modifying
* Set of numbers: add/remove elements
* Dictionary: create contacts, print keys

---

## Slide 9: Strings

* Common methods: `upper()`, `lower()`, `replace()`, `len()`
* f-Strings for formatting:

```python
name = "Alice"
age = 25
print(f"{name} is {age} years old.")
```

---

## Slide 10: String Exercises

* Combine first and last name in uppercase
* Replace vowels with `*`
* Format name, age, favorite color using f-string

---

## Slide 11: File Handling – Text Files

* Write and read files:

```python
with open("example.txt", "w") as f:
    f.write("Hello, Python!")
```

* Reading files:

```python
with open("example.txt", "r") as f:
    print(f.read())
```

---

## Slide 12: File Handling – CSV

* Writing CSV:

```python
import csv
with open("data.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Age"])
```

* Reading CSV:

```python
with open("data.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

---

## Slide 13: File Exercises

* Create text file with 5 quotes
* Read and print lines
* Create CSV file with 3 contacts, read back

---

## Slide 14: End-of-Day Mini Projects

* **Project 1:** Contact Manager (dictionary + CSV)
* **Project 2:** Quiz Game (list of questions, track score)

---

## Slide 15: Tips & Best Practices

* Use functions to organize code
* Test small snippets first
* Comment your code
* Keep files organized

---

## Slide 16: Resources

* [Python Official Documentation – Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
* [Automate the Boring Stuff – Functions & Files](https://automatetheboringstuff.com/)
* [W3Schools Python Tutorial](https://www.w3schools.com/python/)

---

## Slide 17: Thank You / Next Steps

* Preview Day 3 topics: Object-Oriented Programming (OOP), Libraries, Mini Projects
* Encourage learners to complete Day 2 exercises
* Q&A

---

```

---

This **Day 2 Slides Outline**:  
- Covers all key concepts and exercises  
- Includes examples and code snippets  
- Matches the Learner Guide and Lab Sheet  

