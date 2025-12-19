# **Python Crash Course 2025 – Challenge Workbook**

## **Module 1: Foundations — Variables, References & Execution**

### **Challenge 1.1 – Variable Binding & Identity**

```python
x = [1,2,3]
y = x
z = x.copy()
x.append(4)
print(x, y, z)
```

**Solution/Explanation:**
`x` and `y` reference the same list, so both reflect the change. `z` is a copy and remains `[1,2,3]`.

---

### **Challenge 1.2 – Mutable vs Immutable**

```python
a = (1,2,3)
# Try a[0] = 10
# Reassign a = (10,2,3)
```

*Solution:* Tuples are immutable, so `a[0] = 10` raises `TypeError`. Reassignment is allowed.

---

### **Challenge 1.3 – Identity vs Equality**

```python
x = [1,2,3]
y = [1,2,3]
print(x == y)  # True
print(x is y)  # False
```

*Explanation:* Equality checks values; `is` checks object identity.

---

### **Challenge 1.4 – Object Copying**

```python
import copy
nested = [[1,2],[3,4]]
shallow = nested.copy()
deep = copy.deepcopy(nested)
nested[0].append(3)
print(shallow, deep)
```

*Solution:* Shallow copy sees changes in nested lists, deep copy is independent.

---

### **Challenge 1.5 – Execution Pipeline**

```python
def foo():
    return sum(range(10))
print(foo())
```

*Tip:* Python compiles `foo()` to bytecode before execution by PVM.

---

## **Module 2: Numbers, Operators & Precision**

### **Challenge 2.1 – Float Precision**

```python
0.1 + 0.2 == 0.3  # False
from decimal import Decimal
Decimal('0.1') + Decimal('0.2') == Decimal('0.3')  # True
```

---

### **Challenge 2.2 – Arithmetic Operators**

```python
a, b = 7, 3
print(a/b, a//b, a%b, a**b)
```

---

### **Challenge 2.3 – Operator Precedence**

```python
result = 2 + 3 * 4 ** 2 / 2
print(result)
```

*Explanation:* `**` > `*`/`/` > `+`.

---

### **Challenge 2.4 – Complex Numbers**

```python
c = 3 + 4j
print(c.real, c.imag, abs(c))
```

---

### **Challenge 2.5 – Type Conversion**

```python
x = "100"
y = 5
print(int(x) + y)
```

---

## **Module 3: Strings & Text**

### **Challenge 3.1 – Slicing**

```python
text = "Python"
print(text[1:4], text[::-1], text[::2])
```

---

### **Challenge 3.2 – Case Manipulation**

```python
s = "hello world"
print(s.upper(), s.capitalize(), s.title())
```

---

### **Challenge 3.3 – F-Strings**

```python
name = "Alice"
age = 30
print(f"Name: {name}, Age: {age}")
```

---

### **Challenge 3.4 – Multi-line Strings**

```python
print("""Line 1
Line 2
Line 3""")
```

---

### **Challenge 3.5 – String Methods**

```python
s = "   Python  "
print(s.strip(), s.startswith("Py"), s.endswith("on"))
```

---

## **Module 4: Booleans & Truthiness**

### **Challenge 4.1 – Truthiness**

```python
values = [None, 0, "", [], {}, set()]
for v in values:
    print(bool(v))
```

---

### **Challenge 4.2 – Conditional Expressions**

```python
x = 10
result = "Even" if x % 2 == 0 else "Odd"
print(result)
```

---

### **Challenge 4.3 – Logical Operators**

```python
a, b = True, False
print(a and b, a or b, not a)
```

---

### **Challenge 4.4 – Membership Testing**

```python
fruits = ["apple","banana"]
print("apple" in fruits, "orange" not in fruits)
```

---

### **Challenge 4.5 – Short-circuit Evaluation**

```python
def side_effect():
    print("Called")
    return True
x = False and side_effect()  # side_effect not called
```

---

## **Module 5: Collections**

### **Challenge 5.1 – Lists & Tuples**

```python
lst = [1,2,3]
tpl = (4,5,6)
lst.append(4)
print(lst, tpl)
```

---

### **Challenge 5.2 – Sets**

```python
s = {1,2,2,3}
s.add(4)
print(s)
```

---

### **Challenge 5.3 – Dictionaries**

```python
d = {"a":1, "b":2}
d["c"] = 3
print(d)
```

---

### **Challenge 5.4 – Safe Dictionary Access**

```python
user = {"name":"Alice"}
role = user.get("role","viewer")
print(role)
```

---

### **Challenge 5.5 – Nested Dictionary**

```python
profile = {"user": {"name":"Alice"}}
age = profile.get("user", {}).get("age", 0)
print(age)
```

---

### **Challenge 5.6 – Dictionary Comprehension**

```python
words = ["apple","banana"]
lengths = {w:len(w) for w in words}
print(lengths)
```

---

### **Challenge 5.7 – List Comprehension**

```python
evens = [x**2 for x in range(1,11) if x%2==0]
print(evens)
```

---

### **Challenge 5.8 – Nested Comprehension**

```python
matrix = [[i*j for j in range(1,4)] for i in range(1,4)]
print(matrix)
```

---

### **Challenge 5.9 – Flatten Nested List**

```python
nested = [[1,2],[3,4],[5]]
flat = [x for sublist in nested for x in sublist]
print(flat)
```

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

### **Challenge 6.2 – Input Validation**

```python
try:
    age = int(input("Enter age: "))
except ValueError:
    print("Invalid input")
```

---

### **Challenge 6.3 – Default Arguments**

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")
greet()
greet("Alice")
```

---

### **Challenge 6.4 – Variable Arguments**

```python
def add(*args):
    return sum(args)
print(add(1,2,3))
```

---

### **Challenge 6.5 – Keyword Arguments**

```python
def user_info(**kwargs):
    print(kwargs)
user_info(name="Alice", age=30)
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
    print(i,fruit)
```

---

### **Challenge 7.3 – Merging & Deduplication**

```python
l1 = [1,2,3,3]
l2 = [3,4,5]
merged = list(set(l1+l2))
print(merged)
```

---

### **Challenge 7.4 – Memory Awareness**

```python
import sys
lst = list(range(10**6))
tpl = tuple(range(10**6))
print(sys.getsizeof(lst), sys.getsizeof(tpl))
```

---

### **Challenge 7.5 – Palindrome Check**

```python
s = "racecar"
print(s==s[::-1])
```

---

### **Challenge 7.6 – FizzBuzz**

```python
for i in range(1,21):
    print("Fizz"*(i%3==0)+"Buzz"*(i%5==0) or i)
```

---

### **Challenge 7.7 – Sorting Dictionary by Value**

```python
scores = {"Alice":90,"Bob":75,"Charlie":85}
sorted_scores = {k:v for k,v in sorted(scores.items(), key=lambda item: item[1], reverse=True)}
print(sorted_scores)
```

---

### **Challenge 7.8 – Generator Expression**

```python
squares = (x**2 for x in range(10))
for sq in squares:
    print(sq)
```

---

### **Challenge 7.9 – Context Managers**

```python
with open("test.txt","w") as f:
    f.write("Hello")
# file auto-closed
```

---


