# **Python Lab Worksheet: Python Data Types**

**Name:** ______________________
**Date:** ______________________

**Objective:**
Learn about Python’s data types, how to check them, and how to perform basic operations.

---

## **Part 1: Exploring Basic Data Types**

**Task 1: Numbers**

```python
a = 10        # integer
b = 3.14      # float
c = 2 + 3j    # complex
```

* Check the type of each variable using `type()`:

```python
print(type(a))  # Output: ________
print(type(b))  # Output: ________
print(type(c))  # Output: ________
```

* Perform simple operations:

```python
print(a + b)   # Output: ________
print(a * 2)   # Output: ________
print(c + 1)   # Output: ________
```

---

**Task 2: Strings**

```python
s1 = "Hello"
s2 = 'Python'
```

* Check their type:

```python
print(type(s1))  # Output: ________
```

* Concatenate strings:

```python
result = s1 + " " + s2
print(result)    # Output: ________
```

* Repeat strings:

```python
print(s1 * 3)    # Output: ________
```

---

**Task 3: Booleans**

```python
x = True
y = False
```

* Check type and operations:

```python
print(type(x))       # Output: ________
print(x and y)       # Output: ________
print(x or y)        # Output: ________
print(not x)         # Output: ________
```

---

## **Part 2: Collections**

**Task 4: Lists**

```python
my_list = [1, 2, 3, 4]
```

* Check type and length:

```python
print(type(my_list))  # Output: ________
print(len(my_list))   # Output: ________
```

* Access elements:

```python
print(my_list[0])     # Output: ________
print(my_list[-1])    # Output: ________
```

* Modify elements:

```python
my_list[1] = 20
print(my_list)        # Output: ________
```

* Add elements:

```python
my_list.append(5)
print(my_list)        # Output: ________
```

---

**Task 5: Tuples**

```python
my_tuple = (10, 20, 30)
```

* Check type and access elements:

```python
print(type(my_tuple))  # Output: ________
print(my_tuple[1])     # Output: ________
```

* Can you change an element? Try and observe:

```python
my_tuple[0] = 100  # What happens? ________________
```

---

**Task 6: Dictionaries**

```python
my_dict = {"name": "Alice", "age": 25}
```

* Check type and access values:

```python
print(type(my_dict))       # Output: ________
print(my_dict["name"])     # Output: ________
```

* Add a new key-value pair:

```python
my_dict["city"] = "Singapore"
print(my_dict)             # Output: ________
```

---

**Task 7: Sets**

```python
my_set = {1, 2, 3, 3, 4}
```

* Check type and elements:

```python
print(type(my_set))   # Output: ________
print(my_set)         # Output: ________  # Note duplicates
```

* Add an element:

```python
my_set.add(5)
print(my_set)         # Output: ________
```

---

## **Part 3: Type Conversion**

**Task 8:** Convert between types

```python
x = 10
y = 3.14
s = "123"
```

* Convert float to int:

```python
print(int(y))      # Output: ________
```

* Convert int to float:

```python
print(float(x))    # Output: ________
```

* Convert string to int:

```python
print(int(s))      # Output: ________
```

* Convert int to string:

```python
print(str(x))      # Output: ________
```

---

## **Part 4: Extra Challenge**

1. Create a variable of each type (int, float, complex, string, list, tuple, set, dictionary, bool).
2. Use `type()` to confirm the type.
3. Try combining operations where possible (e.g., concatenate strings, add numbers).
4. Note down any errors and explain why they occurred:

| Variable | Type | Operation | Result / Error |
| -------- | ---- | --------- | -------------- |
|          |      |           |                |
|          |      |           |                |
|          |      |           |                |

---

