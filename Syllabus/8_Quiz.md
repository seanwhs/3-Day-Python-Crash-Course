# Quiz - Exception Handling

1. What is an exception in Python?  
A) A syntax error  
B) A logical error  
C) An error that occurs during program execution  
D) A runtime error  

Answer: C) An error that occurs during program execution  

1. Which keyword is used to raise an exception in Python?  
A) except  
B) finally  
C) raise  
D) try  
  
Answer: C) raise  

1. What is the purpose of the finally block in a try-except-finally statement?  
A) To catch exceptions  
B) To handle exceptions  
C) To execute code whether an exception is raised or not  
D) To ignore exceptions  

Answer: C) To execute code whether an exception is raised or not  

1. Which of the following is not a standard Python exception?  
A) ZeroDivisionError  
B) TypeError  
C) IOError  
D) StopIteration  

Answer: D) StopIteration  

1. In a try-except block, which section of code is executed when an exception is raised?  
A) The try block  
B) The except block  
C) The finally block  
D) None of the above  
  
Answer: B) The except block  

1. What is the output of the following code?  

```
pythonCopy code
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Division by zero!")
finally:
    print("This code will always execute.")

```

A) Division by zero!  
B) This code will always execute.  
C) Division by zero! This code will always execute.  
D) None of the above  

Answer: C) Division by zero! This code will always execute.  

1. What is the output of the following code?  

```
pythonCopy code
try:
    f = open("nonexistentfile.txt")
    print(f.read())
except IOError:
    print("File not found!")
finally:
    if 'f' in locals():
        f.close()

```

A) File not found!  
B) An IOError exception is raised.  
C) An exception is raised, but it is not an IOError.  
D) None of the above  

Answer: A) File not found!  

1. Which keyword is used to catch exceptions in Python?  
a) try  
b) except  
c) finally  
d) raise  

Answer: b) except  

1. What is the purpose of the finally block in a try-except statement?  
a) It is executed if an exception is raised  
b) It is always executed, regardless of whether an exception is raised or not  
c) It is executed if the try block is successful  
d) It is used to raise an exception  

Answer: b) It is always executed, regardless of whether an exception is raised or not  

1. Which of the following is not a built-in exception in Python?  
a) ValueError  
b) ZeroDivisionError  
c) TypeError  
d) NullPointerException  

Answer: d) NullPointerException  

1. What is the purpose of the else block in a try-except statement?  
a) It is executed if an exception is raised  
b) It is always executed, regardless of whether an exception is raised or not  
c) It is executed if the try block is successful  
d) It is used to raise an exception  

Answer: c) It is executed if the try block is successful  

1. Which of the following statements is true about the raise statement in Python?  
a) It can only be used to raise built-in exceptions  
b) It can only be used inside a try block  
c) It can be used to raise user-defined exceptions  
d) It can be used to catch exceptions  

Answer: c) It can be used to raise user-defined exceptions  

1. Which of the following keywords is used to specify which exceptions a function can raise?  
a) try  
b) except  
c) raise  
d) None of the above  

Answer: d) None of the above. The correct keyword is "raise" with a list of exceptions in parentheses after it.  

1. What is the purpose of the traceback module in Python?  
a) It is used to handle exceptions  
b) It is used to print a stack trace when an exception occurs  
c) It is used to raise exceptions  
d) It is used to create custom exceptions  

Answer: b) It is used to print a stack trace when an exception occurs  
