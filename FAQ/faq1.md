Q1. Does white space matter in the code?

A1: White space is ignored by the interpreter except in the cases below:

1. When space is in front of a line of code:
```
greeting1 = "Hi"
greeting2 = "Hello  "
```
Running the above code produces an error because of the white space before greeting1.

2. When space is inside strings. Having white space inside a string will not produce any error, but you should keep in mind that  "Hello  " and "Hello"  are not treated as the same value by Python.

3. When space occurs in a variable name:

```
today greeting = "Hello"
```

The above code will produce an error because it is against the syntax rules to have spaces in variables. Programmers are encouraged to use an underscore instead of a space.

---

Q2. Should a function argument be a variable or a value?

A2: It can be either way, depending on the scenario.

It is OK to provide the value (e.g., a string) directly as an argument:

```
user_input = input("Enter a value:")
```


But it is also OK to provide the variable associated with the value:

```
message = "Enter a value:"
user_input = input(message)
```

---

Q3. What happens if you create a variable two times in a program? For example:

```
greeting = "Hello"
greeting = "Hi"
```

A3: The variable will first be assigned the value "Hello" and then immediately, it will be assigned the new value "Hi" overwriting the old value.
