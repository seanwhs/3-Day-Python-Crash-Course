# 🧪 **Hands-On Lab — Python String Operations**

**Focus: text processing, validation, formatting**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Manipulate strings **safely and correctly**
* Apply **immutable string mental models**
* Clean and validate real-world text inputs
* Use Python’s string tools instead of custom hacks

---

## **Lab Rules (Enterprise Standard)**

* No mutation assumptions (strings are immutable)
* Prefer built-in methods over manual loops
* Code must be readable by a new hire
* Avoid clever one-liners unless obvious

---

## **Lab 1 — String Immutability**

**Understand what does *not* change**

### Task

```python
text = "hello"
```

### Requirements

1. Convert `text` to uppercase
2. Print the original value
3. Print the new value

### Reflection

* Why didn’t the original string change?
* What does this imply for performance and safety?

---

## **Lab 2 — Trimming User Input**

**Sanitising external input**

### Task

```python
raw_input = "   alice@example.com  "
```

### Requirements

* Remove leading and trailing whitespace
* Store the cleaned value
* Print both original and cleaned strings

---

## **Lab 3 — Case Normalisation**

**Consistent comparisons**

### Task

```python
role = "Admin"
```

### Requirements

* Convert the role to lowercase
* Compare it safely against `"admin"`
* Print `"Access granted"` or `"Access denied"`

---

## **Lab 4 — String Validation**

**Check for empty or invalid input**

### Task

```python
username = "   "
```

### Requirements

* Strip whitespace
* If empty after stripping, print `"Invalid username"`
* Otherwise, print `"Username accepted"`

---

## **Lab 5 — Splitting Strings**

**Parsing structured text**

### Task

```python
csv_line = "alice,admin,active"
```

### Requirements

* Split into individual values
* Assign them to variables
* Print each value on a new line

---

## **Lab 6 — Joining Strings**

**Generate output cleanly**

### Task

```python
parts = ["2025", "09", "30"]
```

### Requirements

* Join into a date string: `2025-09-30`
* Print the result

---

## **Lab 7 — String Search**

**Membership and position**

### Task

```python
email = "user@company.com"
```

### Requirements

* Check if `"@"` exists
* Check if email ends with `"company.com"`
* Print clear validation messages

---

## **Lab 8 — Replace vs Translate**

**Controlled text updates**

### Task

```python
message = "Error: connection failed"
```

### Requirements

* Replace `"Error"` with `"WARNING"`
* Print the updated message
* Confirm the original string is unchanged

---

## **Lab 9 — f-Strings (Required Standard)**

**Readable formatting**

### Task

```python
user = "alice"
role = "admin"
```

### Requirements

* Use an f-string to produce:

  ```
  User alice has role admin
  ```

---

## **Lab 10 — Real-World Parsing**

**Extract structured information**

### Task

```python
log = "2025-09-30 INFO User alice logged in"
```

### Requirements

1. Extract the date
2. Extract the username
3. Print a formatted summary using f-strings

---

## **Lab 11 — Common Pitfall**

**❌ Incorrect approach**

```python
text = "hello"
text[0] = "H"
```

### Questions

* Why does this fail?
* What is the correct approach?

---

## **Lab 12 — Choose the Right Method**

For each task, name the **best string method**:

1. Remove whitespace
2. Check prefix
3. Check suffix
4. Replace text
5. Split CSV values

---

## **Stretch Lab — Input Cleaning Pipeline**

**Enterprise-style processing**

### Task

Given:

```python
raw = "  Alice.ADMIN@Company.Com  "
```

### Requirements

* Trim whitespace
* Convert to lowercase
* Validate it contains `"@"`
* Print a clean, validated result

---

## **Common Enterprise Mistakes**

* Assuming strings are mutable
* Manual loops instead of built-ins
* Case-sensitive comparisons
* Overusing regex when not needed

---

## **Key Takeaways**

* Strings are **immutable**
* Built-in methods cover most needs
* Clean input early
* f-strings are the standard

**Final mental model:**

> *Strings don’t change — you replace them.*

---

