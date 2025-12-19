# 🧪 **Hands-On Lab — Variables & Memory Management**

**Focus: references, mutability, lifetime, side effects**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Explain how variables reference objects
* Predict behavior of mutable vs immutable objects
* Avoid accidental shared state
* Write safer, side-effect-free functions

---

## **Lab Rules (Enterprise Standard)**

* Variables are **references**, not boxes
* Objects live independently of variable names
* Mutability changes risk profiles
* Assume code will be reused and passed around

---

## **Lab 1 — Variables Are References**

**Understand assignment**

### Task

```python
a = 10
b = a
```

### Requirements

1. Print `a` and `b`
2. Reassign `a` to a new value
3. Print `a` and `b` again

### Reflection

* Why didn’t `b` change?

---

## **Lab 2 — Object Identity**

**Same object or not?**

### Task

```python
x = [1, 2, 3]
y = x
```

### Requirements

* Compare `x == y`
* Compare `x is y`
* Modify `x`
* Observe `y`

---

## **Lab 3 — Mutable vs Immutable**

**Behavior difference**

### Task

```python
a = 100
b = a

x = [1, 2]
y = x
```

### Requirements

* Modify `a`
* Modify `x`
* Observe which changes propagate and why

---

## **Lab 4 — Rebinding vs Mutation**

**Critical distinction**

### Task

```python
nums = [1, 2, 3]
```

### Requirements

1. Rebind `nums` to a new list
2. Mutate the original list
3. Explain the difference in behavior

---

## **Lab 5 — Function Arguments**

**Passing references**

### Task

```python
def add_item(items):
    items.append("new")
```

### Requirements

* Pass a list into the function
* Observe the caller’s list after the function call

### Question

Why did this happen?

---

## **Lab 6 — Avoiding Side Effects**

**Safe function design**

### Task

Refactor the previous function so it:

* Does **not** modify the original list
* Returns a new list instead

---

## **Lab 7 — Default Argument Trap**

**Classic production bug**

### Task

Review:

```python
def add_user(user, users=[]):
    users.append(user)
    return users
```

### Requirements

* Call the function multiple times
* Observe behavior
* Explain why this happens

---

## **Lab 8 — Fixing Mutable Defaults**

**Correct pattern**

### Task

Fix the previous function using:

* `None` as default
* Internal initialization

---

## **Lab 9 — Copying Objects**

**Shallow vs deep**

### Task

```python
import copy

original = {"roles": ["admin", "editor"]}
```

### Requirements

1. Create a shallow copy
2. Create a deep copy
3. Modify nested data
4. Observe differences

---

## **Lab 10 — Identity vs Equality**

**Critical debugging skill**

### Task

```python
a = [1, 2, 3]
b = [1, 2, 3]
```

### Requirements

* Compare with `==`
* Compare with `is`
* Explain when each is appropriate

---

## **Lab 11 — Lifetime & Garbage Collection**

**What gets cleaned up**

### Task

Create an object inside a function and return nothing.

### Questions

* When is the object eligible for garbage collection?
* What controls its lifetime?

---

## **Lab 12 — Real-World Bug Analysis**

**Shared state**

### Scenario

Two services share a configuration object and one mutates it.

### Questions

* Why is this dangerous?
* How do you prevent it?

---

## **Stretch Lab — Design Challenge**

**Safe API design**

### Task

Design a function that:

* Accepts a collection
* Does not mutate caller state
* Is safe for concurrent use

Explain your choices.

---

## **Common Enterprise Mistakes**

* Assuming assignment copies objects
* Mutable defaults
* Hidden side effects
* Overusing `is`

---

## **Key Takeaways**

* Variables point to objects
* Mutation is observable everywhere
* Immutability reduces risk
* Copy intentionally

**Final mental model:**

> *Names change easily. Objects don’t.*

---
