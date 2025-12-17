## Introduction to Python:
Challenge 1: Write a Python program to print the message "Hello, World!" to the console.

```
pythonCopy code
print("Hello, World!")

```

Challenge 2: Write a Python program to calculate the sum of two numbers and print the result.

```
pythonCopy code
a = 5
b = 3
sum = a + b
print("The sum of", a, "and", b, "is", sum)

```

## Data Types and Variables:
Challenge 1: Write a Python program that prompts the user to enter their name and age and then prints out a message that says "Hello, [name]! You are [age] years old."

```
pythonCopy code
name = input("Enter your name: ")
age = int(input("Enter your age: "))
print("Hello,", name + "! You are", age, "years old.")

```

Challenge 2: Write a Python program that calculates the area of a circle given the radius and prints out the result.

```
pythonCopy code
import math
radius = float(input("Enter the radius of the circle: "))
area = math.pi * (radius ** 2)
print("The area of the circle is", area)

```

### Operators:
Challenge 1: Write a Python program that takes two numbers as input from the user and prints out the result of the modulus operation on those two numbers.

```
pythonCopy code
a = int(input("Enter the first number: "))
b = int(input("Enter the second number: "))
result = a % b
print("The result of", a, "mod", b, "is", result)

```

Challenge 2: Write a Python program that takes a sentence as input from the user and prints out the number of words in that sentence.

```
pythonCopy code
sentence = input("Enter a sentence: ")
word_count = len(sentence.split())
print("The sentence contains", word_count, "words.")

```

## Control Structures:
Challenge 1: Write a Python program that takes a number as input from the user and prints out whether that number is even or odd.

```
pythonCopy code
num = int(input("Enter a number: "))
if num % 2 == 0:
    print(num, "is even.")
else:
    print(num, "is odd.")

```

Challenge 2: Write a Python program that takes a list of numbers as input from the user and prints out the sum of those numbers.

```
pythonCopy code
num_list = [int(x) for x in input("Enter a list of numbers, separated by spaces: ").split()]
sum = 0
for num in num_list:
    sum += num
print("The sum of the numbers is", sum)

```

## Functions:
Challenge 1: Write a Python function that takes a string as input and returns the number of vowels in that string.

```
pythonCopy code
def count_vowels(string):
    count = 0
    vowels = "aeiouAEIOU"
    for char in string:
        if char in vowels:
            count += 1
    return count

string = input("Enter a string: ")
num_vowels = count_vowels(string)
print("The string contains", num_vowels, "vowels.")

```

1. Write a function that takes a list of integers as input and returns the sum of all the even numbers in the list.

```
pythonCopy code
def sum_even_numbers(numbers):
    even_numbers = [num for num in numbers if num % 2 == 0]
    return sum(even_numbers)

```

2. Write a function that takes two lists of integers as input and returns a new list containing the common elements of the two input lists.

```
arduinoCopy code
def common_elements(list1, list2):
    common = []
    for num in list1:
        if num in list2 and num not in common:
            common.append(num)
    return common

```

3. Write a function that takes a string as input and returns a dictionary containing the count of each character in the string.

```
cCopy code
def count_characters(string):
    char_count = {}
    for char in string:
        if char in char_count:
            char_count[char] += 1
        else:
            char_count[char] = 1
    return char_count

```

4. Write a function that takes a list of numbers as input and returns a new list containing only the numbers that are perfect squares.

```
arduinoCopy code
import math

def perfect_squares(numbers):
    squares = []
    for num in numbers:
        if math.sqrt(num) == int(math.sqrt(num)):
            squares.append(num)
    return squares

```

5. Write a function that takes a list of words as input and returns a new list containing only the words that are palindromes.

```
arduinoCopy code
def palindromes(words):
    palindromes = []
    for word in words:
        if word == word[::-1]:
            palindromes.append(word)
    return palindromes

```

6. Write a Python program to count the number of characters (character frequency) in a string.

```
pythonCopy code
def count_characters(string):
    # initialize a dictionary to store character frequency
    char_freq = {}

    # loop through each character in the string
    for char in string:
        # if the character is already in the dictionary, increment its count
        if char in char_freq:
            char_freq[char] += 1
        # otherwise, add the character to the dictionary with a count of 1
        else:
            char_freq[char] = 1

    # return the dictionary of character frequencies
    return char_freq

```

7. Write a Python program to find the largest and smallest elements in a list.

```
pythonCopy code
def find_extremes(lst):
    # initialize variables to store the largest and smallest elements
    largest = lst[0]
    smallest = lst[0]

    # loop through each element in the list
    for num in lst:
        # if the current element is larger than the largest, update the largest
        if num > largest:
            largest = num
        # if the current element is smaller than the smallest, update the smallest
        elif num < smallest:
            smallest = num

    # return the largest and smallest elements as a tuple
    return (largest, smallest)

```

8. Write a Python program to remove duplicates from a list.

```
pythonCopy code
def remove_duplicates(lst):
    # initialize an empty list to store the unique elements
    unique_lst = []

    # loop through each element in the list
    for num in lst:
        # if the current element is not in the unique list, add it
        if num not in unique_lst:
            unique_lst.append(num)

    # return the list of unique elements
    return unique_lst

```

9. Write a Python program to reverse a string.

```
pythonCopy code
def reverse_string(string):
    # initialize an empty string to store the reversed string
    reversed_string = ""

    # loop through each character in the string in reverse order
    for i in range(len(string)-1, -1, -1):
        # add the current character to the reversed string
        reversed_string += string[i]

    # return the reversed string
    return reversed_string

```

10. Write a Python program to find the factorial of a number.

```
pythonCopy code
def factorial(n):
    # if n is 0 or 1, return 1
    if n == 0 or n == 1:
        return 1

    # otherwise, use recursion to calculate the factorial
    else:
        return n * factorial(n-1)

```

11. Write a Python program to find the second largest element in a list.

```
pythonCopy code
def second_largest(lst):
    # initialize variables to store the largest and second largest elements
    largest = lst[0]
    second_largest = lst[0]

    # loop through each element in the list
    for num in lst:
        # if the current element is larger than the largest, update both variables
        if num > largest:
            second_largest = largest
            largest = num
        # otherwise, if the current element is larger than the second largest but smaller than the largest, update only the second largest
        elif num > second_largest and num != largest:
            second_largest = num

    # return the second largest element
    return second_largest

```

12. Write a Python function to find the second highest number in a list of integers.

```
pythonCopy code
def find_second_highest(numbers):
    highest = None
    second_highest = None
    for n in numbers:
        if highest is None or n > highest:
            second_highest = highest
            highest = n
        elif second_highest is None or n > second_highest:
            second_highest = n
    return second_highest

```

13. Write a Python function to calculate the sum of all the even numbers in a list.

```
pythonCopy code
def sum_even(numbers):
    total = 0
    for n in numbers:
        if n % 2 == 0:
            total += n
    return total

```

14. Write a Python function to check if a given string is a palindrome.

```
pythonCopy code
def is_palindrome(s):
    return s == s[::-1]

```

15. Write a Python program to find the most frequent element in a list.

```
pythonCopy code
from collections import Counter

def most_frequent(numbers):
    counter = Counter(numbers)
    return counter.most_common(1)[0][0]

```

16. Write a Python function to reverse a string word by word.

```
pythonCopy code
def reverse_words(s):
    words = s.split()
    words.reverse()
    return ' '.join(words)

```

17. Write a program that asks the user to input a string and returns the string in reverse order.

```
luaCopy code
string = input("Enter a string: ")
reverse_string = string[::-1]
print("The reverse of the string is:", reverse_string)

```

18. Write a program that takes in a list of integers and returns the sum of all even numbers in the list.

```
scssCopy code
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_sum = sum([num for num in numbers if num % 2 == 0])
print("The sum of all even numbers is:", even_sum)

```

19. Write a program that takes in a list of integers and returns the maximum and minimum numbers in the list.

```
scssCopy code
numbers = [5, 2, 9, 3, 8, 1, 7, 4, 6]
max_num = max(numbers)
min_num = min(numbers)
print("The maximum number is:", max_num)
print("The minimum number is:", min_num)

```

20. Write a program that takes in a string and checks if it is a palindrome (a word, phrase, or sequence that reads the same backward as forward).

```
luaCopy code
string = input("Enter a string: ")
reverse_string = string[::-1]
if string == reverse_string:
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")

```

21. Write a program that takes in a list of integers and returns a new list with only the unique numbers (i.e. numbers that only appear once in the original list).

```
scssCopy code
numbers = [5, 2, 9, 3, 8, 1, 7, 4, 6, 5, 8, 4]
unique_numbers = [num for num in numbers if numbers.count(num) == 1]
print("The unique numbers in the list are:", unique_numbers)

```

22. Write a program that takes in a list of strings and returns a new list with only the strings that have a length greater than 5.

```
goCopy code
strings = ["apple", "banana", "pear", "grapefruit", "kiwi", "orange"]
long_strings = [string for string in strings if len(string) > 5]
print("The strings with length greater than 5 are:", long_strings)

```

23. Write a program that takes in a list of dictionaries, where each dictionary represents a person with keys for "name" and "age", and returns the name of the oldest person.

```
pythonCopy code
people = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 20}
]
oldest_person = max(people, key=lambda x: x["age"])
print("The name of the oldest person is:", oldest_person["name"])

```

24. Write a program that takes in two lists of integers and returns a new list with only the common elements between the two lists.

```
scssCopy code
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
common_elements = [num for num in list1 if num in list2]
print("The common elements between the two lists are:", common_elements)

```

25. Write a Python program that takes a list of integers as input and returns a list containing only the even numbers.

```
arduinoCopy code
def get_even_numbers(numbers):
    even_numbers = []
    for num in numbers:
        if num % 2 == 0:
            even_numbers.append(num)
    return even_numbers

```

26. Write a Python program that takes two strings as input and returns True if they are anagrams (i.e., contain the same letters in a different order), or False otherwise.

```
pythonCopy code
def is_anagram(str1, str2):
    return sorted(str1) == sorted(str2)

```

27. Write a Python program that takes a list of strings as input and returns a list containing only the strings that have a length of 3 or greater and start with the letter "a".

```
cCopy code
def filter_strings(strings):
    filtered_strings = []
    for string in strings:
        if len(string) >= 3 and string[0] == 'a':
            filtered_strings.append(string)
    return filtered_strings

```

28. Write a Python program that takes a list of integers as input and returns the largest and smallest values in the list.

```
pythonCopy code
def get_min_max(numbers):
    if len(numbers) == 0:
        return None, None
    min_number = max_number = numbers[0]
    for num in numbers[1:]:
        if num < min_number:
            min_number = num
        elif num > max_number:
            max_number = num
    return min_number, max_number

```

1. Write a Python program that takes a list of strings as input and returns a dictionary where the keys are the strings and the values are their lengths.

```
cCopy code
def get_string_lengths(strings):
    return {string: len(string) for string in strings}

```
