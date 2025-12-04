# 🐍 Day 3 Quiz – OOP, Python Libraries & Mini Projects

---

## **Part 1: Multiple Choice Questions (MCQs)**

1. Which of the following is used to create a class in Python?
   a) `def`
   b) `class`
   c) `object`
   d) `init`

2. What will this code output?

```python
class Car:
    def __init__(self, make):
        self.make = make

car = Car("Toyota")
print(car.make)
```

a) Car
b) Toyota
c) make
d) Error

3. Which method is used to initialize an object’s attributes in Python?
   a) `__str__`
   b) `__init__`
   c) `__main__`
   d) `__del__`

4. Which library is used to generate random numbers in Python?
   a) `math`
   b) `random`
   c) `datetime`
   d) `pandas`

5. What will `math.sqrt(25)` return?
   a) 5
   b) 25
   c) 125
   d) Error

---

## **Part 2: True/False**

1. Objects are instances of a class. (True / False)
2. A tuple is mutable in Python. (True / False)
3. `pandas` library can be used to handle tabular data. (True / False)
4. `random.shuffle(list)` randomizes the order of items in a list. (True / False)
5. Methods inside a class can access attributes using `self`. (True / False)

---

## **Part 3: Short Answer / Code Output**

1. What does this code print?

```python
from datetime import datetime
print(datetime.now().year)
```

2. Create a `Person` class with attributes `name` and `age`, and a method `greet()` that prints:

```
Hello, my name is <name> and I am <age> years old.
```

3. What will this print?

```python
import random
numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print(numbers)
```

4. Create a `BankAccount` class with methods `deposit()` and `withdraw()`. Show an example of depositing 500 and withdrawing 200.

5. Using `pandas`, create a DataFrame with columns: Name, Age, City, and add 3 rows of data. Print the DataFrame.

---

## **Part 4: Mini Project / Problem Solving**

1. Write a **function `roll_two_dice()`** that returns the sum of rolling two dice.
2. Create a **text-based quiz game** with 2 questions. Keep score and print the final score.
3. Create a **budget tracker**: store 3 expenses (name and amount) in a list of dictionaries and print total spent.
4. Write a function that **asks for first and last name** and prints the name in **uppercase**.
5. Explain why **OOP is useful** in mini projects.

---

# **Answer Key – Day 3 Quiz**

### **Part 1: MCQs**

1. **b) class**
2. **b) Toyota**
3. **b) **init****
4. **b) random**
5. **a) 5**

---

### **Part 2: True/False**

1. True
2. False
3. True
4. True
5. True

---

### **Part 3: Short Answer / Code Output**

1. Prints the **current year**, e.g., `2025`
2. ```python
   ```

class Person:
def **init**(self, name, age):
self.name = name
self.age = age

```
def greet(self):
    print(f"Hello, my name is {self.name} and I am {self.age} years old.")
```

# Example usage

p = Person("Alice", 25)
p.greet()

````
3. Prints a **shuffled list**, e.g., `[3,1,5,2,4]` (order varies)  
4. ```python
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

# Example usage
account = BankAccount("Bob", 0)
account.deposit(500)
account.withdraw(200)
````

5. ```python
   ```

import pandas as pd

data = {
"Name": ["Alice", "Bob", "Charlie"],
"Age": [25, 30, 22],
"City": ["Paris", "Tokyo", "New York"]
}
df = pd.DataFrame(data)
print(df)

````

---

### **Part 4: Mini Project / Problem Solving**

1. ```python
import random

def roll_two_dice():
    return random.randint(1,6) + random.randint(1,6)

print(roll_two_dice())
````

2. ```python
   ```

questions = [
{"q": "2+2=", "a": "4"},
{"q": "Capital of France?", "a": "Paris"}
]

score = 0
for q in questions:
ans = input(q["q"] + " ")
if ans.strip().lower() == q["a"].lower():
score += 1
print(f"Final score: {score}/{len(questions)}")

````
3. ```python
expenses = [
    {"name":"Groceries","amount":50},
    {"name":"Transport","amount":20},
    {"name":"Entertainment","amount":30}
]

total = sum(item["amount"] for item in expenses)
print(f"Total spent: ${total}")
````

4. ```python
   ```

def print_upper_name():
first = input("First name: ")
last = input("Last name: ")
print(f"{first} {last}".upper())

print_upper_name()

```
5. **OOP is useful** because it makes code **modular, reusable, and easier to manage**, especially in mini projects that combine multiple features like classes, methods, and data structures.  

