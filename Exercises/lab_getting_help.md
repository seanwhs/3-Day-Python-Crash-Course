# **Python Lab Worksheet: Getting Help in Python**
---
**Name:** ______________________
**Date:** ______________________
---
**Objective:**
Learn to explore Python objects, modules, and built-in functions using `help()`, `dir()`, and the `builtins` module.

---

## **Part 1: Using `help()`**

**Task 1: Start the interactive help system**

```python
help()
```

* What happens when you run `help()`?

**Answer / Notes:**

---

---

**Task 2: Get help on a specific function**

```python
help(print)
```

* What arguments does `print()` take?
* Try using `sep` and `end` in a small print statement.

**Example Output / Notes:**

---

---

**Task 3: Get help on a module**

```python
import math
help(math)
```

* Pick three functions you didn’t know before and note what they do:

1. ---
2. ---
3. ---

* Try using one function in code:

```python
# Example:
result = math.sqrt(16)
print(result)
```

**Output:** __________________________

---

## **Part 2: Using `dir()`**

**Task 4: Inspect an object**

```python
x = [1, 2, 3]
dir(x)
```

* List two methods you see: ________________________
* Try one method:

```python
x.append(4)
print(x)
```

**Output:** __________________________

---

**Task 5: Explore built-in functions**

```python
import builtins
dir(builtins)
```

* Pick three built-in functions you haven’t used: ______________________
* Use `help()` to learn about them:

```python
help(builtins.abs)
help(builtins.all)
help(builtins.sorted)
```

* Try each function with a short example:

1. Function: ________  Example: ____________________ Output: _________
2. Function: ________  Example: ____________________ Output: _________
3. Function: ________  Example: ____________________ Output: _________

---

## **Part 3: Combining `dir()` and `help()`**

**Task 6: Investigate a string object**

```python
s = "Hello, Python!"
dir(s)        # List all string methods
help(s.upper) # Learn how to use the 'upper' method
print(s.upper())
```

* Try at least two more string methods:

1. Method: ________ Example: ____________________ Output: _________
2. Method: ________ Example: ____________________ Output: _________

---

## **Part 4: Built-in Functions Challenge**

1. Pick **five built-in functions** from `dir(builtins)` you have never used.
2. Use `help()` to understand them.
3. Write a small example for each:

| Function | Example Code | Output / Notes |
| -------- | ------------ | -------------- |
|          |              |                |
|          |              |                |
|          |              |                |
|          |              |                |
|          |              |                |

---

## **Part 5: Extra Tips**

* Use `help("keywords")` to see all Python keywords.
* Use `dir()` + `help()` to explore **any Python object or module**.

---

