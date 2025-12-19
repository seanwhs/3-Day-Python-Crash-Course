# **Python Crash Course 2025 – Trainer Workbook**

---

## **Module 1: Foundations — Variables, References & Execution**

### **Challenge 1.1 – Variable Binding & Identity**

```python
x = [1, 2, 3]
y = x
z = x.copy()
x.append(4)
print("x:", x, "y:", y, "z:", z)
```

**Trainer Notes:**

* **Line 1:** `x` points to a list `[1,2,3]`.
* **Line 2:** `y = x` → `y` now references the **same list**. Changes to `x` affect `y`.
* **Line 3:** `z = x.copy()` → shallow copy. `z` references a **new list** with same contents.
* **Line 4:** `x.append(4)` → modifies original list.
* **Print:** Shows that `x` and `y` are updated, `z` remains `[1,2,3]`.

**Hint:** Ask students to predict `id(x), id(y), id(z)`.

**Common Pitfall:** Thinking `.copy()` is a deep copy.

---

### **Challenge 1.2 – Mutable vs Immutable**

```python
a = (1, 2, 3)
# a[0] = 10  # ❌ TypeError
a = (10, 2, 3)  # ✅ Reassignment works
```

**Trainer Notes:**

* **Tuples are immutable** → cannot change elements.
* Reassignment creates a **new tuple object**.
* **Tip:** Use tuples for fixed collections, lists for mutable collections.

**Hint:** Have students try `id(a)` before and after reassignment to see it changes.

---

### **Challenge 1.3 – Identity vs Equality**

```python
x = [1, 2, 3]
y = [1, 2, 3]
print(x == y)  # True
print(x is y)  # False
```

**Trainer Notes:**

* `==` compares **values**
* `is` compares **object identity (memory address)**
* **Hint:** Use `id(x)` and `id(y)` to show different addresses.

---

### **Challenge 1.4 – Object Copying**

```python
import copy
nested = [[1, 2], [3, 4]]
shallow = nested.copy()
deep = copy.deepcopy(nested)
nested[0].append(3)
print("Shallow:", shallow)
print("Deep:", deep)
```

**Trainer Notes:**

* Shallow copy copies **outer object** only, inner lists are **shared references**.
* Deep copy copies **everything recursively** → safe from nested mutations.

**Pro Tip:** Use deep copies for nested dicts/lists when building prototypes.

---

### **Challenge 1.5 – Execution Pipeline**

```python
def foo():
    return sum(range(10))
print(foo())
```

**Trainer Notes:**

* Python compiles functions to **bytecode** before execution.
* PVM executes **step-by-step**.
* **Hint:** Use `import dis; dis.dis(foo)` to view instructions.

**Extension:** Ask students to time `sum(range(10))` vs manual loop.

---

## **Module 2: Numbers, Operators & Precision**

### **Challenge 2.1 – Float Precision**

```python
print(0.1 + 0.2 == 0.3)  # False
from decimal import Decimal
print(Decimal('0.1') + Decimal('0.2') == Decimal('0.3'))  # True
```

**Trainer Notes:**

* Floating-point numbers are stored in binary → rounding errors.
* `Decimal` ensures **exact decimal arithmetic**.

**Hint:** Print `0.1 + 0.2` to show `0.30000000000000004`.

---

### **Challenge 2.2 – Arithmetic Operators**

```python
a, b = 7, 3
print(a/b, a//b, a%b, a**b)
```

**Trainer Notes:**

* `/` → true division → float
* `//` → floor division → integer division
* `%` → remainder
* `**` → exponentiation

**Hint:** Try negative numbers and see floor division behavior.

---

### **Challenge 2.3 – Operator Precedence**

```python
result = 2 + 3 * 4 ** 2 / 2
print(result)
```

**Trainer Notes:**

* Precedence: `**` > `*`/`/` > `+`
* Teach students to **always parenthesize** complex expressions.

---

### **Challenge 2.4 – Complex Numbers**

```python
c = 3 + 4j
print("Real:", c.real)
print("Imag:", c.imag)
print("Magnitude:", abs(c))
```

**Trainer Notes:**

* `.real` and `.imag` return float parts
* `abs(c)` → magnitude (Pythagoras theorem)

**Bonus:** Multiply complex numbers and verify results.

---

### **Challenge 2.5 – Type Conversion**

```python
x = "100"
y = 5
print(int(x) + y)
```

**Trainer Notes:**

* Strings → int conversion required before arithmetic.
* Explore `float()`, `str()`, `bool()` conversions.

---

## **Module 3: Strings & Text**

### **Challenge 3.1 – Slicing & Steps**

```python
text = "Python"
print(text[1:4])    # 'yth'
print(text[::-1])   # 'nohtyP'
print(text[::2])    # 'Pto'
```

**Trainer Notes:**

* Slicing: `[start:end:step]`
* Negative indices: count from **end**
* Step can reverse string: `[::-1]`

**Hint:** Ask students to slice every third character from a long string.

---

### **Challenge 3.2 – Case Manipulation**

```python
s = "hello world"
print(s.upper(), s.capitalize(), s.title())
```

* `.upper()` → all uppercase
* `.capitalize()` → first letter uppercase
* `.title()` → first letter of each word uppercase
* Bonus: `.swapcase()`, `.casefold()` for case-insensitive comparison

---

### **Challenge 3.3 – F-Strings**

```python
name = "Alice"
age = 30
print(f"Name: {name}, Age: {age}")
```

**Trainer Notes:**

* Expressions can be evaluated inside f-strings: `{age+5}`, `{name.upper()}`
* Cleaner and faster than concatenation.

---

### **Challenge 3.4 – Multi-line Strings & Raw Strings**

```python
print("""Line 1
Line 2
Line 3""")

path = r"C:\Users\Sean\Desktop"
print(path)
```

**Trainer Notes:**

* `r""` prevents escape sequences from being interpreted
* Multi-line strings are useful for docstrings and formatted output

---

### **Challenge 3.5 – String Methods**

```python
s = "   Python  "
print(s.strip(), s.startswith("Py"), s.endswith("on"), s.find("th"))
```

**Trainer Notes:**

* `.strip()` removes spaces
* `.startswith()` / `.endswith()` → check prefix/suffix
* `.find()` returns first occurrence index, -1 if not found

---

## **Module 4: Booleans, Truthiness & Control Flow**

---

### **Challenge 4.1 – Truthiness Deep Dive**

```python
values = [None, 0, 0.0, "", [], {}, set(), "0", [0]]
for v in values:
    print(v, "→", bool(v))
```

### **Trainer Explanation**

Python does **not** require explicit booleans.

Falsy values:

* `None`
* `0`, `0.0`
* Empty sequences & collections

Truthy values:

* Any **non-empty** object
* Any **non-zero** number

**Critical Mental Model:**

> Python asks: *“Is this empty or zero?”*

---

### **Common Mistake**

```python
if x == True:   # ❌ Bad
```

Instead:

```python
if x:           # ✅ Pythonic
```

---

### **Extension**

Ask students:

```python
class Box:
    pass

b = Box()
print(bool(b))
```

→ Objects are **truthy by default** unless `__bool__` or `__len__` is defined.

---

### **Challenge 4.2 – Conditional Expressions (Ternary)**

```python
x = 15
result = "Even" if x % 2 == 0 else "Odd"
print(result)
```

### **Trainer Notes**

* One-line decision
* Expression, not a statement
* Encourages concise logic

---

### **Extension**

Rewrite this block:

```python
if score >= 50:
    grade = "Pass"
else:
    grade = "Fail"
```

---

### **Challenge 4.3 – Logical Operators & Short-Circuiting**

```python
def side_effect():
    print("Function called")
    return True

print(False and side_effect())
print(True or side_effect())
```

### **Trainer Explanation**

* `and` stops at first `False`
* `or` stops at first `True`

**Why it matters:**
Used heavily in **guards**, **defaults**, and **lazy evaluation**.

---

### **Real-world Pattern**

```python
user = None
name = user and user.username
```

---

## **Module 5: Collections Engineering**

---

### **Challenge 5.1 – List vs Tuple Behavior**

```python
lst = [1, 2, 3]
tpl = (1, 2, 3)

lst.append(4)
# tpl.append(4)  # ❌ AttributeError
print(lst, tpl)
```

### **Trainer Notes**

* Lists: dynamic, mutable
* Tuples: fixed, immutable
* Tuples are **hashable** → usable as dict keys

---

### **Challenge 5.2 – Set Behavior & Deduplication**

```python
nums = [1, 2, 2, 3, 4, 4]
unique = set(nums)
print(unique)
```

### **Trainer Explanation**

* Sets remove duplicates
* Order is **not guaranteed**
* Membership testing is O(1)

---

### **Extension**

```python
emails = ["a@x.com", "b@x.com", "a@x.com"]
```

How would you deduplicate?

---

### **Challenge 5.3 – Dictionary Mutation & Access**

```python
user = {"name": "Alice", "age": 30}
user["role"] = "admin"
print(user)
```

---

### **Challenge 5.4 – Safe Dictionary Access**

```python
user = {"name": "Alice"}
print(user.get("role", "viewer"))
```

### **Trainer Explanation**

* `.get()` avoids `KeyError`
* Default values make code **robust**

---

### **Challenge 5.5 – Nested Safe Access**

```python
data = {"user": {"profile": {}}}
age = data.get("user", {}).get("profile", {}).get("age", 0)
print(age)
```

### **Trainer Notes**

* Defensive programming
* Avoids crashes from missing keys

---

### **Extension**

Introduce `collections.defaultdict` later.

---

### **Challenge 5.6 – List Comprehension (Filter + Transform)**

```python
squares = [x**2 for x in range(10) if x % 2 == 0]
print(squares)
```

### **Trainer Explanation**

Equivalent to:

```python
squares = []
for x in range(10):
    if x % 2 == 0:
        squares.append(x**2)
```

Comprehensions:

* Shorter
* Faster
* More expressive

---

### **Challenge 5.7 – Dict Comprehension**

```python
words = ["apple", "banana", "pear"]
lengths = {w: len(w) for w in words}
print(lengths)
```

---

### **Challenge 5.8 – Flattening Nested Lists**

```python
nested = [[1, 2], [3, 4], [5]]
flat = [x for row in nested for x in row]
print(flat)
```

### **Trainer Tip**

Order matters:

```python
for row in nested:
    for x in row:
        ...
```

---

## **Module 6: Functions, Errors & EAFP**

---

### **Challenge 6.1 – Safe Division (EAFP)**

```python
def safe_div(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return None
```

### **Trainer Explanation**

* EAFP = *Try first, handle failure*
* Cleaner than pre-checking `if b != 0`

---

### **Challenge 6.2 – Input Validation**

```python
try:
    age = int(input("Enter age: "))
except ValueError:
    print("Invalid number")
```

### **Trainer Notes**

* `input()` always returns `str`
* Always validate external input

---

### **Challenge 6.3 – Default Parameters**

```python
def greet(name="Guest"):
    print(f"Hello, {name}")
```

### **Trainer Warning**

Avoid mutable defaults:

```python
def bad(x=[]):  # ❌
```

---

### **Challenge 6.4 – *args (Variadic Arguments)**

```python
def add(*args):
    return sum(args)

print(add(1, 2, 3, 4))
```

### **Trainer Explanation**

* `args` is a tuple
* Used for flexible APIs

---

### **Challenge 6.5 – **kwargs**

```python
def user_info(**kwargs):
    for k, v in kwargs.items():
        print(k, v)

user_info(name="Alice", role="admin")
```

---

## **Module 7: Advanced Pythonic Patterns**

---

### **Challenge 7.1 – Unpacking Operators**

```python
nums = [1, 2, 3, 4, 5]
a, *b, c = nums
print(a, b, c)
```

### **Trainer Explanation**

* `*b` captures the “middle”
* Used heavily in parsing data

---

### **Challenge 7.2 – Merging Collections**

```python
l1 = [1, 2, 3]
l2 = [3, 4, 5]
merged = [*l1, *l2]
print(merged)
```

---

### **Challenge 7.3 – Deduplication Pattern**

```python
unique = list(set(l1 + l2))
```

⚠️ Order not preserved.

---

### **Challenge 7.4 – Enumerate**

```python
fruits = ["apple", "banana"]
for i, fruit in enumerate(fruits, start=1):
    print(i, fruit)
```

---

### **Challenge 7.5 – Palindrome Check**

```python
s = "racecar"
print(s == s[::-1])
```

---

### **Challenge 7.6 – FizzBuzz (Pythonic)**

```python
for i in range(1, 21):
    print("Fizz"*(i%3==0) + "Buzz"*(i%5==0) or i)
```

### **Trainer Explanation**

* Boolean arithmetic
* Empty string is falsy → fallback to `i`

---

### **Challenge 7.7 – Sorting Dict by Value**

```python
scores = {"Alice": 90, "Bob": 75, "Charlie": 85}
sorted_scores = dict(
    sorted(scores.items(), key=lambda item: item[1], reverse=True)
)
print(sorted_scores)
```

---

### **Challenge 7.8 – Generator Expressions**

```python
squares = (x**2 for x in range(5))
print(list(squares))
```

### **Trainer Notes**

* Lazy evaluation
* Memory efficient

---

### **Challenge 7.9 – Context Managers**

```python
with open("test.txt", "w") as f:
    f.write("Hello")
```

### **Trainer Explanation**

* File auto-closed
* Prevents resource leaks
* `with` works with DB connections, locks, files

---

## **Trainer Wrap-Up: Mental Models Reinforced**

✅ Variables are **labels**, not boxes
✅ Mutability explains “mystery bugs”
✅ Truthiness simplifies control flow
✅ Comprehensions beat loops for clarity
✅ EAFP beats defensive if-checks
✅ Python rewards **expressive, readable code**

---


Do you want me to generate **Part 2 next**?
