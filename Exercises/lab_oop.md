# 🧪 **Hands-On Lab — Object-Oriented Programming (OOP)**

**Focus: modeling, encapsulation, behavior**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Model real business entities as classes
* Use encapsulation to protect state
* Apply inheritance responsibly
* Read and refactor class-based code in production systems

---

## **Lab Rules (Enterprise Standard)**

* Classes represent **things with behavior**
* Avoid “data-only” classes
* Keep methods small and intentional
* Prefer composition over inheritance

---

## **Lab 1 — Defining a Simple Class**

**Model a real entity**

### Task

Create a `User` class.

### Requirements

* Attributes: `username`, `role`
* Method: `describe()` → returns a readable string

---

## **Lab 2 — Instance vs Class**

**Understand object creation**

### Task

* Create two `User` objects
* Print each description
* Confirm they hold independent state

---

## **Lab 3 — Encapsulation**

**Protect internal state**

### Task

Extend `User`:

### Requirements

* Add private attribute `_active`
* Add methods:

  * `deactivate()`
  * `is_active()`

**Rule:** no direct access to `_active` outside the class

---

## **Lab 4 — Constructor Validation**

**Fail early**

### Task

Validate inputs in `__init__`.

### Requirements

* `username` must not be empty
* `role` must be one of: `admin`, `editor`, `viewer`
* Raise `ValueError` on invalid input

---

## **Lab 5 — Behavior, Not Data**

**Avoid anemic models**

### Task

Add method:

```python
can_edit()
```

### Rules

* `admin` and `editor` → `True`
* `viewer` → `False`

---

## **Lab 6 — Inheritance (Used Carefully)**

**Specialize behavior**

### Task

Create an `AdminUser` class.

### Requirements

* Inherits from `User`
* Default role is `admin`
* Adds method:

  ```python
  reset_password()
  ```

### Question

Is inheritance justified here?

---

## **Lab 7 — Method Override**

**Custom behavior**

### Task

Override `describe()` in `AdminUser` to:

* Include admin-specific wording
* Still reuse parent logic where possible

---

## **Lab 8 — Composition Over Inheritance**

**Attach responsibilities**

### Task

Create a `Permission` class.

### Requirements

* Stores a set of permissions
* Method:

  ```python
  has(permission)
  ```

### Update `User`

* Inject a `Permission` object
* Delegate permission checks

---

## **Lab 9 — Avoid Shared Mutable State**

**Classic enterprise bug**

### Task

Fix this code:

```python
class User:
    permissions = set()
```

### Questions

* What is the problem?
* How do you fix it?

---

## **Lab 10 — String Representation**

**Debuggability**

### Task

Implement:

```python
__str__()
__repr__()
```

### Rule

* Output must help debugging and logs

---

## **Lab 11 — Real-World Refactor**

**From procedural to OOP**

### Starting Code

```python
def can_user_edit(user):
    return user["role"] in ("admin", "editor")
```

### Task

Move this logic into the `User` class.

---

## **Stretch Lab — Design Challenge**

**Think before coding**

### Scenario

Model a system with:

* Users
* Roles
* Permissions
* Account status (active / suspended)

### Task

* Sketch classes
* Decide what owns what
* Justify inheritance vs composition

---

## **Common Enterprise OOP Mistakes**

* God classes
* Inheritance for reuse only
* Public attributes everywhere
* Logic outside the model

---

## **Key Takeaways**

* Classes model **behavior + state**
* Encapsulation protects invariants
* Inheritance is optional, not mandatory
* Composition scales better

**Final mental model:**

> *Good OOP models the business, not the database.*

---

