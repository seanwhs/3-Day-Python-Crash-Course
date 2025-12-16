# What is a bug?

Programmers spend around 20-40% of their time coding and 20-40% hunting and fixing bugs. Take a look at the program below:

print("Hello"

That program has a bug because when you run the program, it produces an error message. The error message in our case is this:

 File "/Users/as/main.py", line 1
    print("Hello"
         ^
SyntaxError: '(' was never closed

## How to fix a bug

As a programmer, you should carefully read the error message and try to understand it. In our particular example, the error message informs us that we forgot a parenthesis. Therefore, to fix the bug, you should add a parenthesis as follows:

print("Hello")

Run the above code, and you will see that it returns the expected output, which is Hello. That means the bug has been fixed. In the following article, you will do your first bug-fixing exercises.

Let's go!
