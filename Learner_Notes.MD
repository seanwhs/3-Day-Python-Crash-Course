# 🐍 Python Crash Course — Learner Notes 

> **Tone:** Fast-paced, practical, code-first
> **Audience:** Bootcamp learners, career switchers, junior engineers
> **Outcome:** Learners can read, write, debug, and reason about Python code confidently

---

## 🧭 Bootcamp Philosophy

This is **not** a theory-heavy course.

Rules:

* You **code along** — always
* You are expected to **break code and debug it**
* Google, docs, StackOverflow, and AI tools are **allowed**
* Understanding *why* matters more than memorizing syntax

> 💡 *If your code doesn’t break at least once a day, you’re not learning fast enough.*

---

# 🟢 PART 1 — BASIC PYTHON (FOUNDATIONS)

---

## 1️⃣ Variables & Data Types

### What is a Variable?

A variable is a **label pointing to a value in memory**.

Python is **dynamically typed**:

* You don’t declare types
* Python infers them at runtime

```python
x = 10        # int
x = "ten"     # str (same variable, new type)
```

### Core Built-in Types

| Type  | Example | Use Case             |
| ----- | ------- | -------------------- |
| int   | 42      | counters, IDs        |
| float | 3.14    | prices, measurements |
| str   | "hello" | text, messages       |
| bool  | True    | flags, conditions    |

```python
price = 19.99
is_logged_in = False
```

### Mutable vs Immutable (VERY IMPORTANT)

* **Immutable:** int, float, str, tuple
* **Mutable:** list, dict, set

```python
x = 5
y = x
y += 1
# x is still 5
```

```python
lst1 = [1, 2]
lst2 = lst1
lst2.append(3)
# lst1 is now [1, 2, 3]
```

🧠 **Bootcamp Insight:**
Most beginner bugs come from misunderstanding mutability.

---

## 2️⃣ Control Flow (Decision Making)

Programs are just **decisions + repetition**.

### If / Elif / Else

```python
if score >= 80:
    grade = "A"
elif score >= 60:
    grade = "B"
else:
    grade = "C"
```

### Real-World Case: Loan Approval

```python
if income > 5000 and credit_score > 700:
    approved = True
else:
    approved = False
```

> 🧠 Translate English → logic → code

---

## 3️⃣ Loops (Repetition)

### for Loop

```python
for i in range(5):
    print(i)
```

### while Loop

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Loop Control

```python
for i in range(10):
    if i == 5:
        break
```

---

## 4️⃣ Functions (Stop Copy-Pasting)

### Why Functions Matter

* Reuse code
* Reduce bugs
* Improve readability

```python
def add(a, b):
    return a + b
```

### Default Arguments

```python
def greet(name="Guest"):
    print(f"Hello {name}")
```

🧠 **Bootcamp Rule:**
If you copy-paste code twice → make a function.

---

# 🟡 PART 2 — INTERMEDIATE PYTHON (STRUCTURE)

---

## 5️⃣ Object-Oriented Programming (OOP)

### Mental Model

Objects = **data + behavior**

```python
class User:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print(f"Hi, I am {self.name}")
```

```python
u = User("Alice")
u.greet()
```

### Case Study: Backend Systems

* Django models
* API resources
* Domain entities

OOP lets your code **scale beyond scripts**.

---

## 6️⃣ Inheritance (Reuse Carefully)

```python
class Employee:
    def get_role(self):
        return "Employee"

class Manager(Employee):
    def get_role(self):
        return "Manager"
```

🧠 **Engineering Advice:**
Prefer composition over deep inheritance.

---

## 7️⃣ Modules & Packages

```python
import math
math.sqrt(16)
```

### Project Structure

```
project/
 ├── main.py
 ├── utils/
 │   ├── helpers.py
```

```python
from utils.helpers import format_date
```

---

## 8️⃣ File I/O (Real-World Essential)

### Reading Files

```python
with open("data.txt") as f:
    for line in f:
        print(line)
```

### Writing Files

```python
with open("out.txt", "w") as f:
    f.write("Hello")
```

### Case Study

Processing logs, CSVs, reports, exports.

---

# 🔴 PART 3 — ADVANCED PYTHON (ENGINEERING)

---

## 9️⃣ Decorators (Power Tool)

Decorators **wrap functions** to add behavior.

```python
def logger(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper
```

```python
@logger
def run():
    print("Running")
```

### Real Uses

* Authentication
* Logging
* Timing
* Caching

---

## 🔟 Generators (Memory Efficiency)

```python
def read_lines(file):
    with open(file) as f:
        for line in f:
            yield line
```

🧠 Used for:

* Large files
* Streams
* Data pipelines

---

## 1️⃣1️⃣ Async & Concurrency

### Concurrency Models

| Model           | Use Case         |
| --------------- | ---------------- |
| threading       | I/O bound        |
| multiprocessing | CPU bound        |
| asyncio         | High concurrency |

```python
import asyncio

async def task():
    await asyncio.sleep(1)
    print("done")

asyncio.run(task())
```

### Case Study

Calling 100 APIs concurrently.

---

# 🎯 FINAL BOOTCAMP OUTCOME

By the end of this bootcamp, learners can:

✅ Read Python code confidently
✅ Write structured, clean Python
✅ Debug errors logically
✅ Understand backend frameworks like Django

