# Exercises - Input and Output

1. Write a program to read a file "input.txt" and write its contents to a new file "output.txt".

```
pythonCopy code
with open("input.txt", "r") as input_file:
    with open("output.txt", "w") as output_file:
        output_file.write(input_file.read())

```

1. Write a program to read the first line of a file "data.txt" and print it to the console.

```
pythonCopy code
with open("data.txt", "r") as file:
    first_line = file.readline()
    print(first_line)

```

1. Write a program to read a file "data.txt" and count the number of lines in it.

```
pythonCopy code
with open("data.txt", "r") as file:
    num_lines = 0
    for line in file:
        num_lines += 1
    print("Number of lines:", num_lines)

```

1. Write a program to read a file "data.txt" and print only the lines that contain the word "Python".

```
pythonCopy code
with open("data.txt", "r") as file:
    for line in file:
        if "Python" in line:
            print(line)

```

1. Write a program to read a file "data.txt" and write only the lines that contain the word "Python" to a new file "python_data.txt".

```
pythonCopy code
with open("data.txt", "r") as input_file:
    with open("python_data.txt", "w") as output_file:
        for line in input_file:
            if "Python" in line:
                output_file.write(line)

```

Exercise 2: File Modes

1. What is the file mode used for writing to a file in Python?
Answer: "w"
2. What is the file mode used for appending to a file in Python?
Answer: "a"
3. What is the file mode used for reading and writing to a file in Python?
Answer: "r+"
4. What is the file mode used for writing to a new file only if it does not already exist in Python?
Answer: "x"
5. What is the file mode used for reading a file as binary data in Python?
Answer: "rb"

1. Write a Python program to read a file and display the contents of the file on the console.

```
pythonCopy code
with open("file.txt", "r") as f:
    contents = f.read()
    print(contents)

```

1. Write a Python program to read the contents of a file line by line and display the lines on the console.

```
pythonCopy code
with open("file.txt", "r") as f:
    for line in f:
        print(line)

```

1. Write a Python program to write the contents of a list to a file.

```
pythonCopy code
my_list = ['apple', 'banana', 'cherry']

with open("file.txt", "w") as f:
    for item in my_list:
        f.write("%s\n" % item)

```

1. Write a Python program to read the contents of a CSV file and display them on the console.

```
pythonCopy code
import csv

with open('file.csv', mode='r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)

```

1. Write a Python program to append text to an existing file.

```
pythonCopy code
with open("file.txt", "a") as f:
    f.write("This is some appended text.")

```

1. Write a Python program to read a file and count the number of lines, words, and characters in the file.

```
pythonCopy code
with open("file.txt", "r") as f:
    num_lines = 0
    num_words = 0
    num_chars = 0
    for line in f:
        words = line.split()
        num_lines += 1
        num_words += len(words)
        num_chars += len(line)
    print("Number of lines:", num_lines)
    print("Number of words:", num_words)
    print("Number of characters:", num_chars)

```

1. Write a Python program to create a file, write some text to the file, and then read the file and display its contents.

```
pythonCopy code
with open("file.txt", "w") as f:
    f.write("This is some text.")

with open("file.txt", "r") as f:
    contents = f.read()
    print(contents)

```

1. Write a Python program to copy the contents of one file to another file.

```
pythonCopy code
with open("file1.txt", "r") as f1:
    with open("file2.txt", "w") as f2:
        for line in f1:
            f2.write(line)

```

Answers:

1. Assuming the file to read is called **`file.txt`**, the output of this program would be the contents of the file printed on the console.  
2. Assuming the file to read is called **`file.txt`**, the output of this program would be each line of the file printed on the console.  
3. Assuming the list to write is called **`my_list`** and the file to write to is called **`file.txt`**, this program would write each item of the list to the file on a separate line.    
4. Assuming the file to read is a CSV file called **`file.csv`**, this program would print each row of the file on the console.  
5. Assuming the file to append to is called **`file.txt`**, this program would append the text "This is some appended text." to the end of the file.
6. Assuming the file to read is called **`file.txt`**, this program would print the number of lines, words, and characters in the file.  
7. This program would create a file called **`file.txt`**, write the text "This is some text."  
