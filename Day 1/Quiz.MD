# 🐍 Day 1 Quiz – Python Basics & Core Concepts

## **Part 1: Multiple Choice Questions (MCQs)**

1. Which of the following is a **valid variable name** in Python?
   a) `1name`
   b) `user_name`
   c) `user-name`
   d) `name!`

2. What will be the output of the following code?

```python
a = 5
b = 2
print(a / b)
```

a) `2`
b) `2.5`
c) `2.0`
d) `TypeError`

3. Which of the following data types is **immutable**?
   a) List
   b) Tuple
   c) Set
   d) Dictionary

4. What does the `input()` function return?
   a) Integer
   b) Float
   c) String
   d) Boolean

5. Which operator is used for **modulus (remainder)** in Python?
   a) `%`
   b) `//`
   c) `**`
   d) `/`

---

## **Part 2: True/False**

1. `while` loops always run a fixed number of times. (True / False)
2. In Python, `elif` is used after an `if` statement to check another condition. (True / False)
3. Variables must always be declared before use in Python. (True / False)
4. Python is case-sensitive. (True / False)
5. The `print()` function can accept multiple arguments separated by commas. (True / False)

---

## **Part 3: Short Answer / Code Output**

1. What will be the output of this code?

```python
x = 10
y = 3
print(x % y)
```

2. Write a Python statement to **ask the user for their name** and print:

```
Hello <name>!
```

3. What will this code print?

```python
for i in range(2, 11, 2):
    print(i, end=' ')
```

4. Write a Python expression to **calculate the area of a rectangle** with width = 8 and height = 5.

5. Predict the output:

```python
age = int(input("Enter your age: "))
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

*(Assume the user enters `15`.)*

---

## **Part 4: Problem-Solving / Mini Coding**

1. Write a Python program that asks the user for **two numbers** and prints their **sum, difference, product, and quotient**.

2. Create a program that asks the user for a number and prints:

* `"Positive"` if the number > 0
* `"Negative"` if the number < 0
* `"Zero"` if the number = 0

3. Write a **while loop** that prints numbers from 1 to 5.

4. Modify the number guessing game so that it gives the user **3 attempts only** to guess a number between 1 and 10.

5. End-of-Day Challenge: Write a program that asks for a user’s **name, age, and favorite number** and prints:

```
Hello <name>! In 5 years, you will be <age+5>. Your favorite number doubled is <favorite_number*2>.
```

---

# **Answer Key – Day 1 Quiz**

### **Part 1: MCQs**

1. **b) `user_name`**
2. **b) `2.5`**
3. **b) Tuple**
4. **c) String**
5. **a) `%`**

---

### **Part 2: True/False**

1. False
2. True
3. False
4. True
5. True

---

### **Part 3: Short Answer / Code Output**

1. `1`
2. ```python
   ```

name = input("Enter your name: ")
print(f"Hello {name}!")

````
3. `2 4 6 8 10 `  
4. ```python
width = 8
height = 5
area = width * height
print(area)  # Output: 40
````

5. `Minor`

---

### **Part 4: Problem-Solving / Mini Coding**

**1. Two numbers – arithmetic operations**

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

print("Sum:", num1 + num2)
print("Difference:", num1 - num2)
print("Product:", num1 * num2)
if num2 != 0:
    print("Quotient:", num1 / num2)
else:
    print("Cannot divide by zero")
```

**2. Positive/Negative/Zero**

```python
num = float(input("Enter a number: "))
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

**3. While loop 1–5**

```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

**4. Number guessing game (3 attempts)**

```python
import random
secret_number = random.randint(1, 10)
attempts = 0
max_attempts = 3

while attempts < max_attempts:
    guess = int(input("Guess the number (1-10): "))
    attempts += 1
    if guess == secret_number:
        print("Correct!")
        break
    elif guess < secret_number:
        print("Too low!")
    else:
        print("Too high!")
else:
    print(f"Out of attempts! The number was {secret_number}.")
```

**5. End-of-Day Challenge**

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
favorite_number = float(input("Enter your favorite number: "))

print(f"Hello {name}! In 5 years, you will be {age + 5}. "
      f"Your favorite number doubled is {favorite_number * 2}.")
```

