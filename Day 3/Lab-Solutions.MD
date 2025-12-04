# 🐍 Day 3 Lab Solutions

## 🏁 Exercise 1: Object-Oriented Programming (OOP)

### Task 1: Car Class

```python
# oop_examples.py

# 1. Define Car class
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"Car: {self.make} {self.model}, Year: {self.year}")

# Create car objects
car1 = Car("Toyota", "Corolla", 2015)
car2 = Car("Honda", "Civic", 2018)

# Display info
car1.display_info()
car2.display_info()
```

### Task 2: Add age() method

```python
from datetime import datetime

class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"Car: {self.make} {self.model}, Year: {self.year}")

    def age(self):
        current_year = datetime.now().year
        return current_year - self.year

# Test
car1 = Car("Toyota", "Corolla", 2015)
car2 = Car("Honda", "Civic", 2018)

print(f"{car1.make} age: {car1.age()} years")
print(f"{car2.make} age: {car2.age()} years")
```

### Task 3: BankAccount Class (Optional Challenge)

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited ${amount}. New balance: ${self.balance}")

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient funds!")
        else:
            self.balance -= amount
            print(f"Withdrew ${amount}. New balance: ${self.balance}")

# Test accounts
account1 = BankAccount("Alice", 1000)
account1.deposit(500)
account1.withdraw(300)
account1.withdraw(1500)  # insufficient funds
```

---

## 🔢 Exercise 2: Python Libraries

### Standard Libraries

```python
# library_exercises.py
import random
from datetime import datetime
import math

# 1. Random: Roll two dice
die1 = random.randint(1, 6)
die2 = random.randint(1, 6)
print(f"Dice rolled: {die1} + {die2} = {die1 + die2}")

# 2. DateTime: Current date and time
now = datetime.now()
print("Current date and time:", now.strftime("%Y-%m-%d %H:%M"))

# 3. Math: sqrt, power, factorial
num = 5
print("Square root:", math.sqrt(num))
print("Power 5^3:", math.pow(num, 3))
print("Factorial:", math.factorial(num))
```

### Optional Libraries

```python
# Optional: pandas and requests
import pandas as pd
import requests

# 1. pandas DataFrame
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 22],
    "City": ["Paris", "Tokyo", "New York"]
}
df = pd.DataFrame(data)
print(df)

# 2. requests (optional)
# response = requests.get("https://api.github.com")
# print(response.json())
```

---

## 🛠 Exercise 3: Mini Projects

### Project 1: Quiz Game (Text-Based)

```python
# mini_projects_solutions.py

import random

class Question:
    def __init__(self, prompt, answer):
        self.prompt = prompt
        self.answer = answer

questions = [
    Question("What is the capital of France? ", "Paris"),
    Question("2 + 2 = ", "4"),
    Question("Python keyword to define function? ", "def")
]

score = 0
random.shuffle(questions)

for q in questions:
    user_answer = input(q.prompt)
    if user_answer.strip().lower() == q.answer.strip().lower():
        print("Correct!")
        score += 1
    else:
        print(f"Wrong! The correct answer is {q.answer}")

print(f"Your final score is {score}/{len(questions)}")
```

---

### Project 2: Small Utility – Budget Tracker

```python
# budget_tracker.py

budget = []

def add_expense(name, amount):
    budget.append({"name": name, "amount": amount})
    print(f"Added {name}: ${amount}")

def view_budget():
    total = 0
    print("Expenses:")
    for item in budget:
        print(f"{item['name']}: ${item['amount']}")
        total += item['amount']
    print(f"Total spent: ${total}")

# Example Usage
add_expense("Groceries", 50)
add_expense("Transport", 15)
view_budget()
```

---

## ✅ End-of-Day Challenge Solution Idea

**Combined Project:** Quiz Game using OOP and libraries

* Use `Question` class (OOP)
* Randomize questions with `random.shuffle()`
* Track score and optionally store results in `pandas.DataFrame` for display:

```python
import random
import pandas as pd

class Question:
    def __init__(self, prompt, answer):
        self.prompt = prompt
        self.answer = answer

questions = [
    Question("Capital of France? ", "Paris"),
    Question("5 + 7 = ", "12"),
    Question("Python function keyword? ", "def")
]

random.shuffle(questions)
results = []

score = 0
for q in questions:
    answer = input(q.prompt)
    correct = answer.strip().lower() == q.answer.lower()
    results.append({"Question": q.prompt, "Your Answer": answer, "Correct": correct})
    if correct:
        score += 1

df = pd.DataFrame(results)
print("\nQuiz Results:")
print(df)
print(f"Final Score: {score}/{len(questions)}")
```

---

### 💡 Trainer Notes

* Highlight **OOP benefits**: modular, reusable, scalable code.
* Encourage **library exploration** (`random`, `math`, `datetime`), then optional ones (`pandas`, `requests`).
* Mini-projects integrate **everything learned**: classes, loops, functions, libraries, and file I/O.
* Suggest learners **add enhancements**: error handling, input validation, more questions, or extended functionality.

