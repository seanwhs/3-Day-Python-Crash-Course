# Modules

Modules in Python are separate files containing Python code that can be imported into other Python programs. They can be considered as libraries of Python code that can be used to enhance the functionality of a program. The advantage of using modules is that it promotes code reuse and helps to keep the code organized and easy to maintain.

Python comes with a large number of built-in modules, such as **`math`**, **`random`**, and **`os`**, which provide functionality for common tasks such as mathematical operations, generating random numbers, and working with the operating system.

In addition to the built-in modules, Python also allows you to create your own modules by defining functions and variables in a separate file and importing them into your program.

To use a module in Python, you can import it using the **`import`** keyword followed by the name of the module. You can then use the functions and variables defined in the module using the dot notation, such as **`module_name.function_name()`**.

There are different ways to import modules in Python, such as importing the entire module, importing specific functions or variables from a module, or giving a module a different name when importing it.

Modules are an important concept in Python programming and can greatly enhance the functionality and organization of your code.

Here are some examples of how to use modules in Python:

Example 1: Using the **`math`** module to perform mathematical operations

```
import math

# Calculate the square root of a number
x = math.sqrt(25)
print(x)

# Calculate the value of pi
pi = math.pi
print(pi)

# Calculate the sine of an angle
angle = math.radians(45)
sin = math.sin(angle)
print(sin)
```

Output:

```
5.0
3.141592653589793
0.7071067811865475
```

Example 2: Using the **`random`** module to generate random numbers

```
import random

# Generate a random integer between 1 and 10
x = random.randint(1, 10)
print(x)

# Generate a random float between 0 and 1
y = random.random()
print(y)

# Shuffle a list of items
my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)
print(my_list)
```

Output:

```
7
0.4214255146845926
[4, 3, 2, 5, 1]
```

Example 3: Creating and importing a custom module

In a separate file named **`my_module.py`**, define a function that prints a message:

```
def my_function():
    print("Hello, world!")
```

In the main program, import the **`my_module`** module and use the **`my_function`** function:

```
import my_module

my_module.my_function()
```

Output:

```
Hello, world!
```

<aside>
💡

**Modules vs Packages**

In Python, modules and packages are two related concepts but they have different meanings.

A module is a single file containing Python definitions and statements, which can be imported and used in other Python programs. For example, the built-in **`math`** module contains mathematical functions and constants.

A package, on the other hand, is a collection of related modules that are organized in a directory hierarchy. A package can have sub-packages and modules, and can also contain files other than Python modules. A package is identified by a directory that contains a special file called **`__init__.py`**. The **`__init__.py`** file can be empty, or it can contain initialization code for the package.

Here's an example of a package structure:

```
my_package/
    __init__.py
    module1.py
    module2.py
    subpackage/
        __init__.py
        module3.py
```

To use a module or a package in your Python program, you can import it using the **`import`** statement. For example:

```
import math
import my_package.module1
import my_package.subpackage.module3
```

In the first line, we import the built-in **`math`** module. In the second line, we import a module named **`module1`** from a package named **`my_package`**. In the third line, we import a module named **`module3`** from a subpackage named **`subpackage`**, which is inside the **`my_package`** package.

</aside>
