# 🧪 **Hands-On Lab — Python Functions**
---
**Name:** ______________________
**Date:** ______________________
---


**Focus: contracts, reuse, and predictable behavior**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Design clear, reusable functions
* Control inputs, outputs, and side effects
* Use functions as **behavioral boundaries**
* Write functions that are easy to test and maintain

---

## **Lab Rules (Enterprise Standard)**

* Functions do **one thing**
* Prefer explicit parameters over hidden state
* Avoid side effects unless intentional
* Name functions by **what they do**, not how

---

## **Lab 1 — Defining a Simple Function**

**Basic contract**

### Task

Write a function:

```python
def greet(name):
    ...
```

### Requirements

* Accepts a name
* Returns a greeting string
* Does not print

---

## **Lab 2 — Return vs Print**

**Control output**

### Task

Call `greet()` and:

* Print the result outside the function
* Explain why returning is preferred

---

## **Lab 3 — Multiple Parameters**

**Clear inputs**

### Task

Create:

```python
def calculate_total(price, tax_rate):
    ...
```

### Requirements

* Return total price including tax
* Do not round inside the function

---

## **Lab 4 — Default Parameters**

**Safe defaults**

### Task

Add a default tax rate:

```python
def calculate_total(price, tax_rate=0.07):
    ...
```

### Question

When are defaults helpful?

---

## **Lab 5 — Keyword Arguments**

**Readable calls**

### Task

Call `calculate_total()` using keyword arguments.

---

## **Lab 6 — Input Validation**

**Fail fast**

### Task

Validate inputs:

* `price` must be non-negative
* `tax_rate` must be between `0` and `1`
* Raise `ValueError` on invalid input

---

## **Lab 7 — Avoiding Side Effects**

**Pure function**

### Task

Review:

```python
def add_discount(prices):
    prices.append(0)
```

### Requirements

* Explain the side effect
* Refactor to avoid mutating the input

---

## **Lab 8 — Returning Multiple Values**

**Structured output**

### Task

Write a function that returns:

* min value
* max value

### Requirement

* Return as a tuple
* Unpack at call site

---

## **Lab 9 — Functions Calling Functions**

**Composition**

### Task

Refactor logic so:

* One function validates input
* Another performs calculation

---

## **Lab 10 — Docstrings**

**Communicate intent**

### Task

Add a docstring that explains:

* What the function does
* Parameters
* Return value
* Exceptions raised

---

## **Lab 11 — Type Hints (Recommended)**

**Readable contracts**

### Task

Add type hints to:

```python
def calculate_total(price, tax_rate=0.07):
    ...
```

### Question

How do type hints help teams?

---

## **Lab 12 — Exception Boundaries**

**Where to handle errors**

### Task

Decide:

* Which function raises exceptions
* Which layer catches them

Explain your reasoning.

---

## **Stretch Lab — Refactor for Clarity**

**From script to functions**

### Starting Code

```python
price = 100
tax = 0.07
total = price + (price * tax)
print(total)
```

### Task

Refactor into reusable, testable functions.

---

## **Common Enterprise Mistakes**

* Printing inside functions
* Functions that do too much
* Hidden dependencies
* Silent failures

---

## **Key Takeaways**

* Functions define **contracts**
* Return values beat side effects
* Validation belongs at boundaries
* Small functions scale better

**Final mental model:**

> *Functions are promises. Keep them.*

---

