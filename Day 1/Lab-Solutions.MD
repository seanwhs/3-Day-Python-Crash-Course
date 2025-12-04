# 🐍 Day 1 Lab Solutions

## 🏁 Exercise 1: Hello Python

```python
# hello.py
# Prints name, age, and welcome message

print("Alice")
print(25)
print("Welcome to Python!")
```

**Example Output:**

```
Alice
25
Welcome to Python!
```

---

## 🔢 Exercise 2: Variables and Data Types

```python
# variables_and_types.py

# Create variables
your_name = "Alice"
your_age = 25
favorite_number = 7.5

# Print each variable
print(your_name)
print(your_age)
print(favorite_number)

# Bonus: Print a sentence using all three variables
print(f"{your_name} is {your_age} years old and her favorite number is {favorite_number}.")
```

---

## ➕ Exercise 3: Basic Operators

```python
# basic_operators.py

# Assign values
a = 10
b = 3

# Perform operations
print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Modulus:", a % b)

# Extra challenge: Area of rectangle
width = 5
height = 7
area = width * height
print("Area of rectangle:", area)
```

---

## 🛣️ Exercise 4: Input and Output

```python
# input_output.py

# Ask user for name and age
name = input("Enter your name: ")
age = int(input("Enter your age: "))

# Greeting message
print(f"Hello {name}! You are {age} years old.")

# Bonus: Sum, difference, product, quotient
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print("Sum:", num1 + num2)
print("Difference:", num1 - num2)
print("Product:", num1 * num2)

# Check for division by zero
if num2 != 0:
    print("Quotient:", num1 / num2)
else:
    print("Cannot divide by zero")
```

---

## 🔀 Exercise 5: Control Flow – If/Else

```python
# control_flow.py

# Part 1: Positive, negative, zero
num = float(input("Enter a number: "))
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")

# Bonus: Age categories
age = int(input("Enter your age: "))
if age < 12:
    print("Child")
elif 12 <= age < 18:
    print("Teen")
else:
    print("Adult")
```

---

## 🔀 Exercise 6: Loops

### Part A – For Loop

```python
# loops_for.py

# 1. Numbers 1–10
for i in range(1, 11):
    print(i)

# 2. Even numbers 2–20
for i in range(2, 21, 2):
    print(i)
```

### Part B – While Loop

```python
# loops_while.py

count = 0
while count < 5:
    print(count)
    count += 1
```

### Bonus: Number Guessing Game

```python
# number_guessing_game.py
import random

secret_number = random.randint(1, 10)
guess = None

while guess != secret_number:
    guess = int(input("Guess the number between 1 and 10: "))
    if guess < secret_number:
        print("Too low!")
    elif guess > secret_number:
        print("Too high!")
    else:
        print("Congratulations! You guessed it.")
```

---

## ✅ End-of-Day Mini Project

```python
# mini_project.py

# Number of users
for _ in range(3):
    name = input("Enter your name: ")
    age = int(input("Enter your age: "))
    favorite_number = float(input("Enter your favorite number: "))

    print(f"Hello {name}! In 5 years, you will be {age + 5}. "
          f"Your favorite number doubled is {favorite_number * 2}.")
    print("-" * 40)
```

---

### 💡 Notes for Trainers

* Encourage **students to test each part separately**.
* Use **print statements to debug** and understand flow.
* Reinforce the **difference between `int`, `float`, and `str`**.
* For loops and `while` loops, emphasize **range vs condition-based looping**.
* Bonus challenges help advanced learners stay engaged.

