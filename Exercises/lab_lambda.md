# 🧪 **Hands-On Lab — Python `lambda`**
---
**Name:** ______________________
**Date:** ______________________
---


**Focus: small, disposable functions used correctly**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Use `lambda` for **simple, local transformations**
* Recognize when `def` is the better choice
* Read and refactor lambda-heavy production code
* Avoid common lambda pitfalls

---

## **Lab Rules (Enterprise Standard)**

* Lambdas must fit on **one line**
* No side effects
* No business logic in lambdas
* If you must explain it → use `def`

---

## **Lab 1 — Basic Lambda**

**One expression, one purpose**

### Task

Create a lambda that squares a number.

### Requirements

* Accept one argument
* Return the square
* Call it with `5`

---

## **Lab 2 — Lambda vs `def`**

**Recognize equivalence**

### Task

Rewrite this function as a lambda:

```python
def is_even(n):
    return n % 2 == 0
```

### Question

Which version is clearer—and why?

---

## **Lab 3 — Lambda with `sorted()`**

**Inline behavior**

### Task

Sort users by last login time.

```python
users = [
    {"name": "Alice", "last_login": 5},
    {"name": "Bob", "last_login": 2},
    {"name": "Carol", "last_login": 8},
]
```

### Requirements

* Use `sorted()`
* Use a lambda as the key
* Sort by `last_login`

---

## **Lab 4 — Lambda with `map()`**

**Simple transformations**

### Task

Convert a list of prices to include tax.

```python
prices = [100, 200, 300]
```

### Requirements

* Add 7% tax
* Use `map()` and `lambda`
* Return a new list

---

## **Lab 5 — Lambda with `filter()`**

**Boolean predicates**

### Task

Filter active users.

```python
users = [
    {"name": "Alice", "active": True},
    {"name": "Bob", "active": False},
]
```

### Requirements

* Keep only active users
* Use `filter()` and `lambda`

---

## **Lab 6 — Readability Check**

**Refactor if unclear**

### Task

Review this code:

```python
result = list(map(lambda x: x * x if x > 0 else 0, values))
```

### Requirements

* Decide if this lambda is acceptable
* If not, refactor using `def`

---

## **Lab 7 — Lambda and Scope**

**Closures**

### Task

Predict the output:

```python
funcs = []

for i in range(3):
    funcs.append(lambda: i)

for f in funcs:
    print(f())
```

### Questions

* Why does this happen?
* How do you fix it?

---

## **Lab 8 — Fix the Closure**

**Correct binding**

### Task

Fix the previous lab using default arguments.

---

## **Lab 9 — When NOT to Use Lambda**

**Identify misuse**

### Task

Explain what is wrong with this code:

```python
lambda x: (
    print(x),
    x * 2,
    x / 3
)
```

### Question

What should be used instead?

---

## **Lab 10 — Enterprise Refactor**

**From lambda to named function**

### Starting Code

```python
handler = lambda request: request["user"]["role"] in ("admin", "editor")
```

### Task

Refactor into a named function with clear intent.

---

## **Stretch Lab — Decision Making**

For each scenario, answer **Lambda or `def`?** and why:

1. Sorting items by timestamp
2. Validating business rules
3. One-off data transformation
4. Error-handling logic

---

## **Common Enterprise Mistakes**

* Lambdas doing too much
* Nested lambdas
* Hidden side effects
* Clever one-liners

---

## **Key Takeaways**

* Lambdas are **disposable**
* Clarity beats brevity
* `def` is always acceptable
* Lambdas shine in **keys and predicates**

**Final mental model:**

> *A lambda is a throwaway function, not a design.*

---
