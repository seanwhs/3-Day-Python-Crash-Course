# 🐍 Weekend Python Crash Course – Post-Course Assessment

**Total Duration:** 90–120 minutes
**Instructions:** Answer all questions. For coding tasks, write correct and working Python code. You may use comments for explanations where needed.

---

## **Part 1: Multiple Choice Questions (MCQs)**

1. Which of the following statements is correct about Python classes?
   a) Classes cannot have methods.
   b) Classes can have attributes and methods.
   c) Python does not support classes.
   d) Objects are not related to classes.

2. What does the `self` keyword in Python refer to?
   a) A global variable
   b) The current object instance
   c) A function parameter
   d) The class itself

3. What will this code output?

```python
import math
print(math.factorial(4))
```

a) 24
b) 12
c) 8
d) 16

4. Which of the following libraries is **NOT** part of Python standard libraries?
   a) `random`
   b) `datetime`
   c) `pandas`
   d) `math`

5. Which method is used to add an item to a list?
   a) `append()`
   b) `add()`
   c) `insert_item()`
   d) `extend_item()`

---

## **Part 2: True/False**

1. A Python object can have multiple methods. (True / False)
2. A dictionary key must be immutable. (True / False)
3. The `datetime.now()` function returns the current date and time. (True / False)
4. You can call a class method without creating an object if it’s decorated with `@staticmethod`. (True / False)
5. Using OOP makes large Python programs easier to manage. (True / False)

---

## **Part 3: Short Answer / Code Output**

1. What does this code print?

```python
class Animal:
    def __init__(self, species):
        self.species = species

a = Animal("Dog")
print(a.species)
```

2. Write Python code to **roll two dice** using the `random` library and print their sum.

3. Create a `Car` class with attributes `make`, `model`, and `year`. Add a method `age()` that calculates the car’s age based on the current year. Show an example using 2025 as the current year.

4. Using `pandas`, create a DataFrame with columns: `Product`, `Price`, `Stock`. Add 3 rows of data and display the DataFrame.

5. Write Python code to **shuffle a list of 5 numbers** using `random.shuffle()` and print the shuffled list.

---

## **Part 4: Mini Project / Problem Solving**

1. **Quiz Game**: Write a Python program that asks **3 questions**, keeps score, and prints the final score. Use lists or classes if needed.

2. **Bank Account Simulation**: Create a `BankAccount` class with `deposit()`, `withdraw()`, and `balance` attributes. Demonstrate depositing 1000 and withdrawing 250.

3. **Budget Tracker**: Write a small program to store **3 expenses** in a list of dictionaries (`name` and `amount`) and calculate the total.

4. Write a function `print_uppercase_name()` that asks for the user’s first and last name and prints it in **uppercase**.

5. Explain in 2–3 sentences why **combining OOP, functions, and libraries** is beneficial in mini projects.

---

## **Answer Key – Post-Course Assessment**

### **Part 1: MCQs**

1. **b) Classes can have attributes and methods**
2. **b) The current object instance**
3. **a) 24**
4. **c) pandas**
5. **a) append()**

---

### **Part 2: True/False**

1. True
2. True
3. True
4. True
5. True

---

### **Part 3: Short Answer / Code Output**

1. `Dog`
2. ```python
   ```

import random

die1 = random.randint(1,6)
die2 = random.randint(1,6)
print("Sum:", die1 + die2)

````
3. ```python
from datetime import datetime

class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def age(self, current_year):
        return current_year - self.year

car = Car("Toyota", "Corolla", 2018)
print("Car age:", car.age(2025))
````

4. ```python
   ```

import pandas as pd

data = {
"Product": ["Laptop", "Mouse", "Keyboard"],
"Price": [1200, 25, 45],
"Stock": [5, 50, 20]
}

df = pd.DataFrame(data)
print(df)

````
5. ```python
import random

numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print(numbers)
````

---

### **Part 4: Mini Project / Problem Solving**

1. **Quiz Game Example**

```python
questions = [
    {"q":"2+2=", "a":"4"},
    {"q":"Capital of France?", "a":"Paris"},
    {"q":"Python keyword to define a function?", "a":"def"}
]

score = 0
for q in questions:
    ans = input(q["q"] + " ")
    if ans.strip().lower() == q["a"].lower():
        score += 1

print(f"Final score: {score}/{len(questions)}")
```

2. **Bank Account Simulation**

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

account = BankAccount("Alice")
account.deposit(1000)
account.withdraw(250)
```

3. **Budget Tracker**

```python
expenses = [
    {"name":"Groceries","amount":50},
    {"name":"Transport","amount":20},
    {"name":"Entertainment","amount":30}
]

total = sum(item["amount"] for item in expenses)
print(f"Total spent: ${total}")
```

4. **Uppercase Name Function**

```python
def print_uppercase_name():
    first = input("First name: ")
    last = input("Last name: ")
    print(f"{first} {last}".upper())

print_uppercase_name()
```

5. **Explanation**
   Combining **OOP, functions, and libraries** allows mini projects to be **modular, reusable, and more powerful**. OOP structures the code, functions make tasks reusable, and libraries provide ready-made tools for real-world applications.

