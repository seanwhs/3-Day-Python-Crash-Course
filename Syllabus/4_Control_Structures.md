# Control Structures

Python Control Structures include if-else statements, loops (for and while loops), and conditional expressions. These structures allow programmers to control the flow of a program based on certain conditions or criteria.

1. if-else statements:
If-else statements allow a program to perform different actions based on whether a condition is true or false. The basic syntax for an if-else statement in Python is as follows:

```
if condition:
    # code to execute if condition is True
else:
    # code to execute if condition is False
```

1. Loops:
Loops are used to repeatedly execute a block of code until a specific condition is met. Python supports two types of loops: for loops and while loops.
- For loops: For loops are used to iterate over a sequence of elements (such as a list or a string) for a specified number of times. The basic syntax for a for loop in Python is as follows:

```
for item in sequence:
    # code to execute for each item in sequence
```

- While loops: While loops are used to repeatedly execute a block of code as long as a condition is true. The basic syntax for a while loop in Python is as follows:

```
while condition:
    # code to execute as long as condition is True
```

1. Conditional expressions:
Conditional expressions, also known as ternary operators, are a way to write if-else statements in a single line. The basic syntax for a conditional expression in Python is as follows:

```
value_if_true if condition else value_if_false
```

For example, the following code prints "Even" if a number is even and "Odd" if it is odd, using a conditional expression:

```
num = 5
print("Even" if num % 2 == 0 else "Odd")
```
