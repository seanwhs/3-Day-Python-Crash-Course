# 🐍 Weekend Python Crash Course – Pre-Course Assessment

**Total Duration:** 45–60 minutes
**Instructions:** Answer all questions. For coding tasks, write working Python code. This is not graded strictly; it’s for understanding prior knowledge.

---

## **Part 1: Multiple Choice Questions (MCQs)**

1. Which of the following is the **correct way to define a class** in Python?
   a) `class Person:`
   b) `class Person():`
   c) `def Person():`
   d) Both a and b

2. What will `type(3.14)` return?
   a) `int`
   b) `float`
   c) `str`
   d) `bool`

3. Which of the following **Python libraries** is used to generate random numbers?
   a) `datetime`
   b) `random`
   c) `math`
   d) `os`

4. What does `len([1,2,3,4])` return?
   a) 3
   b) 4
   c) 5
   d) Error

5. Which statement is **true about tuples**?
   a) Tuples are mutable
   b) Tuples are immutable
   c) Tuples cannot store multiple data types
   d) Tuples are slower than lists

---

## **Part 2: True/False**

1. You can call a function before defining it in Python. (True / False)
2. Lists can contain other lists as elements. (True / False)
3. Python allows multiple inheritance in classes. (True / False)
4. The `math` library must be installed using pip before using it. (True / False)
5. The `input()` function always returns a string. (True / False)

---

## **Part 3: Short Answer / Code Output**

1. What is printed by this code?

```python
x = 5
y = 2
print(x ** y)
```

2. Write Python code to create a list of 5 numbers and **print the largest number** using a built-in function.

3. Create a **simple class `Person`** with attributes `name` and `age`. Create one object and print its name.

4. Write Python code to **get the current year** using the `datetime` module.

5. What is the output of this code?

```python
numbers = [1, 2, 3, 4, 5]
print(numbers[1:4])
```

---

## **Part 4: Mini Problem / Conceptual**

1. Explain in 1–2 sentences what a **class** and an **object** are in Python.

2. Write Python code to **simulate a dice roll** (1–6) using the `random` library.

3. Create a dictionary with **3 contacts** (name → phone number) and print all the names.

4. Explain why **functions** are useful in Python programs.

5. List **two benefits of using Python libraries**.

---

## **Answer Key – Pre-Course Assessment**

### **Part 1: MCQs**

1. **d) Both a and b**
2. **b) float**
3. **b) random**
4. **b) 4**
5. **b) Tuples are immutable**

---

### **Part 2: True/False**

1. False
2. True
3. True
4. False
5. True

---

### **Part 3: Short Answer / Code Output**

1. `25`
2. ```python
   ```

numbers = [5, 3, 8, 1, 4]
print(max(numbers))

````
3. ```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p = Person("Alice", 25)
print(p.name)
````

4. ```python
   ```

from datetime import datetime
print(datetime.now().year)

````
5. `[2, 3, 4]`  

---

### **Part 4: Mini Problem / Conceptual**

1. **Class**: a blueprint for creating objects; **Object**: an instance of a class with attributes and methods.  

2. ```python
import random
dice = random.randint(1,6)
print(dice)
````

3. ```python
   ```

contacts = {"Alice":"123", "Bob":"456", "Charlie":"789"}
print(list(contacts.keys()))

```

4. Functions allow **code reuse, modularity, and easier maintenance**.  

5. Benefits of libraries:  
   - Save time by providing **pre-built functions**  
   - Enable handling **complex tasks** (like data manipulation, math operations) easily  

