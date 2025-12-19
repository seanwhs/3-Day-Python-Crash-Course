# 📘 **Python Crash Course 2025 – Advanced Challenge Workbook**

## **Module 1: Foundations — Memory, References & Execution**

### **Challenge 1.1 – Variable Binding & Identity**

```python
x = [1, 2, 3]
y = x
z = x.copy()
x.append(4)
print(f"ID x: {id(x)}, ID y: {id(y)}, ID z: {id(z)}")
print(x, y, z)

```

**Engineering Deep Dive:** Python variables are labels. `y = x` binds the label `y` to the exact same memory address as `x`. `z = x.copy()` creates a new object (shallow copy).

---

### **Challenge 1.2 – The Mutable Default Argument Trap**

*New Challenge: Identify why this code is dangerous.*

```python
def add_item(item, basket=[]):
    basket.append(item)
    return basket

print(add_item("Apple"))  # ['Apple']
print(add_item("Banana")) # Expected ['Banana'], actual ['Apple', 'Banana']

```

**Solution:** Default arguments are evaluated **once** at function definition time, not at call time. The list `basket` persists across calls. **Fix:** Use `basket=None` and initialize inside the function.

---

### **Challenge 1.3 – Small Integer Interning**

```python
a = 256
b = 256
print(a is b) # True

c = 257
d = 257
print(c is d) # False (usually)

```

**Explanation:** For performance, Python interns (caches) integers from `-5` to `256`. Beyond that, new objects are created in memory, so `is` (identity check) fails even if `==` (value check) passes.

---

## **Module 2: Numbers, Operators & Precision**

### **Challenge 2.1 – IEEE 754 & Financial Integrity**

```python
# The Floating Point Error
print(0.1 + 0.2 == 0.3) # False

from decimal import Decimal, getcontext
getcontext().prec = 4 # Set precision
val = Decimal('0.1000') + Decimal('0.2000')
print(val == Decimal('0.3000')) # True

```

**Statistics:** Standard floats (binary) cannot represent  exactly. In financial systems, using `float` instead of `Decimal` can lead to errors of  or more per transaction, which aggregates to significant capital loss in high-volume trading.

---

### **Challenge 2.2 – Floor Division vs. Truncation**

```python
print(-7 // 3)  # -3
print(int(-7 / 3)) # -2

```

**Explanation:** `//` is **floor division** (rounds toward negative infinity). `int()` casting performs **truncation** (rounds toward zero).

---

## **Module 3: Strings & Text Engineering**

### **Challenge 3.1 – String Interning & Memory**

```python
s1 = "python_is_fast"
s2 = "python_is_fast"
print(s1 is s2) # True (Interned by compiler)

s3 = "".join(["py", "thon"])
s4 = "python"
print(s3 is s4) # False (Created at runtime)

```

### **Challenge 3.2 – Advanced Slicing & Step**

```python
data = "123456789"
# Extract even numbers in reverse
print(data[7::-2]) # "8642"

```

---

## **Module 4: Booleans & Truthiness**

### **Challenge 4.1 – The `or` Operator for Defaults**

```python
user_input = ""
display_name = user_input or "Anonymous"
print(display_name) # "Anonymous"

```

**Explanation:** Python's `or` returns the first "Truthy" value it encounters. This is a common pattern for setting fallbacks.

### **Challenge 4.2 – Short-circuit Safety**

```python
def is_valid(val):
    return val > 0

data = None
# This prevents an AttributeError/TypeError
if data is not None and is_valid(data):
    print("Valid")

```

---

## **Module 5: Collection Engineering**

### **Challenge 5.1 – Big-O Complexity: List vs. Set**

```python
import time
large_list = list(range(10_000_000))
large_set = set(large_list)

# Search speed comparison
start = time.time()
9_999_999 in large_list # O(n) - Linear search
print(f"List time: {time.time() - start}")

start = time.time()
9_999_999 in large_set # O(1) - Hash lookup
print(f"Set time: {time.time() - start}")

```

**Statistics:** For 10 million elements, a `set` lookup is approximately **100,000x faster** than a `list` lookup because it uses a hash table.

---

## **Module 6: Functions, Scoping & EAFP**

### **Challenge 6.1 – LEGB Scoping Mystery**

```python
x = 10
def outer():
    x = 20
    def inner():
        nonlocal x
        x += 5
        print(f"Inner: {x}")
    inner()
    print(f"Outer: {x}")

outer()
print(f"Global: {x}")

```

**Solution:** Inner: 25, Outer: 25, Global: 10. `nonlocal` modifies the enclosing scope, while `global` would modify the top-level scope.

---

### **Challenge 6.2 – EAFP for File I/O**

```python
# LBYL (Look Before You Leap) - Prone to race conditions
import os
if os.path.exists("data.txt"):
    with open("data.txt") as f:
        pass

# EAFP (Easier to Ask Forgiveness than Permission) - Atomic and Pythonic
try:
    with open("data.txt") as f:
        pass
except FileNotFoundError:
    print("File not found.")

```

---

## **Module 7: Advanced Pythonic Patterns**

### **Challenge 7.1 – Generator Memory Efficiency**

```python
import sys
# List comprehension (Loads everything into RAM)
list_comp = [x**2 for x in range(10_000)]
# Generator expression (Lazy evaluation)
gen_exp = (x**2 for x in range(10_000))

print(f"List Size: {sys.getsizeof(list_comp)} bytes")
print(f"Gen Size: {sys.getsizeof(gen_exp)} bytes")

```

**Engineering Note:** A generator always occupies about **112 bytes** regardless of the range size, making it the only viable choice for processing infinite streams or multi-gigabyte log files.

### **Challenge 7.2 – Dictionary Merging (Python 3.9+)**

```python
base_config = {"host": "localhost", "port": 8080}
user_config = {"port": 9000, "debug": True}

# The Merge Operator
merged = base_config | user_config 
print(merged) # {'host': 'localhost', 'port': 9000, 'debug': True}

```

### **Challenge 7.3 – The `__missing__` Pattern**

```python
class MyDict(dict):
    def __missing__(self, key):
        return "Key not found!"

d = MyDict(a=1)
print(d['b']) # "Key not found!"

```

### **Challenge 7.4 – Decorators (Introduction)**

```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        print(f"Execution time: {time.time() - start}s")
        return result
    return wrapper

@timer
def heavy_task():
    time.sleep(1)

heavy_task()

```
