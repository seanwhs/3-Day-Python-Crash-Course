# Exercises - Functions

1. Write a function in Python that takes a string as input and returns the number of words in that string.

```
pythonCopy code
def count_words(input_string):
    word_list = input_string.split()
    return len(word_list)

# Example usage
input_string = "This is a test string"
print(count_words(input_string)) # Output: 5

```

1. Write a function in Python that takes a list of integers as input and returns the average of those integers.

```
pythonCopy code
def calculate_average(input_list):
    total = sum(input_list)
    count = len(input_list)
    if count == 0:
        return 0
    else:
        return total / count

# Example usage
input_list = [2, 4, 6, 8]
print(calculate_average(input_list)) # Output: 5.0

```

1. Write a function in Python that takes a string as input and returns True if the string is a palindrome, and False otherwise.

```
pythonCopy code
def is_palindrome(input_string):
    input_string = input_string.lower()
    input_string = input_string.replace(" ", "")
    reverse_string = input_string[::-1]
    if input_string == reverse_string:
        return True
    else:
        return False

# Example usage
input_string = "A man a plan a canal Panama"
print(is_palindrome(input_string)) # Output: True

```

1. Write a function in Python that takes a list of integers as input and returns the maximum and minimum values in the list.

```
pythonCopy code
def find_max_min(input_list):
    max_val = max(input_list)
    min_val = min(input_list)
    return max_val, min_val

# Example usage
input_list = [4, 1, 6, 2, 8]
print(find_max_min(input_list)) # Output: (8, 1)

```

1. Write a function in Python that takes a list of integers as input and returns a new list containing only the even numbers.

```
pythonCopy code
def filter_even_numbers(input_list):
    output_list = []
    for num in input_list:
        if num % 2 == 0:
            output_list.append(num)
    return output_list

# Example usage
input_list = [2, 5, 7, 8, 10]
print(filter_even_numbers(input_list)) # Output: [2, 8, 10]

```

1. Write a function in Python that takes two lists of integers as input and returns a new list containing the common elements in both input lists.

```
pythonCopy code
def find_common_elements(list1, list2):
    output_list = []
    for num in list1:
        if num in list2 and num not in output_list:
            output_list.append(num)
    return output_list

# Example usage
list1 = [1, 2, 3, 4, 5]
list2 = [3, 4, 5, 6, 7]
print(find_common_elements(list1, list2)) # Output: [3, 4, 5]

```

1. Write a function in Python that takes a list of strings as input and returns the longest string in the list.

```
pythonCopy code
def find_longest_string(input_list):
    longest_string = ""
    for string in input_list:
        if len(string) > len(longest_string):
            longest_string = string
    return longest_string

# Example usage
input_list = ["hello", "world", "this", "is", "a", "test"]
print(find_longest_string(input_list)) # Output: "hello"

```

1. Write a function in Python that takes a list of numbers as input and returns True if the numbers are in strictly increasing order, and False otherwise.

```
pythonCopy code
def is_increasing(input_list):
    for i in range(len(input_list)-1):
        if input_list[i] >= input_list[i+1]:
            return False
    return True

# Example usage
input_list1 = [1, 2, 3, 4, 5]
input_list2 = [1, 3, 2, 4, 5]
print(is_increasing(input_list1)) # Output: True
print(is_increasing(input_list2)) # Output: False

```

1. Write a function in Python that takes a string as input and returns the number of vowels in the string.

```
pythonCopy code
def count_vowels(input_string):
    vowels = "aeiou"
    count = 0
    for char in input_string:
        if char.lower() in vowels:
            count += 1
    return count

# Example usage
input_string = "Hello World"
print(count_vowels(input_string)) # Output: 3

```

1. Write a function in Python that takes a list of strings as input and returns a new list containing only the strings that have length greater than 5.

```
pythonCopy code
def filter_long_strings(input_list):
    output_list = []
    for string in input_list:
        if len(string) > 5:
            output_list.append(string)
    return output_list

# Example usage
input_list = ["hello", "world", "this", "is", "a", "test"]
print(filter_long_strings(input_list)) # Output: ["wor

```
