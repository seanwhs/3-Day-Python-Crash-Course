# **Python Crash Course 2025 – Challenge Workbook**

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

**Solution/Explanation:**

* `x` and `y` point to the **same object** → both reflect changes.
* `z` is a **shallow copy** → independent of original list.

**Bonus:** Try `z = list(x)` or `z = x[:]` and observe results.

---

### **Challenge 1.2 – Mutable vs Immutable**

```python
a = (1, 2, 3)
# Uncomment to test: a[0] = 10  # ❌ TypeError
a = (10, 2, 3)  # ✅ Reassignment works
```

* Tuples are **immutable**, lists are **mutable**.
* Test `id(a)` before and after reassignment to observe object identity change.

---

### **Challenge 1.3 – Identity vs Equality**

```python
x = [1, 2, 3]
y = [1, 2, 3]
print("Equal?", x == y)  # True
print("Same object?", x is y)  # False
```

**Extension:** Use `copy.deepcopy()` and check identity of nested lists.

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

* **Shallow copies**: nested objects are shared.
* **Deep copies**: fully independent.

**Pro Tip:** Deep copy for nested structures when mutation must not affect original.

---

### **Challenge 1.5 – Execution Pipeline**

```python
def foo():
    return sum(range(10))
print(foo())
```

* Python compiles `foo()` to **bytecode** before execution by **PVM**.
* Try using `import dis; dis.dis(foo)` to view the bytecode.

---

## **Module 2: Numbers, Operators & Precision**

### **Challenge 2.1 – Float Precision**

```python
print(0.1 + 0.2 == 0.3)  # False
from decimal import Decimal
print(Decimal('0.1') + Decimal('0.2') == Decimal('0.3'))  # True
```

**Bonus:** Explore `round(0.1+0.2, 10)` and floating-point quirks.

---

### **Challenge 2.2 – Arithmetic Operators**

```python
a, b = 7, 3
print("a/b:", a/b)
print("a//b:", a//b)
print("a%b:", a%b)
print("a**b:", a**b)
```

* Experiment with negative numbers and floor division.

---

### **Challenge 2.3 – Operator Precedence**

```python
result = 2 + 3 * 4 ** 2 / 2
print(result)  # Check order of operations
```

**Tip:** Use parentheses to change order: `(2+3)*(4**2)/2`

---

### **Challenge 2.4 – Complex Numbers**

```python
c = 3 + 4j
print("Real:", c.real)
print("Imag:", c.imag)
print("Magnitude:", abs(c))
```

**Pro Tip:** Useful for scientific computations.

---

### **Challenge 2.5 – Type Conversion**

```python
x = "100"
y = 5
print(int(x) + y)  # 105
```

* Also explore `float()`, `str()`, `bool()`, and `complex()` conversions.

---

## **Module 3: Strings & Text**

### **Challenge 3.1 – Slicing & Steps**

```python
text = "Python"
print(text[1:4])    # 'yth'
print(text[::-1])   # 'nohtyP'
print(text[::2])    # 'Pto'
```

**Bonus:** Slice strings with negative start and end indices.

---

### **Challenge 3.2 – Case Manipulation**

```python
s = "hello world"
print(s.upper(), s.capitalize(), s.title())
```

* Try `s.lower()`, `s.swapcase()`, and `s.casefold()`.

---

### **Challenge 3.3 – F-Strings**

```python
name = "Alice"
age = 30
print(f"Name: {name}, Age: {age}")
```

**Extension:** Use expressions inside f-strings: `{age+5}` or `{name.upper()}`

---

### **Challenge 3.4 – Multi-line Strings & Raw Strings**

```python
print("""Line 1
Line 2
Line 3""")

path = r"C:\Users\Sean\Desktop"
print(path)
```

---

### **Challenge 3.5 – String Methods**

```python
s = "   Python  "
print(s.strip(), s.startswith("Py"), s.endswith("on"), s.find("th"))
```

---

## **Module 4: Booleans & Truthiness**

### **Challenge 4.1 – Truthiness in Collections**

```python
values = [None, 0, "", [], {}, set(), "Hello"]
for v in values:
    print(v, "is", bool(v))
```

---

### **Challenge 4.2 – Conditional Expressions**

```python
x = 10
result = "Even" if x % 2 == 0 else "Odd"
print(result)
```

**Extension:** Nest ternary operators for more complex conditions.

---

### **Challenge 4.3 – Logical Operators & Short-circuiting**

```python
a, b = True, False
print(a and b, a or b, not a)

def side_effect():
    print("Called")
    return True

x = False and side_effect()  # side_effect not called
```

---

### **Challenge 4.4 – Membership Testing**

```python
fruits = ["apple", "banana"]
print("apple" in fruits, "orange" not in fruits)
```

---

## **Module 5: Collections**

### **Challenge 5.1 – Lists & Tuples**

```python
lst = [1, 2, 3]
tpl = (4, 5, 6)
lst.append(4)
print(lst, tpl)
```

* Try unpacking: `a, *b, c = lst`

---

### **Challenge 5.2 – Sets & Deduplication**

```python
s = {1, 2, 2, 3}
s.add(4)
print(s)
```

**Bonus:** `set([1,2,2,3,3,4])` → automatic deduplication.

---

### **Challenge 5.3 – Dictionaries & Safe Access**

```python
d = {"a": 1, "b": 2}
d["c"] = 3
print(d)
role = d.get("role", "viewer")
print("Role:", role)
```

---

### **Challenge 5.4 – Nested Dictionaries**

```python
profile = {"user": {"name":"Alice"}}
age = profile.get("user", {}).get("age", 0)
print(age)
```

---

### **Challenge 5.5 – Comprehensions**

```python
words = ["apple","banana","cherry"]
lengths = {w:len(w) for w in words}
evens = [x**2 for x in range(1,11) if x%2==0]
matrix = [[i*j for j in range(1,4)] for i in range(1,4)]
flat = [x for sub in matrix for x in sub]
```

**Bonus:** Try `{i:i**2 for i in range(5) if i%2==1}`

---

## **Module 6: Functions & EAFP**

### **Challenge 6.1 – Safe Division**

```python
def safe_div(a,b):
    try:
        return a/b
    except ZeroDivisionError:
        return None

print(safe_div(10,0))
```

---

### **Challenge 6.2 – Default & Variable Arguments**

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()
greet("Alice")

def add(*args):
    return sum(args)
print(add(1,2,3))

def user_info(**kwargs):
    print(kwargs)
user_info(name="Alice", age=30)
```

---

### **Challenge 6.3 – Lambda & Map/Filter**

```python
nums = [1,2,3,4,5]
squared = list(map(lambda x:x**2, nums))
evens = list(filter(lambda x:x%2==0, nums))
print(squared, evens)
```

---

## **Module 7: Advanced Pythonic Patterns**

### **Challenge 7.1 – Unpacking Operators**

```python
numbers = [1,2,3,4,5]
a,*b,c = numbers
merged = [*numbers, 6,7]
print(a,b,c,merged)
```

---

### **Challenge 7.2 – Enumerate & Items**

```python
fruits = ["apple","banana"]
for i, fruit in enumerate(fruits,1):
    print(i, fruit)
```

* For dicts: `for k,v in d.items(): print(k,v)`

---

### **Challenge 7.3 – Generators & Memory Awareness**

```python
squares = (x**2 for x in range(10))
for sq in squares:
    print(sq)

import sys
lst = list(range(10**6))
tpl = tuple(range(10**6))
print(sys.getsizeof(lst), sys.getsizeof(tpl))
```

---

### **Challenge 7.4 – File Handling & Context Managers**

```python
with open("test.txt","w") as f:
    f.write("Hello World")

with open("test.txt") as f:
    print(f.read())
```

---

### **Challenge 7.5 – FizzBuzz Extended**

```python
for i in range(1,31):
    output = "Fizz"*(i%3==0) + "Buzz"*(i%5==0)
    print(output or i)
```

---

### **Challenge 7.6 – Sorting & Lambda**

```python
scores = {"Alice":90,"Bob":75,"Charlie":85}
sorted_scores = {k:v for k,v in sorted(scores.items(), key=lambda item: item[1], reverse=True)}
print(sorted_scores)
```

---

### **Challenge 7.7 – Palindrome Check & String Reversal**

```python
s = "racecar"
print(s == s[::-1])

# Extended: Ignore case and spaces
s2 = "A man a plan a canal Panama".replace(" ", "").lower()
print(s2 == s2[::-1])
```

---

### **Challenge 7.8 – Nested Data & Flattening**

```python
nested = [[1,2],[3,4],[5,6]]
flat = [x for sub in nested for x in sub]
print(flat)
```

