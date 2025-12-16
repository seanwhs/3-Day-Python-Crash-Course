# Operators Exercises:

Exercise 1: Write a program to calculate the area of a rectangle. The length and width of the rectangle should be input by the user.

```
length = float(input("Enter the length of the rectangle: "))
width = float(input("Enter the width of the rectangle: "))

area = length * width

print("The area of the rectangle is:", area)
```

Exercise 2: Write a program to convert temperature from Celsius to Fahrenheit. The temperature in Celsius should be input by the user.

```
celsius = float(input("Enter temperature in Celsius: "))

fahrenheit = (celsius * 9/5) + 32

print("Temperature in Fahrenheit:", fahrenheit)
```

Exercise 3: Write a program to calculate the sum of two numbers. The numbers should be input by the user.

```
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))

sum = num1 + num2

print("The sum of", num1, "and", num2, "is:", sum)
```

Exercise 4: Write a program to check if a number is positive, negative, or zero. The number should be input by the user.

```
num = float(input("Enter a number: "))

if num > 0:
    print(num, "is positive")
elif num < 0:
    print(num, "is negative")
else:
    print(num, "is zero")
```

Exercise 5: Write a program to check if a number is even or odd. The number should be input by the user.

```
num = int(input("Enter a number: "))

if num % 2 == 0:
    print(num, "is even")
else:
    print(num, "is odd")
```

Exercise 6: Write a program to calculate the average of three numbers. The numbers should be input by the user.

```
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))
num3 = float(input("Enter the third number: "))

avg = (num1 + num2 + num3) / 3

print("The average of", num1, ",", num2, ", and", num3, "is:", avg)
```

Exercise 7: Write a program to check if a year is a leap year. The year should be input by the user.

```
year = int(input("Enter a year: "))

if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print(year, "is a leap year")
        else:
            print(year, "is not a leap year")
    else:
        print(year, "is a leap year")
else:
    print(year, "is not a leap year")
```

Exercise 8: Write a program to check if a number is a palindrome. The number should be input by the user.

```
num = input("Enter a number: ")

if num == num[::-1]:
    print(num, "is a palindrome")
else:
    print(num, "is not a palindrome")
```

Exercise 9: Write a program to find the sum of all the numbers in a list.

```
nums = [3, 5, 8, 13, 21]
sum = 0

for num in nums:
    sum += num

print("The sum of the numbers is:", sum)
```

Exercise 10: Write a program to find the largest number in a list.

```
nums = [45, 23, 67, 89, 12]
max_num = nums[0]

for num in nums:
    if num > max_num:
        max_num = num

print("The largest number in the list is:", max_num)
```

Exercise 11: Write a program to check if a given number is prime or not.

```
num = int(input("Enter a number: "))
is_prime = True

if num < 2:
    is_prime = False

for i in range(2, num):
    if num % i == 0:
        is_prime = False
        break

if is_prime:
    print(num, "is a prime number")
else:
    print(num, "is not a prime number")
```

Exercise 12: Write a program to find the factorial of a given number.

```
num = int(input("Enter a number: "))
factorial = 1

if num < 0:
    print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
    print("The factorial of 0 is 1")
else:
    for i in range(1, num + 1):
        factorial *= i
    print("The factorial of", num, "is", factorial)
```

Exercise 12: Write a program to print the Fibonacci sequence up to a given number.

```
num = int(input("Enter a number: "))
fibonacci = [0, 1]

while fibonacci[-1] < num:
    fibonacci.append(fibonacci[-1] + fibonacci[-2])

print("The Fibonacci sequence up to", num, "is:", fibonacci[:-1])
```

Exercise 13: Write a program to remove duplicates from a list.

```
nums = [2, 4, 6, 2, 8, 4, 9, 2]
unique_nums = []

for num in nums:
    if num not in unique_nums:
        unique_nums.append(num)

print("The list with duplicates removed is:", unique_nums)
```

Exercise 14: Write a program to find the second largest number in a list.

```
nums = [45, 23, 67, 89, 12]
max_num = nums[0]
second_max = nums[0]

for num in nums:
    if num > max_num:
        second_max = max_num
        max_num = num
    elif num > second_max and num != max_num:
        second_max = num

print("The second largest number in the list is:", second_max)
```

Exercise 15: Write a program to check if a given string is a palindrome or not.

```
string = input("Enter a string: ")
reversed_string = string[::-1]

if string == reversed_string:
    print(string, "is a palindrome")
else:
    print(string, "is not a palindrome")
```

Exercise 16: Write a program to count the number of vowels in a given string.

```
string = input("Enter a string: ")
vowels = "aeiou"
count = 0

for char in string:
    if char.lower() in vowels:
        count += 1

print("The number of vowels in the string is:", count)
```

Exercise 17: Write a program to find the GCD (greatest common divisor) of two numbers.

```
def gcd(a, b):
    if b == 0:
        return a
    else:
        return gcd(b, a % b)

num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))

print("The GCD of", num1, "and", num2, "is", gcd(num1, num2))
```
