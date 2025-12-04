# Weekend Python Crash Course 🐍  
## Day 1: Python Basics & Core Concepts – Learner Guide

---

## 📚 Objectives
By the end of Day 1, you will be able to:

1. Understand what Python is and why it is popular.  
2. Install Python and set up an IDE (VS Code / PyCharm / Jupyter Notebook).  
3. Run your first Python scripts and use the REPL.  
4. Understand variables and data types.  
5. Write programs using basic operators and input/output.  
6. Implement control flow using `if`, `elif`, `else`, and loops (`for`, `while`).  

---

## 🏁 1. Getting Started with Python

### What is Python?
- Python is a high-level, interpreted programming language.  
- Known for readability, versatility, and a large community.  

### Setting Up Your Environment
1. Install **Python** from [python.org](https://www.python.org/downloads/).  
2. Choose an IDE:  
   - [VS Code](https://code.visualstudio.com/)  
   - [PyCharm](https://www.jetbrains.com/pycharm/)  
   - [Jupyter Notebook](https://jupyter.org/install)  
3. Test your installation:
```bash
python --version
````

### Running Your First Script

1. Open your IDE or terminal.
2. Create a new file `hello.py`.
3. Type the following:

```python
print("Hello, Python!")
```

4. Run the script and see the output.

---

## 🔢 2. Variables and Data Types

### Variables

* Used to store data values.

```python
name = "Alice"
age = 25
height = 1.65
```

### Data Types

| Type  | Example      |
| ----- | ------------ |
| int   | 25           |
| float | 1.65         |
| str   | "Alice"      |
| bool  | True / False |

### Exercises

1. Create variables for your **name**, **age**, and **favorite number**.
2. Print a sentence introducing yourself using your variables.

---

## ➕ 3. Basic Operators

### Arithmetic Operators

```python
a = 10
b = 3
print(a + b)  # Addition
print(a - b)  # Subtraction
print(a * b)  # Multiplication
print(a / b)  # Division
print(a % b)  # Modulus
```

### Exercises

* Calculate the area of a rectangle with width=5 and height=7.
* Convert temperature from Celsius to Fahrenheit using the formula:

```python
F = (C * 9/5) + 32
```

---

## 🛣️ 4. Input and Output

### Getting Input

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

### Exercises

* Ask the user for **two numbers** and print their **sum**.
* Ask the user for their **age** and print **how old they will be in 5 years**.

---

## 🔀 5. Control Flow

### If / Else

```python
age = int(input("Enter your age: "))
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

### Exercises

* Ask the user for a number and print if it is **positive, negative, or zero**.

### Loops

#### For Loop

```python
for i in range(5):
    print(i)
```

#### While Loop

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Exercises

1. Print all **even numbers** from 1 to 20.
2. Write a **number guessing game** where the program selects a number between 1–10, and the user guesses until correct.

---

## 💡 Tips for Today

* Save your scripts often.
* Use comments to explain your code:

```python
# This is a comment
```

* Don’t worry about mistakes — debugging is part of learning.
* Experiment with the code! Try changing numbers, strings, and conditions.

---

## ✅ End-of-Day Challenge

Create a small program that:

1. Asks the user for their **name**, **age**, and **favorite number**.
2. Prints a message like:

```
Hello Alice! In 5 years, you will be 30 years old. Your favorite number doubled is 42.
```

3. Bonus: Add a loop to repeat this for **3 different users**.

---

## 📚 Resources

* [Python Official Documentation](https://docs.python.org/3/)
* [Replit Online IDE](https://replit.com/)
* [W3Schools Python Tutorial](https://www.w3schools.com/python/)

---

```

---

This **Day 1 Learner Guide** includes:  
- Concepts explanations  
- Code examples  
- Exercises and mini-projects  
- Tips and references  

