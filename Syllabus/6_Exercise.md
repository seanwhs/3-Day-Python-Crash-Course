# Modules - Exercises

1. Create a module named "math_ops" that contains functions for addition, subtraction, multiplication, and division.

```
pythonCopy code
# math_ops.py

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    return x / y

```

1. Import the "math_ops" module and use its functions to perform the following operations:
    - Add 5 and 10.
    - Subtract 7 from 20.
    - Multiply 4 and 9.
    - Divide 25 by 5.

```
pythonCopy code
import math_ops

print(math_ops.add(5, 10))
print(math_ops.subtract(20, 7))
print(math_ops.multiply(4, 9))
print(math_ops.divide(25, 5))

```

Output:

```
Copy code
15
13
36
5.0

```

1. Create a package named "shapes" that contains two modules: "circle" and "rectangle". The "circle" module should have functions for calculating the area and circumference of a circle, and the "rectangle" module should have functions for calculating the area and perimeter of a rectangle.

```
pythonCopy code
# shapes/circle.py

import math

def area(radius):
    return math.pi * radius ** 2

def circumference(radius):
    return 2 * math.pi * radius

# shapes/rectangle.py

def area(length, width):
    return length * width

def perimeter(length, width):
    return 2 * (length + width)

```

1. Import the "shapes" package and use its modules to calculate the following:
    - The area and circumference of a circle with radius 5.
    - The area and perimeter of a rectangle with length 10 and width 5.

```
pythonCopy code
import shapes.circle as circle
import shapes.rectangle as rectangle

print(circle.area(5))
print(circle.circumference(5))
print(rectangle.area(10, 5))
print(rectangle.perimeter(10, 5))

```

Output:

```
Copy code
78.53981633974483
31.41592653589793
50
30

```

1. Create a virtual environment named "myenv".

```
pythonCopy code
python -m venv myenv

```

1. Activate the "myenv" virtual environment.

```
pythonCopy code
source myenv/bin/activate

```

1. Install the "numpy" package in the "myenv" virtual environment.

```
pythonCopy code
pip install numpy

```

1. Write a Python module that includes a function to calculate the area of a circle. Import the module into a new Python script and use the function to calculate the area of a circle with a radius of 5.

```
pythonCopy code
# circle.py
import math

def calculate_area(radius):
    area = math.pi * radius ** 2
    return area

# main.py
import circle

radius = 5
area = circle.calculate_area(radius)
print(f"The area of a circle with a radius of {radius} is {area:.2f}")

```

Output:

```
csharpCopy code
The area of a circle with a radius of 5 is 78.54

```

1. Create a Python module named **`colors`** that defines a list of five colors. Import the module into a new Python script and print each color.

```
pythonCopy code
# colors.py
color_list = ["red", "green", "blue", "yellow", "orange"]

# main.py
import colors

for color in colors.color_list:
    print(color)

```

Output:

```
Copy code
red
green
blue
yellow
orange

```

1. Create a Python module named **`utils`** that includes a function **`reverse_string(string)`** that returns the input string in reverse order. Import the module into a new Python script and use the function to reverse the string "Hello, World!".

```
pythonCopy code
# utils.py
def reverse_string(string):
    return string[::-1]

# main.py
import utils

string = "Hello, World!"
reversed_string = utils.reverse_string(string)
print(reversed_string)

```

Output:

```
diffCopy code
!dlroW ,olleH

```
