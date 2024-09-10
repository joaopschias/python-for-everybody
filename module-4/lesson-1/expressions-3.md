# Module 4, Lesson 3: Writing Your First Python Program

## Overview

In this lesson, we will create our first complete Python program that includes input, processing, and output. We’ll also discuss the importance of comments in code to improve readability and maintainability.

## Key Topics Covered

### 1. Comments in Python
As demonstrated in the **Comments in Python** slide, comments are a way to add human-readable explanations to your code that are ignored by Python during execution. Comments are useful for describing what the code does, documenting the author of the code, and for temporarily disabling code during debugging.

#### Example:
```python
# This is a comment
x = 42  # This assigns 42 to x
```

In this example:
- Any text following the `#` symbol is ignored by Python.

Comments help you understand the purpose of your code when revisiting it later and are particularly helpful when working on large or complex codebases.

### 2. Word Frequency Program
The **Word Frequency Program** slide shows a simple Python program that counts the frequency of words in a file. The comments included in the code help explain each section of the program.

#### Example Code with Comments:
```python
# Get the name of the file and open it
name = input('Enter file:')
handle = open(name, 'r')

# Count word frequency
counts = dict()
for line in handle:
    words = line.split()
    for word in words:
        counts[word] = counts.get(word, 0) + 1

# Find the most common word
bigcount = None
bigword = None
for word, count in counts.items():
    if bigcount is None or count > bigcount:
        bigword = word
        bigcount = count

# All done
print(bigword, bigcount)
```

- **Comments** describe each major block of code, making it easier for someone reading the program to understand what is happening.
- The program reads the file, counts word occurrences, and finds the most frequent word.

### 3. Converting User Input
As shown in the **Converting User Input** slide, when gathering input from the user, Python treats the input as a string by default. To perform numeric operations, you must convert the input to the appropriate data type (e.g., `int` or `float`).

#### Example:
```python
# Convert elevator floors
inp = input('Europe floor? ')
usf = int(inp) + 1
print('US floor', usf)
```

In this example:
- The `input()` function prompts the user for a floor number, but the input is treated as a string.
- The `int()` function is used to convert the string input into an integer, so arithmetic operations can be performed.

This small program demonstrates the input, processing, and output pattern:
- **Input**: The user is asked for the European floor number.
- **Processing**: The program converts the input and adds one to the floor number.
- **Output**: The corresponding US floor is printed.

### 4. Input, Processing, and Output Pattern
The program we wrote follows the classic **input-processing-output** pattern, which is common in most programs:
1. **Input**: Collect data from the user or another source.
2. **Processing**: Perform calculations or manipulate the data.
3. **Output**: Present the result to the user.

In this case, the input is the floor number, the processing is the conversion from European to US floor standards, and the output is the adjusted floor number.

### 5. Importance of Using Comments
As discussed throughout the lesson, comments are essential for making code more understandable. Writing clear, meaningful comments helps not only others but also your future self when revisiting the code after some time.

You should add comments where necessary, but avoid adding comments for trivial actions like `x = 1  # assign 1 to x`, as they do not provide additional insight.

This lesson covered the basic structure of Python programs, including input, processing, and output. We also discussed how to use comments effectively to improve code readability. Next, we will explore **conditional execution** using `if` statements, which will allow us to add decision-making capabilities to our programs.
