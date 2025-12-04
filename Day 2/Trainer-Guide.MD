# Weekend Python Crash Course 🐍  
## Day 2 Trainer Guide – Functions, Data Structures & File Handling

---

## 🕒 Schedule Overview (Day 2)

| Time | Topic | Format |
|------|-------|--------|
| 9:00 – 9:30 AM | Functions – Defining and Using | Presentation + Demo |
| 9:30 – 10:30 AM | Function Exercises | Lab Exercises / Pair Programming |
| 10:30 – 11:00 AM | Break | — |
| 11:00 – 12:30 PM | Lists, Tuples, Sets, Dictionaries | Presentation + Lab Exercises |
| 12:30 – 1:30 PM | Lunch | — |
| 1:30 – 2:30 PM | Strings – Methods & f-Strings | Demo + Exercises |
| 2:30 – 3:15 PM | File Handling – Text & CSV | Demo + Lab Exercises |
| 3:15 – 4:30 PM | Mini Projects | Independent Coding / Instructor Support |
| 4:30 – 5:00 PM | Wrap-Up & Q&A | Discussion / Tips |

---

## 📝 Instructor Notes

### **Functions**
- Emphasize reusability and reducing repetition.  
- Show examples of functions with/without return values.  
- Explain **local vs global variables** with simple examples.

**Tips for Trainers:**
- Encourage learners to test each function independently.  
- Provide hints rather than full solutions immediately.  

---

### **Data Structures**
- **Lists:** mutable, ordered; useful for storing collections.  
- **Tuples:** immutable, fixed data.  
- **Sets:** unique, unordered elements; great for removing duplicates.  
- **Dictionaries:** key-value mapping; ideal for contact lists.  

**Key Points:**
- Demonstrate adding/removing elements for each structure.  
- Encourage learners to think about which structure fits their use case.  

---

### **Strings**
- Highlight common string methods: `upper()`, `lower()`, `replace()`, `len()`.  
- Demonstrate f-strings for clean formatting.  
- Encourage using string methods in exercises.  

---

### **File Handling**
- **Text files:** show `open()` with modes `"w"` and `"r"`.  
- **CSV files:** use `csv` module for reading/writing.  
- Stress saving files in project folder.  
- Provide live demonstration of writing, reading, and printing file content.  

---

### **Mini Projects**
- **Contact Manager:** dictionary + CSV for storage.  
- **Quiz Game:** list of questions and answers, track score.  
- Encourage customization: add more fields, questions, or features.  

---

## ✅ Exercise Solutions (Examples)

### Functions
```python
def square(number):
    return number ** 2

def greet_user():
    name = input("Enter your name: ")
    print(f"Hello, {name}!")

def is_even(number):
    return number % 2 == 0

def calculate_area(width, height):
    return width * height

import random
def roll_dice():
    print(random.randint(1,6))
````

### Lists, Tuples, Sets, Dictionaries

```python
# List
favorite_movies = ["Inception", "Matrix", "Titanic", "Avatar", "Interstellar"]
favorite_movies.append("Joker")
print(favorite_movies[0], favorite_movies[-1])

# Tuple
cities = ("Paris", "Tokyo", "New York")
# cities[0] = "London"  # Error: tuples are immutable

# Set
numbers = {1, 2, 3, 3, 4}
numbers.add(5)
numbers.remove(2)
print(numbers)

# Dictionary
contacts = {"Alice": "12345", "Bob": "67890"}
contacts["Charlie"] = "54321"
print(contacts.keys())
```

### Strings

```python
first = input("First name: ").upper()
last = input("Last name: ").upper()
full_name = first + " " + last
print(full_name)

text = "Python is fun"
for vowel in "aeiou":
    text = text.replace(vowel, "*")
print(text)

name = "Alice"
age = 25
color = "Blue"
print(f"{name} is {age} years old and her favorite color is {color}.")
```

### File Handling

```python
# Text file
with open("quotes.txt", "w") as f:
    f.write("Line 1\nLine 2\nLine 3\nLine 4\nLine 5\n")

with open("quotes.txt", "r") as f:
    print(f.read())

# CSV file
import csv
with open("contacts.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Phone", "Email"])
    writer.writerow(["Alice", "12345", "alice@example.com"])
    writer.writerow(["Bob", "67890", "bob@example.com"])
    writer.writerow(["Charlie", "54321", "charlie@example.com"])

with open("contacts.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)
```

---

## 💡 Tips for Trainers

* Walk around during lab sessions; assist learners as needed.
* Encourage experimentation: let learners modify exercises.
* Provide instant feedback and explain errors.
* Keep the atmosphere fun and interactive.

