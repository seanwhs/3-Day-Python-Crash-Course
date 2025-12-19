# 🧪 **Hands-On Lab — Python Magic Methods**

**Focus: making objects behave predictably in real systems**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Implement magic methods intentionally
* Improve debuggability and readability
* Integrate custom objects cleanly with Python syntax
* Avoid overengineering and misuse

---

## **Lab Rules (Enterprise Standard)**

* Implement magic methods **only when they add clarity**
* Behavior must match developer expectations
* Avoid surprising side effects
* Prefer explicit behavior over cleverness

---

## **Lab 1 — `__init__` (Object Creation)**

**Establish valid state**

### Task

Create a `User` class.

### Requirements

* Attributes: `username`, `role`
* Validate inputs
* Raise `ValueError` for invalid values

---

## **Lab 2 — `__str__` (Human-Readable Output)**

**Logs and UI**

### Task

Implement `__str__` for `User`.

### Requirements

* Output must be readable
* Suitable for logs and print statements

---

## **Lab 3 — `__repr__` (Debug Output)**

**Developer-facing representation**

### Task

Implement `__repr__`.

### Requirements

* Unambiguous
* Ideally copy-pasteable
* Helps debugging

---

## **Lab 4 — Equality with `__eq__`**

**Value-based comparison**

### Task

Compare users by `username`.

### Requirements

* Implement `__eq__`
* Handle comparison with non-`User` objects safely

---

## **Lab 5 — Hashing with `__hash__`**

**Using objects in sets and dicts**

### Task

Make `User` hashable.

### Requirements

* Ensure hash is consistent with `__eq__`
* Use only immutable fields

### Question

Why is this dangerous if state changes?

---

## **Lab 6 — Length with `__len__`**

**Intuitive behavior**

### Task

Create a `Team` class.

### Requirements

* Store users internally
* `len(team)` returns number of users

---

## **Lab 7 — Containment with `__contains__`**

**Readable membership checks**

### Task

Extend `Team`.

### Requirements

* Allow:

  ```python
  if user in team:
      ...
  ```

---

## **Lab 8 — Iteration with `__iter__`**

**Integrate with loops**

### Task

Make `Team` iterable.

### Requirements

* Support:

  ```python
  for user in team:
      ...
  ```

---

## **Lab 9 — Callable Objects (`__call__`)**

**Objects that act like functions**

### Task

Create a `PermissionChecker`.

### Requirements

* `checker(user)` returns `True` or `False`
* Hide internal logic

---

## **Lab 10 — Context Managers (`__enter__`, `__exit__`)**

**Resource safety**

### Task

Create a simple context manager.

### Requirements

* Print `"Start"` on enter
* Print `"End"` on exit
* Ensure exit runs even on error

---

## **Lab 11 — Operator Overloading (`__add__`)**

**Only when meaningful**

### Task

Create a `Money` class.

### Requirements

* Support addition of same currency
* Raise error for mismatched currencies

---

## **Lab 12 — Anti-Pattern Recognition**

**When NOT to use magic methods**

### Task

Review this idea:

> Override `__add__` to merge users

### Questions

* Is this intuitive?
* What would be clearer?

---

## **Stretch Lab — Design Challenge**

**Design before coding**

### Scenario

You are designing a `TaskQueue` object.

### Requirements

* Supports:

  * `len(queue)`
  * Iteration
  * Membership checks
* Justify each magic method used

---

## **Common Enterprise Mistakes**

* Overloading operators for surprise behavior
* Implementing too many magic methods
* Mutable objects used as dict keys
* Prioritizing cleverness over clarity

---

## **Key Takeaways**

* Magic methods integrate with Python syntax
* Behavior must be intuitive
* Less is more
* Explicit is still better than implicit

**Final mental model:**

> *Magic methods should feel boring.*

---
