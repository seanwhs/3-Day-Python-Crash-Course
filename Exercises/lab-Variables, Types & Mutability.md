# **Python Lab: Variables, Types & Mutability**

**Name:** ______________________
**Date:** ______________________

**Objective**

* Understand Python’s **dynamic typing**
* Learn to inspect types using `type()` and `isinstance()`
* Observe differences between **mutable** and **immutable** objects

---

## **Exercise 1 — Assign Different Types**

**Instructions**

1. Assign different types of values to the same variable.
2. Print the value and its type.

```python
# Assign integer
x = 10
print(x, type(x))

# Assign float
x = 3.14
print(x, type(x))

# Assign string
x = "hello"
print(x, type(x))

# Assign boolean
x = True
print(x, type(x))
```

**Expected Output**

```
10 <class 'int'>
3.14 <class 'float'>
hello <class 'str'>
True <class 'bool'>
```

**Memory Diagram**

```
x -> 10   (int)
x -> 3.14 (float)
x -> "hello" (str)
x -> True   (bool)
```

**Observation Questions**

* How the same variable can hold different types.
* No explicit type declaration is required in Python.

---

## **Exercise 2 — Checking Types Explicitly**

**Instructions**

1. Create a variable and check its type using `type()` and `isinstance()`.

```python
value = [1, 2, 3]

print(type(value))
print(isinstance(value, list))
print(isinstance(value, tuple))
```

**Expected Output**

```
<class 'list'>
True
False
```

**Observation Questions**

* `type()` returns the exact type of an object.
* `isinstance()` checks if an object is an instance of a class (or subclass).

---

## **Exercise 3 — Immutable Objects (Integers & Strings)**

**Instructions**

1. Assign integers and strings to variables.
2. Reassign or modify them. Observe what changes.

```python
# Integers
a = 10
b = a
a = a + 5
print(a)
print(b)

# Strings
s1 = "python"
s2 = s1
s1 = s1.upper()
print(s1)
print(s2)
```

**Expected Output**

```
15
10
PYTHON
python
```

**Memory Diagram**

```
Integers:
a -> 10  b -> 10
a -> 15  b -> 10   # new object for a, b unchanged

Strings:
s1 -> "python"
s2 -> "python"
s1 -> "PYTHON"  # new object for s1, s2 unchanged
```

**Observation Questions**

* Original objects are **unchanged**.
* Reassignment creates **new objects**.

---

## **Exercise 4 — Mutable Objects (Lists)**

**Instructions**

1. Create a list and assign it to another variable.
2. Modify the list and observe changes.

```python
list1 = [1, 2, 3]
list2 = list1

list1.append(4)

print(list1)
print(list2)
```

**Expected Output**

```
[1, 2, 3, 4]
[1, 2, 3, 4]
```

**Memory Diagram**

```
list1 ---> [1, 2, 3, 4] <--- list2
# Both variables reference the same object
```

**Observation Questions**

* Both variables reflect the change.
* Mutability allows in-place modification.

---

## **Reflection Questions**

1. Which objects changed in place? ✅
2. Which created new objects? ✅
3. How could this behavior cause unexpected bugs?

---

## **Key Takeaway**

> Python variables are **references**, and **mutability** determines whether changes are shared between variables referencing the same object.

