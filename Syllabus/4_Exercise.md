# Control Structures Exercises:

Exercise 1: Write a program that prints all the numbers from 1 to 10 using a for loop.

```
for i in range(1, 11):
    print(i)
```

Exercise 2: Write a program to find the sum of all the numbers from 1 to 100.

```
sum = 0

for i in range(1, 101):
    sum += i

print("The sum of all the numbers from 1 to 100 is:", sum)
```

Exercise 3: Write a program to print all the odd numbers from 1 to 20.

```
for i in range(1, 21):
    if i % 2 != 0:
        print(i)
```

Exercise 4: Write a program to print the multiplication table of a given number.

```
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(num, "x", i, "=", num * i)
```

Exercise 5: Write a program to find the factorial of a given number.

```
num = int(input("Enter a number: "))
factorial = 1

for i in range(1, num + 1):
    factorial *= i

print("The factorial of", num, "is", factorial)
```

Exercise 6: Write a program to print the Fibonacci series up to a given number.

```
num = int(input("Enter a number: "))

a, b = 0, 1
fibonacci = []

while b < num:
    fibonacci.append(b)
    a, b = b, a + b

print("The Fibonacci series up to", num, "is:", fibonacci)
```

Exercise 7: Write a program to find the prime numbers between 1 and 100.

```
for num in range(2, 101):
    for i in range(2, num):
        if (num % i) == 0:
            break
    else:
        print(num)
```

Exercise 8: Write a program to check if a given number is prime or not.

```
num = int(input("Enter a number: "))

for i in range(2, num):
    if (num % i) == 0:
        print(num, "is not a prime number")
        break
else:
    print(num, "is a prime number")
```
