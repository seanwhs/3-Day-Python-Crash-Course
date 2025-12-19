# **Python Lab Worksheet: Python Operators (Updated)**

**Name:** ______________________
**Date:** ______________________

**Objective:**
Understand and practice Python operators, including arithmetic, comparison, logical, assignment, membership, identity, and unpacking operators.

---

## **Part 1: Arithmetic Operators**

**Task 1:** Basic arithmetic operations

```python
a = 10
b = 3
```

```python
print(a + b)    # Addition → ________
print(a - b)    # Subtraction → ________
print(a * b)    # Multiplication → ________
print(a / b)    # Division → ________
print(a // b)   # Floor division → ________
print(a % b)    # Modulus → ________
print(a ** b)   # Exponent → ________
```

---

## **Part 2: Comparison Operators**

```python
x = 5
y = 8
```

```python
print(x == y)   # Equal → ________
print(x != y)   # Not equal → ________
print(x > y)    # Greater than → ________
print(x < y)    # Less than → ________
print(x >= y)   # Greater or equal → ________
print(x <= y)   # Less or equal → ________
```

---

## **Part 3: Logical Operators**

```python
a = True
b = False
```

```python
print(a and b)  # Logical AND → ________
print(a or b)   # Logical OR → ________
print(not a)    # Logical NOT → ________
```

* Combining comparisons:

```python
x = 10
y = 20
print(x > 5 and y < 25)  # ________
print(x > 5 or y < 15)   # ________
```

---

## **Part 4: Assignment Operators**

```python
n = 10
```

```python
n += 5   # n = n + 5 → ________
n -= 3   # n = n - 3 → ________
n *= 2   # n = n * 2 → ________
n /= 4   # n = n / 4 → ________
n %= 3   # n = n % 3 → ________
```

---

## **Part 5: Membership Operators**

```python
fruits = ["apple", "banana", "cherry"]
```

```python
print("apple" in fruits)      # ________
print("orange" not in fruits) # ________
```

---

## **Part 6: Identity Operators**

```python
x = [1, 2, 3]
y = [1, 2, 3]
z = x
```

```python
print(x is y)    # ________
print(x is z)    # ________
print(x == y)    # ________
```

---

## **Part 7: Unpacking Operators**

**Task 7a: List unpacking (`*`)**

```python
numbers = [1, 2, 3, 4, 5]
first, *middle, last = numbers
print(first)    # ________
print(middle)   # ________
print(last)     # ________
```

* Use `*` to combine lists:

```python
a = [1, 2]
b = [3, 4]
combined = [*a, *b]
print(combined)  # ________
```

**Task 7b: Dictionary unpacking (`**`)**

```python
dict1 = {"x": 1, "y": 2}
dict2 = {"y": 3, "z": 4}
merged = {**dict1, **dict2}
print(merged)   # ________  # Observe how keys are overwritten
```

* Use `**` in function calls:

```python
def greet(name, age):
    print(f"Hello {name}, you are {age} years old!")

data = {"name": "Alice", "age": 25}
greet(**data)  # Output → ________
```

---

## **Part 8: Operator Challenge**

1. Combine arithmetic, comparison, and logical operators:

```python
a = 5
b = 10
c = 15
result = (a + b > c) and (c % a == 0)
print(result)  # ________
```

2. Experiment with unpacking operators in expressions:

```python
numbers = [1, 2, 3]
more_numbers = [*numbers, 4, 5]
print(more_numbers)  # ________
```

---

