# **Python Lab: Safe Dictionary Access**

**Name:** ______________________
**Date:** ______________________

**Objective:**
Learn how to safely access dictionary keys using `dict.get()` to avoid `KeyError` and provide default values.

---

## **Part 1: Basic Safe Access**

**Task 1:** Access a key that exists

```python
user = {"name": "Alice", "role": "admin"}

# Use dict.get() to access "role"
role = user.get("role", "viewer")
print(role)  # Output → ________
```

**Task 2:** Access a key that does NOT exist

```python
user = {"name": "Bob"}

# Use dict.get() to access "role" safely
role = user.get("role", "viewer")
print(role)  # Output → ________
```

---

## **Part 2: Multiple Keys**

**Task 3:** Safely access multiple keys

```python
user = {"name": "Charlie", "email": "charlie@example.com"}

name = user.get("name", "Unknown")
role = user.get("role", "viewer")
email = user.get("email", "not_provided")

print(name)   # Output → ________
print(role)   # Output → ________
print(email)  # Output → ________
```

---

## **Part 3: Nested Dictionaries**

**Task 4:** Access nested dictionary safely

```python
user = {
    "name": "Dana",
    "profile": {"age": 28, "city": "Singapore"}
}

# Access profile info safely
age = user.get("profile", {}).get("age", 0)
country = user.get("profile", {}).get("country", "Unknown")

print(age)      # Output → ________
print(country)  # Output → ________
```

> **Hint:** Using `.get("profile", {})` ensures that if `"profile"` is missing, we get an empty dictionary instead of `None`, avoiding an error.

---

## **Part 4: Lab Challenge**

**Task 5:** Create a function `get_user_info(user)` that safely returns a tuple `(name, role, city)` with defaults `"Unknown"`, `"viewer"`, and `"N/A"` respectively.

```python
def get_user_info(user):
    # Your code here
    ...
    
# Test cases
user1 = {"name": "Eve", "role": "admin", "city": "Paris"}
user2 = {"name": "Frank"}  # Missing role and city

print(get_user_info(user1))  # Output → ________
print(get_user_info(user2))  # Output → ________
```

---

✅ **Lab Outcome:**
After completing this lab, you should be able to:

1. Access dictionary keys safely using `dict.get()`.
2. Provide default values for missing keys.
3. Handle nested dictionaries without causing `KeyError`.
4. Write robust code that works with optional or incomplete data.

