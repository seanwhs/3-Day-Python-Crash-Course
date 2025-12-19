# 🧪 **Hands-On Lab — Python Exception Handling**

**Focus: predictable failures, clear recovery, safe systems**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Catch **specific exceptions**
* Apply **EAFP** (Easier to Ask Forgiveness than Permission)
* Preserve error context
* Write failure-safe, debuggable code

---

## **Lab Rules (Enterprise Standard)**

* Catch **specific**, not generic, exceptions
* Never swallow errors silently
* Log or re-raise with intent
* Exceptions represent **unexpected states**, not control flow

---

## **Lab 1 — Basic `try / except`**

**Handle failure explicitly**

### Task

```python
value = int("42")
```

### Requirements

* Wrap in `try / except`
* Catch the correct exception
* Print a helpful message on failure

---

## **Lab 2 — Catching Specific Exceptions**

**Avoid blanket `except`**

### Task

```python
value = int("abc")
```

### Requirements

* Catch only `ValueError`
* Do **not** use bare `except`

---

## **Lab 3 — EAFP Pattern**

**Try first, handle failure**

### Task

Given:

```python
config = {"timeout": 30}
```

### Requirements

* Read `config["retries"]`
* Use EAFP
* Provide a default value on failure

---

## **Lab 4 — Avoiding LBYL**

**Why pre-checking is brittle**

### Task

Compare:

```python
if "retries" in config:
    retries = config["retries"]
```

vs

```python
try:
    retries = config["retries"]
except KeyError:
    retries = 3
```

### Question

Why is EAFP preferred in Python?

---

## **Lab 5 — Multiple Exceptions**

**Handle related failures**

### Task

```python
data = {"count": "ten"}
```

### Requirements

* Convert `data["count"]` to `int`
* Catch all relevant exceptions
* Handle them explicitly

---

## **Lab 6 — `else` Clause**

**Success-only logic**

### Task

Use:

* `try`
* `except`
* `else`

### Requirements

* Print `"Conversion successful"` only if no exception occurs

---

## **Lab 7 — `finally` Clause**

**Guaranteed cleanup**

### Task

Simulate opening a resource.

### Requirements

* Always print `"Cleanup complete"`
* Even if an error occurs

---

## **Lab 8 — Raising Exceptions**

**Fail fast**

### Task

Create a function:

```python
def withdraw(balance, amount):
    ...
```

### Requirements

* Raise `ValueError` if `amount` is negative
* Raise `RuntimeError` if balance is insufficient

---

## **Lab 9 — Re-raising Exceptions**

**Preserve context**

### Task

Catch an exception, log a message, then re-raise it.

### Rule

* Do not lose the original traceback

---

## **Lab 10 — Custom Exceptions**

**Express intent**

### Task

Create:

```python
class InvalidRoleError(Exception):
    pass
```

### Requirements

* Raise it when role validation fails
* Catch it separately from built-in exceptions

---

## **Lab 11 — Do Not Swallow Errors**

**Anti-pattern**

### Review

```python
try:
    risky_operation()
except Exception:
    pass
```

### Questions

* Why is this dangerous?
* What should be done instead?

---

## **Lab 12 — Exception Boundaries**

**Where to catch**

### Task

Decide where exceptions should be handled:

* Low-level utility function
* Business logic layer
* API boundary

Explain your reasoning.

---

## **Stretch Lab — Real-World Scenario**

**Design for failure**

### Scenario

You are processing user input from an API.

### Requirements

* Validate input
* Raise meaningful exceptions
* Catch exceptions at the boundary
* Return safe error messages

---

## **Common Enterprise Mistakes**

* Catching `Exception`
* Using exceptions for normal logic
* Losing stack traces
* Silent failures

---

## **Key Takeaways**

* Exceptions signal **unexpected failure**
* Catch only what you can handle
* EAFP is Pythonic
* Silence is the worst error handling

**Final mental model:**

> *Errors should be loud, clear, and intentional.*

---

