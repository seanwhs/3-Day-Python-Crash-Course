# Exercises - Exception Handling

1. Write a program that asks the user to enter a number and then prints its square. If the user enters a non-numeric value, catch the exception and print an error message.

```
pythonCopy code
try:
    num = float(input("Enter a number: "))
    print("The square of", num, "is", num**2)
except ValueError:
    print("Error: Invalid input. Please enter a valid number.")

```

1. Write a program that reads two numbers from the user and performs division. If the user enters an invalid input or tries to divide by zero, catch the exception and print an error message.

```
pythonCopy code
try:
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
    result = num1 / num2
    print(num1, "divided by", num2, "is", result)
except ValueError:
    print("Error: Invalid input. Please enter a valid number.")
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")

```

1. Write a program that reads a file and prints its contents. If the file does not exist or cannot be opened, catch the exception and print an error message.

```
pythonCopy code
filename = input("Enter the file name: ")
try:
    with open(filename, 'r') as file:
        print(file.read())
except FileNotFoundError:
    print("Error: File not found.")
except IOError:
    print("Error: Could not open file.")

```

1. Write a program that asks the user to enter a password. If the password is less than 8 characters long, raise a custom exception with an error message.

```
pythonCopy code
class PasswordTooShortError(Exception):
    pass

password = input("Enter your password: ")
try:
    if len(password) < 8:
        raise PasswordTooShortError("Error: Password is too short.")
except PasswordTooShortError as e:
    print(e)
else:
    print("Password accepted.")

```

1. Write a program that reads a list of integers and calculates their average. If the list is empty, catch the exception and print an error message.

```
pythonCopy code
try:
    numbers = input("Enter a list of numbers, separated by commas: ")
    numbers = [int(n) for n in numbers.split(',')]
    avg = sum(numbers) / len(numbers)
    print("The average of the numbers is", avg)
except ZeroDivisionError:
    print("Error: Empty list.")
except ValueError:
    print("Error: Invalid input. Please enter a list of integers."

```

1. Write a program that takes two numbers as input from the user and divides the first number by the second number. Use a try-except block to catch the ZeroDivisionError if the second number entered is 0.

```
pythonCopy code
try:
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
    result = num1 / num2
    print("The result is:", result)
except ZeroDivisionError:
    print("Error: Cannot divide by zero")

```

1. Write a program that takes a list of numbers as input from the user and calculates the average of the numbers. Use a try-except block to catch any ValueErrors that may occur if the user enters non-numeric input.

```
pythonCopy code
try:
    nums = input("Enter a list of numbers separated by spaces: ").split()
    nums = [float(num) for num in nums]
    avg = sum(nums) / len(nums)
    print("The average is:", avg)
except ValueError:
    print("Error: Invalid input. Please enter only numbers.")

```

1. Write a program that takes a filename as input from the user and prints the contents of the file. Use a try-except block to catch any FileNotFoundError that may occur if the file does not exist.

```
pythonCopy code
try:
    filename = input("Enter the filename: ")
    with open(filename, 'r') as f:
        contents = f.read()
    print("The contents of the file are:")
    print(contents)
except FileNotFoundError:
    print("Error: File not found.")

```

1. Write a program that takes a string as input from the user and checks if it contains only letters. If the string contains non-letter characters, raise a ValueError with an appropriate error message. Use a try-except block to catch the ValueError and print the error message.

```
pythonCopy code
try:
    string = input("Enter a string: ")
    if not string.isalpha():
        raise ValueError("Error: String should only contain letters.")
    print("The string is:", string)
except ValueError as e:
    print(e)

```

1. Write a program that takes a list of numbers as input from the user and calculates the sum of the squares of the numbers. Use a try-except block to catch any TypeError that may occur if the user enters non-numeric input.

```
pythonCopy code
try:
    nums = input("Enter a list of numbers separated by spaces: ").split()
    nums = [float(num) for num in nums]
    sum_of_squares = sum(num**2 for num in nums)
    print("The sum of the squares is:", sum_of_squares)
except TypeError:
    print("Error: Invalid input. Please enter only numbers.")

```

I hope these exercises and their solutions help you practice and understand exception handling in Python better!
