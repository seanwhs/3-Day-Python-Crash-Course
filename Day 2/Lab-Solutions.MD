# 🐍 Day 2 Lab Solutions

## 🏁 Exercise 1: Functions

```python
# functions_examples.py
import random

# 1. Square of a number
def square(number):
    return number ** 2

# 2. Greet user
def greet_user():
    name = input("Enter your name: ")
    print(f"Hello, {name}!")

# 3. Check if even
def is_even(number):
    return number % 2 == 0

# 4. Area of rectangle
def calculate_area(width, height):
    return width * height

# Bonus: Roll dice
def roll_dice():
    result = random.randint(1, 6)
    print(f"You rolled a {result}")
```

---

## 🔢 Exercise 2: Lists, Tuples, Sets, Dictionaries

```python
# lists_tuples_sets_dicts.py

# --- Lists ---
favorite_movies = ["Inception", "Avatar", "Titanic", "The Matrix", "Interstellar"]
favorite_movies.append("Joker")
print("All movies:", favorite_movies)
print("First movie:", favorite_movies[0])
print("Last movie:", favorite_movies[-1])

# --- Tuples ---
cities = ("Paris", "Tokyo", "New York")
# Tuples are immutable; attempting to modify will raise an error
# cities[0] = "London"  # Uncommenting this will cause an error

# --- Sets ---
numbers = {1, 2, 3, 3, 4}  # Duplicate '3' removed automatically
numbers.add(5)
print("Set after adding 5:", numbers)
numbers.remove(2)
print("Set after removing 2:", numbers)

# --- Dictionaries ---
contacts = {"Alice": "123-456-7890", "Bob": "987-654-3210"}
contacts["Charlie"] = "555-555-5555"
print("Contact names:", list(contacts.keys()))
```

---

## 🛠 Exercise 3: Strings

```python
# strings_examples.py

# 1. Uppercase name
first_name = input("Enter first name: ")
last_name = input("Enter last name: ")
full_name = f"{first_name} {last_name}".upper()
print("Full name in uppercase:", full_name)

# 2. Replace vowels with '*'
text = "Hello World"
vowels = "aeiouAEIOU"
for vowel in vowels:
    text = text.replace(vowel, "*")
print("Text with vowels replaced:", text)

# 3. f-string formatting
name = "Alice"
age = 25
favorite_color = "Blue"
print(f"{name} is {age} years old and her favorite color is {favorite_color}.")
```

---

## 📄 Exercise 4: File Handling

### Text Files

```python
# file_handling_text.py

# 1. Create and write quotes
quotes = [
    "The best way to get started is to quit talking and begin doing.",
    "Don't let yesterday take up too much of today.",
    "It's not whether you get knocked down, it's whether you get up.",
    "If you are working on something exciting, it will keep you motivated.",
    "Success is not in what you have, but who you are."
]

with open("quotes.txt", "w") as f:
    for quote in quotes:
        f.write(quote + "\n")

# 2. Read and print quotes
with open("quotes.txt", "r") as f:
    for line in f:
        print(line.strip())
```

### CSV Files

```python
# file_handling_csv.py
import csv

# 1. Create CSV file
with open("contacts.csv", "w", newline="") as csvfile:
    writer = csv.DictWriter(csvfile, fieldnames=["Name", "Phone", "Email"])
    writer.writeheader()
    writer.writerow({"Name": "Alice", "Phone": "123-456", "Email": "alice@example.com"})
    writer.writerow({"Name": "Bob", "Phone": "987-654", "Email": "bob@example.com"})
    writer.writerow({"Name": "Charlie", "Phone": "555-555", "Email": "charlie@example.com"})

# 2. Read CSV file
with open("contacts.csv", "r") as csvfile:
    reader = csv.DictReader(csvfile)
    for row in reader:
        print(row)
```

---

## ✅ Mini Project Solutions

### Project 1: Contact Manager

```python
# contact_manager.py
import csv

contacts = {}

# Load contacts from CSV if exists
try:
    with open("contacts.csv", "r") as csvfile:
        reader = csv.DictReader(csvfile)
        for row in reader:
            contacts[row["Name"]] = {"Phone": row["Phone"], "Email": row["Email"]}
except FileNotFoundError:
    pass

def add_contact():
    name = input("Enter name: ")
    phone = input("Enter phone: ")
    email = input("Enter email: ")
    contacts[name] = {"Phone": phone, "Email": email}
    print(f"Contact {name} added!")

def view_contacts():
    for name, info in contacts.items():
        print(f"{name}: Phone={info['Phone']}, Email={info['Email']}")

def search_contact():
    name = input("Enter name to search: ")
    if name in contacts:
        info = contacts[name]
        print(f"{name}: Phone={info['Phone']}, Email={info['Email']}")
    else:
        print(f"{name} not found.")

# Example menu
while True:
    print("\n1. Add contact\n2. View contacts\n3. Search contact\n4. Exit")
    choice = input("Choose an option: ")
    if choice == "1":
        add_contact()
    elif choice == "2":
        view_contacts()
    elif choice == "3":
        search_contact()
    elif choice == "4":
        # Save contacts to CSV before exit
        with open("contacts.csv", "w", newline="") as csvfile:
            writer = csv.DictWriter(csvfile, fieldnames=["Name", "Phone", "Email"])
            writer.writeheader()
            for name, info in contacts.items():
                writer.writerow({"Name": name, "Phone": info["Phone"], "Email": info["Email"]})
        print("Exiting. Contacts saved!")
        break
    else:
        print("Invalid choice.")
```

---

### Project 2: Quiz Game

```python
# quiz_game.py

questions = [
    {"question": "What is the capital of France?", "answer": "Paris"},
    {"question": "2 + 2 =", "answer": "4"},
    {"question": "What is Python's keyword to define a function?", "answer": "def"}
]

score = 0

for q in questions:
    user_answer = input(q["question"] + " ")
    if user_answer.strip().lower() == q["answer"].strip().lower():
        print("Correct!")
        score += 1
    else:
        print(f"Wrong! The correct answer is {q['answer']}")

print(f"Your final score is {score}/{len(questions)}")
```

---

### 💡 Notes for Trainers

* Emphasize **writing reusable functions** in Exercise 1.
* Encourage learners to **experiment with different data structures** to see their strengths and limitations.
* For file handling, reinforce the difference between **reading and writing files**, and the importance of **closing files** or using `with`.
* Mini projects help learners **integrate multiple concepts**: functions, loops, data structures, and file I/O.

