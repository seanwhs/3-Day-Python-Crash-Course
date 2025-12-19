# 🧪 **Hands-On Lab — Python Collections**

**Focus: list · tuple · dict · set**

---

## **Lab Objectives**

By the end of this lab, engineers can:

* Choose the **correct collection** for a problem
* Manipulate collections safely
* Avoid common enterprise pitfalls
* Read and reason about collection-heavy code

---

## **Setup**

* Python 3.9+
* No external libraries
* Use REPL, Jupyter Notebook, or `.py` file

---

## **Lab 1 — Lists (Sequences That Change)**

### **Task**

You are given a list of task names.
Add a new task and remove invalid ones.

```python
tasks = ["design", "build", "", "test", None, "deploy"]
```

### **Requirements**

* Remove empty or `None` values
* Add `"monitor"` at the end
* Print the final list

### **Expected Outcome**

* Order preserved
* Only valid task names remain

---

## **Lab 2 — Lists vs Sets (Membership Check)**

### **Task**

You are validating user roles.

```python
roles = ["admin", "editor", "viewer", "admin", "viewer"]
```

### **Requirements**

1. Remove duplicates
2. Check if `"admin"` exists
3. Explain **why your chosen collection is correct**

---

## **Lab 3 — Tuples (Fixed Structure)**

### **Task**

Represent a database connection endpoint.

### **Requirements**

* Store `host`, `port`, `database`
* Unpack values into variables
* Attempt to modify one value (observe result)

```python
connection = ("localhost", 5432, "users")
```

### **Reflection**

* Why is immutability useful here?

---

## **Lab 4 — Dictionaries (Identity & Lookup)**

### **Task**

Model users by ID.

```python
users = {
    101: {"name": "Alice", "role": "admin"},
    102: {"name": "Bob", "role": "viewer"},
}
```

### **Requirements**

1. Retrieve Alice’s role
2. Safely get a role for a non-existent user
3. Loop and print: `id → role`

---

## **Lab 5 — Safe Access Pattern**

### **Task**

Avoid runtime errors when data is incomplete.

```python
config = {
    "timeout": 30,
}
```

### **Requirements**

* Read `timeout`
* Read `retries` with a default value of `3`
* Do **not** raise `KeyError`

---

## **Lab 6 — Sets (Fast Membership)**

### **Task**

You are checking access permissions.

```python
permissions = {"read", "write"}
```

### **Requirements**

* Check if `"delete"` is allowed
* Add `"delete"`
* Recheck membership

---

## **Lab 7 — Nested Collections (Real-World Shape)**

### **Task**

Model users and their roles.

```python
users = {
    "u1": {"roles": {"admin", "editor"}},
    "u2": {"roles": {"viewer"}},
}
```

### **Requirements**

1. Check if `u1` is an admin
2. Add `"editor"` to `u2`
3. Print all users with their roles

---

## **Lab 8 — Mutation Pitfall**

### **Task**

Remove negative values safely.

```python
values = [5, -3, 8, -1, 0, 7]
```

### **Requirements**

* Do **not** mutate while iterating
* Produce a clean list with only non-negative values

---

## **Lab 9 — Choose the Right Collection**

For each requirement, choose the correct collection and explain **why**:

1. Ordered event history
2. Unique feature flags
3. Configuration that must not change
4. Lookup user by ID

---

## **Stretch Exercise (Optional)**

### **Task**

Convert this data into a better structure:

```python
records = [
    ("u1", "admin"),
    ("u2", "viewer"),
    ("u1", "editor"),
]
```

### **Goal**

* Group roles by user
* Avoid duplicates
* Enable fast membership checks

---

## **Key Takeaways**

* Collections express **intent**
* Wrong choice = unnecessary complexity
* Lists, tuples, dicts, and sets each exist for a reason

**Final mental model:**

> *Data structure choice is a design decision.*

---


