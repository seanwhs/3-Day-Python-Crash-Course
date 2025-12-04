# Weekend Python Crash Course 🐍  
## Day 1 Trainer Guide – Python Basics & Core Concepts

---

## 🕒 Schedule Overview (Day 1)

| Time | Topic | Format |
|------|-------|--------|
| 9:00 – 9:30 AM | Introduction to Python & Course Objectives | Presentation / Discussion |
| 9:30 – 10:30 AM | Setting up Python & IDE | Demo / Hands-on |
| 10:30 – 11:00 AM | Break | — |
| 11:00 – 12:30 PM | Variables, Data Types, and Basic Operators | Presentation + Lab Exercises |
| 12:30 – 1:30 PM | Lunch | — |
| 1:30 – 3:00 PM | Input/Output and If/Else Control Flow | Lab Exercises / Pair Programming |
| 3:00 – 3:15 PM | Break | — |
| 3:15 – 4:30 PM | Loops (`for`, `while`) + Mini Exercises | Lab Exercises / Guided Coding |
| 4:30 – 5:00 PM | End-of-Day Mini Project | Independent Coding / Instructor Support |
| 5:00 – 5:15 PM | Wrap-Up & Q&A | Discussion / Tips |

---

## 📝 Instructor Notes

### **Introduction to Python**
- Emphasize readability, versatility, and popularity.  
- Highlight career uses: web dev, data science, automation, etc.  
- Encourage learners to ask questions and experiment.

### **Setting up Python & IDE**
- Show step-by-step installation (Python + IDE).  
- Demonstrate running a script and REPL.  
- Tip: Ensure everyone can run `print("Hello Python!")` before moving on.  

### **Variables & Data Types**
- Explain each type with examples.  
- Discuss mutability (lists vs tuples) and type conversion.  
- Common pitfalls: mixing data types without casting.

**Key Points to Emphasize:**
- Variable names must start with a letter or underscore.  
- Use descriptive names for clarity.  

### **Basic Operators**
- Walk through arithmetic operators with examples.  
- Explain integer vs float division.  
- Use simple, relatable examples (e.g., age calculation, price total).  

### **Input/Output**
- Stress that `input()` always returns a string; use `int()` or `float()` when needed.  
- Encourage testing small snippets before combining into a program.  

### **If / Else Control Flow**
- Show nested `if` statements if time permits.  
- Explain logical operators (`and`, `or`, `not`).  
- Provide real-life examples (age checks, grading system).  

### **Loops**
- Demonstrate both `for` and `while` loops.  
- Highlight termination conditions for `while` loops to avoid infinite loops.  
- Encourage learners to trace loops on paper first.  

### **End-of-Day Mini Project**
- Guide learners step by step if needed but let them attempt independently.  
- Encourage creativity: change text, add extra calculations.  

---

## 💡 Tips for Trainers
- Walk around during lab sessions; offer help but let learners try first.  
- Encourage pair programming for collaborative problem-solving.  
- Use slides as prompts, but show live coding examples.  
- Remind learners to save their work often.  
- Provide immediate feedback on exercises and mini-projects.  

---

## ✅ Exercise Solutions

### Exercise 1: Hello Python
```python
print("Hello, Alice!")
print("You are 25 years old.")
print("Welcome to Python!")
````

### Exercise 2: Variables & Data Types

```python
your_name = "Alice"
your_age = 25
favorite_number = 7.5
print(your_name, your_age, favorite_number)
print(f"{your_name} is {your_age} years old and her favorite number is {favorite_number}")
```

### Exercise 3: Basic Operators

```python
a = 10
b = 3
print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a % b)
# Bonus: Area of rectangle
width = 5
height = 7
area = width * height
print(area)
```

### Exercise 4: Input/Output

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
print(f"Hello {name}! You are {age} years old.")
# Bonus: sum of two numbers
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))
print(num1 + num2, num1 - num2, num1 * num2, num1 / num2)
```

### Exercise 5: If/Else

```python
num = int(input("Enter a number: "))
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

### Exercise 6: Loops

```python
# For loop
for i in range(1, 11):
    print(i)
for i in range(2, 21, 2):
    print(i)
# While loop
count = 0
while count < 5:
    print(count)
    count += 1
# Bonus: Number guessing game
import random
number = random.randint(1,10)
guess = 0
while guess != number:
    guess = int(input("Guess the number (1-10): "))
    if guess < number:
        print("Too low!")
    elif guess > number:
        print("Too high!")
print("Correct!")
```

### End-of-Day Mini Project

```python
for _ in range(3):
    name = input("Enter your name: ")
    age = int(input("Enter your age: "))
    fav_num = float(input("Enter your favorite number: "))
    print(f"Hello {name}! In 5 years, you will be {age + 5}. Your favorite number doubled is {fav_num * 2}.")
```

---

## 🎯 Key Takeaways for Trainers

* Emphasize hands-on practice — coding is learned by doing.
* Encourage learners to explore variations of examples.
* Maintain a fun, supportive, and interactive environment.


