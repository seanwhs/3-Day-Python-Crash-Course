# Functions

Functions are a way of organizing and reusing code in Python. A function is a block of code that performs a specific task and returns a result. It takes one or more inputs as arguments, processes them, and returns a result.

A function in Python is defined using the **`def`** keyword, followed by the function name, and the parameters in parentheses. The function code is indented under the function definition.

```
def function_name(parameter1, parameter2, ...):
    # Function code
    return result
```

Here, **`parameter1`**, **`parameter2`**, ... are the input parameters that are passed to the function. The **`return`** statement is used to return a value from the function.

Python provides several built-in functions, such as **`print()`**, **`len()`**, **`max()`**, **`min()`**, etc. You can also create your own functions using the **`def`** keyword.

Functions in Python can be categorized into two types:

1. Built-in Functions
2. User-defined Functions

Built-in functions are those functions that are provided by Python itself, and you can use them directly in your program. On the other hand, user-defined functions are those functions that you define yourself, and you can use them repeatedly in your program.

Python functions can also have optional parameters, which are known as default parameters. Default parameters are used to provide a default value to the parameter if no value is passed to the function.

Python also supports anonymous functions, which are known as lambda functions. Lambda functions are small, one-line functions that can take any number of arguments, but can only have one expression.

```
lambda arguments: expression
```

Lambda functions are mainly used when you need a small function for a short period of time, and you don't want to define a separate function for it.

In summary, functions are an essential part of Python programming. They allow you to organize your code, make it more readable, and reuse it. You can create your own functions, use built-in functions, and even use lambda functions for short tasks.

Here are some examples of functions in Python:

Example 1: A function that takes two numbers as input and returns their sum.

```
def add_numbers(num1, num2):
    sum = num1 + num2
    return sum

result = add_numbers(10, 20)
print(result)   # Output: 30
```

Example 2: A function that checks if a number is even or odd.

```
def even_or_odd(num):
    if num % 2 == 0:
        return "Even"
    else:
        return "Odd"

result = even_or_odd(5)
print(result)   # Output: Odd
```

Example 3: A function that calculates the area of a rectangle.

```
def calculate_area(length, width):
    area = length * width
    return area

result = calculate_area(5, 10)
print(result)   # Output: 50
```

Example 4: A function with default parameters.

```
def greet(name, message="Hello"):
    print(message, name)

greet("John")                   # Output: Hello John
greet("Mary", "Hi")             # Output: Hi Mary
```

Example 5: A lambda function that multiplies two numbers.

```
multiply = lambda x, y: x * y
result = multiply(10, 5)
print(result)   # Output: 50
```
