# 🐍 Day 2 Quiz – Functions, Data Structures & File Handling

---

## **Part 1: Multiple Choice Questions (MCQs)**

1. Which of the following is **immutable** in Python?
   a) List
   b) Tuple
   c) Set
   d) Dictionary

2. What is the output of this code?

```python
def add(a, b=5):
    return a + b

print(add(3))
```

a) 3
b) 8
c) 5
d) Error

3. Which method would you use to **replace all vowels** in a string with `*`?
   a) `string.replace("aeiou", "*")`
   b) `string.replace("a","*").replace("e","*")...`
   c) `string.upper()`
   d) `string.strip()`

4. What is the **correct way to open a file for writing** in Python?
   a) `open("file.txt", "r")`
   b) `open("file.txt", "w")`
   c) `open("file.txt", "a")`
   d) Both b and c

5. Which data structure is best for **storing unique elements**?
   a) List
   b) Tuple
   c) Set
   d) Dictionary

---

## **Part 2: True/False**

1. Functions in Python can return multiple values. (True / False)
2. Lists and tuples are both mutable. (True / False)
3. Dictionaries store data in key-value pairs. (True / False)
4. The `with` statement automatically closes files after use. (True / False)
5. Global variables can be accessed inside functions without passing them as arguments. (True / False)

---

## **Part 3: Short Answer / Code Output**

1. What will this code print?

```python
def is_even(n):
    return n % 2 == 0

print(is_even(7))
```

2. Write a function `greet_user()` that asks for the user’s name and prints:

```
Hello, <name>!
```

3. What will this print?

```python
numbers = {1, 2, 2, 3, 4}
numbers.add(5)
print(numbers)
```

4. Write a **tuple of 4 cities** you want to visit. Try to modify one element – what happens?

5. Given this code:

```python
name = "Alice"
age = 25
print(f"{name} will be {age + 5} in 5 years.")
```

What is printed?

---

## **Part 4: File Handling & CSV**

1. Write Python code to create a file `quotes.txt` and write **3 of your favorite quotes**.

2. Write Python code to **read the file** and print each line.

3. Using `csv` module, write a CSV file `contacts.csv` with columns: Name, Phone, Email. Add **3 contacts**.

4. Read the CSV file and print all rows.

5. Explain why using `with open(...) as f:` is preferred over just `open(...)`.

---

## **Part 5: Mini Project / Problem Solving**

1. Write a **function `calculate_area(width, height)`** that returns the area of a rectangle.

2. Create a **list of 5 favorite movies** and print them all.

3. Write a **quiz game** with **2 questions**, track the score, and print the final score.

4. Create a **dictionary for 3 contacts** with keys as names and values as phone numbers. Print all names.

5. Ask the user for **first and last name** and print in **uppercase** using a function.

---

# **Answer Key – Day 2 Quiz**

### **Part 1: MCQs**

1. **b) Tuple**
2. **b) 8**
3. **b) string.replace(...) multiple times**
4. **d) Both b and c**
5. **c) Set**

---

### **Part 2: True/False**

1. True
2. False
3. True
4. True
5. True

---

### **Part 3: Short Answer / Code Output**

1. `False`
2. ```python
   ```

def greet_user():
name = input("Enter your name: ")
print(f"Hello, {name}!")

````
3. `{1, 2, 3, 4, 5}` (order may vary)  
4. Example:
```python
cities = ("Paris", "Tokyo", "New York", "London")
# cities[0] = "Berlin"  # Error: tuples are immutable
````

5. `Alice will be 30 in 5 years.`

---

### **Part 4: File Handling & CSV**

1. ```python
   ```

with open("quotes.txt", "w") as f:
f.write("Quote 1\nQuote 2\nQuote 3\n")

````
2. ```python
with open("quotes.txt", "r") as f:
    for line in f:
        print(line.strip())
````

3. ```python
   ```

import csv
with open("contacts.csv", "w", newline="") as f:
writer = csv.writer(f)
writer.writerow(["Name", "Phone", "Email"])
writer.writerow(["Alice", "123", "[alice@example.com](mailto:alice@example.com)"])
writer.writerow(["Bob", "456", "[bob@example.com](mailto:bob@example.com)"])
writer.writerow(["Charlie", "789", "[charlie@example.com](mailto:charlie@example.com)"])

````
4. ```python
with open("contacts.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
````

5. Using `with` automatically **closes the file** even if an error occurs, preventing data loss.

---

### **Part 5: Mini Project / Problem Solving**

1. ```python
   ```

def calculate_area(width, height):
return width * height

````
2. ```python
movies = ["Inception", "Avatar", "Titanic", "Matrix", "Interstellar"]
print(movies)
````

3. ```python
   ```

questions = [{"q":"2+2=", "a":"4"}, {"q":"Capital of France?", "a":"Paris"}]
score = 0
for q in questions:
ans = input(q["q"] + " ")
if ans.strip().lower() == q["a"].lower():
score += 1
print(f"Final score: {score}/{len(questions)}")

````
4. ```python
contacts = {"Alice":"123", "Bob":"456", "Charlie":"789"}
print(list(contacts.keys()))
````

5. ```python
   ```

def print_upper_name():
first = input("First name: ")
last = input("Last name: ")
print(f"{first} {last}".upper())

print_upper_name()

```

