# Weekend Python Crash Course 🐍  
## Day 2: Learner Guide – Functions, Data Structures & File Handling

---

## 📚 Objectives
By the end of Day 2, you will be able to:

1. Define and use functions with arguments and return values.  
2. Understand variable scope (local vs global).  
3. Work with Python data structures: lists, tuples, sets, dictionaries.  
4. Manipulate strings with methods and formatting.  
5. Read and write text and CSV files.  
6. Complete exercises to apply functions and data structures.

---

## 🏁 1. Functions

### What is a Function?
- A reusable block of code that performs a specific task.  
- Helps organize code and avoid repetition.

### Defining a Function
```python
def greet(name):
    print(f"Hello, {name}!")
````

### Function with Return Value

```python
def add(a, b):
    return a + b
```

### Scope

* **Local variables** exist only inside a function.
* **Global variables** can be accessed anywhere.

### Exercises

1. Write a function `square(number)` that returns the square of a number.
2. Create a `greet_user()` function that asks for a name and prints a greeting.
3. Write a function `is_even(number)` that returns `True` if even, else `False`.

---

## ➕ 2. Lists, Tuples, Sets, Dictionaries

### Lists

* Ordered, mutable collection.

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits[0])  # apple
```

### Tuples

* Ordered, immutable collection.

```python
colors = ("red", "green", "blue")
```

### Sets

* Unordered, unique elements.

```python
numbers = {1, 2, 3, 3}
print(numbers)  # {1, 2, 3}
```

### Dictionaries

* Key-value pairs.

```python
person = {"name": "Alice", "age": 25}
print(person["name"])
```

### Exercises

1. Create a list of 5 favorite movies and print them.
2. Make a tuple of 3 cities you want to visit.
3. Create a set of numbers, add a new number, and print the set.
4. Create a dictionary for a contact book with 2 entries and print each contact.

---

## 🛠 3. Strings

### Common String Methods

```python
text = "Python is fun"
print(text.upper())
print(text.lower())
print(text.replace("fun", "awesome"))
print(len(text))
```

### f-Strings

```python
name = "Alice"
age = 25
print(f"{name} is {age} years old.")
```

### Exercises

1. Ask the user for their first and last name and print them together in uppercase.
2. Replace all vowels in a string with `*`.
3. Format a string using f-string to display name and favorite color.

---

## 📄 4. File Handling

### Reading and Writing Files

```python
# Writing to a file
with open("example.txt", "w") as f:
    f.write("Hello, Python!\nThis is Day 2.\n")

# Reading a file
with open("example.txt", "r") as f:
    content = f.read()
    print(content)
```

### CSV Files

```python
import csv

# Writing CSV
with open("data.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Alice", 25])
    writer.writerow(["Bob", 30])

# Reading CSV
with open("data.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

### Exercises

1. Create a text file and write 5 lines of your favorite quotes.
2. Read the file and print each line.
3. Write a CSV file with 3 contacts (name, phone, email) and read it back.

---

## 💡 Tips for Day 2

* Use functions to break large tasks into smaller pieces.
* Test your functions separately before using them in programs.
* Keep your files organized in folders for easy access.
* Experiment with different data structures for practice.

---

## ✅ End-of-Day Mini Project

**Project 1: Contact Manager**

* Create a program that:

  1. Stores contacts in a **dictionary** (name, phone, email).
  2. Lets the user **add**, **view**, and **search** contacts.
  3. Saves contacts to a **CSV file**.

**Project 2: Simple Quiz**

* Create a **list of questions** and answers.
* Ask the user questions in a loop and track the score.
* Print the final score using f-strings.

---

## 📚 Resources

* [Python Official Documentation – Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
* [Automate the Boring Stuff with Python – Functions & Files](https://automatetheboringstuff.com/)
* [W3Schools Python Tutorial](https://www.w3schools.com/python/)

---

```

---

This **Day 2 Learner Guide** covers:  
- Functions  
- Lists, Tuples, Sets, Dictionaries  
- Strings and formatting  
- File I/O (text & CSV)  
- Mini-projects to consolidate learning  

