# **Python Crash Course 2025 – Trainer Workbook & Code-Along**

---

## **Module 1: Foundations – Pythonic Mental Models**

### **1. Python Execution Pipeline**

```python
# Define a simple function
def add(a, b):
    return a + b

# Execution
result = add(5, 7)
print("Result:", result)

# Trainer Notes:
# 1. Source code is compiled into bytecode (.pyc)
# 2. Python Virtual Machine (PVM) executes the bytecode
# 3. Step-by-step execution demonstrates top-down predictability
```

**Variation Examples:**

```python
# Loops and branching
for i in range(3):
    if i % 2 == 0:
        print(f"{i} is even")
    else:
        print(f"{i} is odd")
```

**Discussion:** Bytecode execution, control flow, and performance insights.

---

### **2. Variables as References (Labels)**

```python
# Immutable binding
x = 100
y = x
print("x:", x, "id:", id(x))
print("y:", y, "id:", id(y))

# Mutable binding
lst1 = [1,2,3]
lst2 = lst1
lst1.append(4)
print("lst1:", lst1)
print("lst2:", lst2)  # Both changed due to shared reference

# Reassignment
lst1 = [9,9,9]
print("lst1:", lst1)
print("lst2:", lst2)
```

**Edge Cases:**

```python
# Integer caching
a = 256
b = 256
print(a is b)  # True, small integers cached
c = 257
d = 257
print(c is d)  # False, new object
```

**Mini-Lab Exercises:**

1. Assign a list to two variables, mutate one, observe the other.
2. Assign an integer > 256 to two variables, compare identities.
3. Explain why small integers are cached.

---

### **3. Mutable vs Immutable Objects**

```python
# Immutable string
s = "hello"
print(s.upper())  # Returns new object
print(s)          # Original unchanged

# Mutable list
lst = [10, 20]
lst.append(30)
print(lst)

# Functions with immutables vs mutables
def mutate_list(l):
    l.append("new")
    return l

def increment_num(n):
    n += 5
    return n

nums = [1,2]
print("Before mutation:", nums)
mutate_list(nums)
print("After mutation:", nums)

num = 10
print("Before increment:", num)
increment_num(num)
print("After increment:", num)
```

**Discussion:** Side effects, immutability, and thread-safety.

---

## **Module 2: Types & Operators**

### **1. Numeric Types and Precision**

```python
# Integers
big_int = 10**50
print("Big integer:", big_int)

# Float precision
print("0.1 + 0.2 =", 0.1 + 0.2)

# Decimal precision
from decimal import Decimal
print(Decimal('0.1') + Decimal('0.2'))

# Operators
print("5 / 2 =", 5 / 2)    # True division
print("5 // 2 =", 5 // 2)  # Floor division
print("5 % 2 =", 5 % 2)    # Modulo
print("2 ** 10 =", 2 ** 10) # Exponentiation
```

**Mini-Lab Exercises:**

1. Calculate factorial using integers.
2. Compare float vs decimal sum of `0.1 + 0.2`.
3. Demonstrate floor division and modulo for a random number.

---

### **2. Strings & Slicing**

```python
text = "Python Crash Course"

# Case
print(text.capitalize())
print(text.title())
print(text.upper())
print(text.lower())

# Slicing
print(text[:6])    # First 6 chars
print(text[::-1])  # Reverse string
print(text[::2])   # Every 2nd character

# F-Strings
name, age = "Alice", 30
print(f"My name is {name} and I am {age} years old")
```

**Exercise:**

* Reverse a user-input string
* Slice out every third character
* Format multiple variables in a sentence using f-strings

---

### **3. Booleans & Truthiness**

```python
values = [0, "", [], {}, set(), None, "Hello", [1,2]]
for v in values:
    print(v, "->", bool(v))

# Conditional checks
users = []
if users:
    print("Users exist")
else:
    print("No users")
```

**Discussion:** Falsy vs Truthy, idiomatic Python conditionals.

---

## **Module 3: Collections & Comprehensions**

### **1. Lists, Tuples, Sets, Dictionaries**

```python
# List
lst = [1, 2, 3]
lst.append(4)
print("List:", lst)

# Tuple
tup = (10, 20, 30)
print("Tuple:", tup)

# Set
s = {1, 2, 2, 3}
s.add(4)
print("Set:", s)

# Dictionary
d = {"name":"Alice", "role":"admin"}
print("Dict:", d)
```

**Mini-Lab:** Create examples demonstrating order (lists vs sets), immutability (tuples), and fast lookup (dict).

---

### **2. Safe Dictionary Access**

```python
user = {"name": "Bob"}

# Safe access
role = user.get("role", "viewer")
profile = user.get("profile", {})
age = profile.get("age", 0)
print(role, age)
```

**Exercise:** Access nested dictionary safely with missing keys.

---

### **3. Comprehensions**

```python
# List comprehension
squares = [x**2 for x in range(1,6)]
evens = [x for x in range(1,11) if x%2==0]

# Dictionary comprehension
words = ["apple","banana","cherry"]
lengths = {w: len(w) for w in words}

# Tuple via generator
tuple_squares = tuple(x**2 for x in range(5))

# Nested comprehension
matrix = [[i*j for j in range(1,4)] for i in range(1,4)]

# Flatten nested list
nested = [[1,2],[3,4]]
flat = [item for sublist in nested for item in sublist]
```

**Mini-Lab Exercises:**

* Filter vowels from a string using comprehension
* Flatten a 3-level nested list
* Create a dict mapping numbers to their squares if even

---

## **Module 4: Robust Python Practices**

### **1. Input Validation & EAFP**

```python
try:
    age = int(input("Enter age: "))
except ValueError:
    print("Please enter a valid number")

# EAFP example
my_dict = {"a":1}
try:
    val = my_dict["b"]
except KeyError:
    val = 0
print("Value:", val)
```

**Exercise:** Write a function to safely access deeply nested dictionary keys.

---

### **2. Type Hinting**

```python
def multiply(a:int, b:int)->int:
    return a*b

print(multiply(5,7))
```

**Mini-Lab:** Add type hints to 3 user-defined functions and validate with mypy.

---

## **Module 5: Advanced Pythonic Patterns**

### **1. Unpacking Operators**

```python
numbers = [1,2,3,4,5]
a,*b,c = numbers
print(a,b,c)

# Merge lists
list1 = [1,2]
list2 = [3,4]
merged = [*list1, *list2]
print(merged)
```

---

### **2. Iteration Techniques**

```python
fruits = ["apple","banana"]
for idx, fruit in enumerate(fruits):
    print(idx, fruit)

person = {"name":"Alice","age":30}
for k,v in person.items():
    print(k,v)
```

---

### **3. Mutable vs Immutable Behavior in Functions**

```python
def add_item(lst):
    lst.append("x")
    return lst

my_list = [1,2]
add_item(my_list)
print(my_list)  # Shows mutation

def increment(n):
    n += 5
    return n

num = 10
increment(num)
print(num)  # Immutable, original unchanged
```

---

### **Mini-Lab Exercises for Module 5**

1. Flatten a nested list using a comprehension
2. Merge multiple dictionaries, resolving conflicts
3. Demonstrate mutation vs immutability in functions

**Expected Outputs:**

* Flattened list
* Merged dictionary
* Immutable objects remain unchanged after function calls

---

### ✅ **Trainer Notes Summary**

* Encourage **prediction before running code**
* Discuss **mental models for each section**
* Include **interactive challenges and variations**
* Highlight **common pitfalls** (shared references, float precision, KeyError)
* Include **edge cases** for advanced learners

