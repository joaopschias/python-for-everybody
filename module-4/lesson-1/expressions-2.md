# Module 4, Lesson 2: Operators, Expressions, and Data Types in Python

## Overview

In this lesson, we dive deeper into the right-hand side of assignment statements, focusing on operators, expressions, and how Python handles different data types. You will learn how to use operators for arithmetic operations, manage the order of operations, and how Python distinguishes between types like integers, floating-point numbers, and strings.

## Key Topics Covered

### 1. Arithmetic Operators in Python
Python supports common arithmetic operations such as:
- **Addition (`+`)**
- **Subtraction (`-`)**
- **Multiplication (`*`)**
- **Division (`/`)**
- **Exponentiation (`**`)**: Raises a number to the power of another.
- **Modulo (`%`)**: Returns the remainder after division, useful for tasks like generating random numbers within a range or checking for even/odd numbers.

...

### 5. Integer Division
As shown in the **Integer Division** slide, integer division in Python 3 always returns a floating-point result, even if the division is exact.

#### Example:
```python
print(10 / 2)  # Outputs: 5.0
print(9 / 2)   # Outputs: 4.5
print(99 / 100)  # Outputs: 0.99
```

In Python 3, the division operator (`/`) produces a floating-point result, regardless of whether the numbers divide evenly. This behavior differs from Python 2, where integer division would truncate the decimal portion if both operands were integers.

### 6. String Conversions
Python allows you to convert strings to integers or floats using the `int()` and `float()` functions, as demonstrated in the **String Conversions** slide. However, you will encounter an error if the string doesn't represent a valid number.

#### Example:
```python
sval = '123'
print(type(sval))  # Outputs: <class 'str'>

ival = int(sval)  # Converts the string to an integer
print(type(ival))  # Outputs: <class 'int'>
print(ival + 1)  # Outputs: 124
```

If the string contains non-numeric characters, attempting to convert it to an integer or float will raise a `ValueError`:

```python
nsv = 'hello bob'
niv = int(nsv)  # Raises a ValueError
```

### 7. User Input
The **input()** function allows Python to pause and wait for the user to input data via the keyboard. The input is always returned as a string, as shown in the **User Input** slide.

#### Example:
```python
nam = input('Who are you? ')
print('Welcome', nam)
```

In this example, the program waits for the user to type their name and then prints a welcome message. Even if the user inputs numbers, they are treated as strings by default. To work with numerical input, you can convert the string to an integer or float.

