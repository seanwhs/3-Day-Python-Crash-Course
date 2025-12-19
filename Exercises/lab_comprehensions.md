# **Python Lab Worksheet: Comprehensions in Python**

**Name:** ______________________
**Date:** ______________________

**Objective:**
Learn how to create **lists, tuples, and dictionaries efficiently** using comprehensions, and practice applying conditions and transformations.

---

## **Part 1: List Comprehension**

**Task 1: Basic list comprehension**

Create a list of squares from 1 to 5:

```python
squares = [x**2 for x in range(1, 6)]
print(squares)  # Output → ________
```

---

**Task 2: List comprehension with condition**

Create a list of even numbers from 1 to 10:

```python
evens = [x for x in range(1, 11) if x % 2 == 0]
print(evens)  # Output → ________
```

---

**Task 3: Transform items in a list**

```python
words = ["python", "java", "c++"]
upper_words = [w.upper() for w in words]
print(upper_words)  # Output → ________
```

---

## **Part 2: Tuple Comprehension (via generator expression)**

> Note: Python does not support direct tuple comprehension, but we can use a **generator expression** and convert it to a tuple.

**Task 4: Basic tuple comprehension**

```python
t = tuple(x**2 for x in range(1, 6))
print(t)  # Output → ________
```

**Task 5: Tuple comprehension with condition**

```python
t_even = tuple(x for x in range(1, 11) if x % 2 == 0)
print(t_even)  # Output → ________
```

---

## **Part 3: Dictionary Comprehension**

**Task 6: Basic dictionary comprehension**

Create a dictionary mapping numbers to their squares:

```python
squares_dict = {x: x**2 for x in range(1, 6)}
print(squares_dict)  # Output → ________
```

---

**Task 7: Dictionary comprehension with condition**

Create a dictionary of numbers from 1 to 10 that are even, mapping to their cubes:

```python
even_cubes = {x: x**3 for x in range(1, 11) if x % 2 == 0}
print(even_cubes)  # Output → ________
```

---

**Task 8: Transform keys or values**

```python
words = ["apple", "banana", "cherry"]
word_lengths = {w: len(w) for w in words}
print(word_lengths)  # Output → ________
```

---

## **Part 4: Nested Comprehension**

**Task 9: Nested list comprehension**

Create a 3x3 matrix as a list of lists:

```python
matrix = [[i*j for j in range(1, 4)] for i in range(1, 4)]
print(matrix)  # Output → ________
```

**Task 10: Nested dictionary comprehension**

Create a dictionary mapping numbers 1-3 to their multiples 1-3:

```python
multi_dict = {i: {j: i*j for j in range(1, 4)} for i in range(1, 4)}
print(multi_dict)  # Output → ________
```

---

## **Part 5: Challenge**

1. Use **list comprehension** to create a list of all vowels in a sentence:

```python
sentence = "Python is fun"
vowels = [ch for ch in sentence if ch.lower() in "aeiou"]
print(vowels)  # Output → ________
```

2. Use **dictionary comprehension** to map each character in the sentence to its ASCII value:

```python
char_dict = {ch: ord(ch) for ch in sentence}
print(char_dict)  # Output → ________
```

3. Use **tuple comprehension** (generator expression) to get squares of odd numbers from 1 to 10:

```python
odd_squares = tuple(x**2 for x in range(1, 11) if x % 2 != 0)
print(odd_squares)  # Output → ________
```

---

