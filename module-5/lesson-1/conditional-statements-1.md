# Module 5, Lesson 1: Conditional Execution in Python

## Overview

In this lesson, we delve into **conditional execution**, which allows us to control the flow of our Python programs based on specific conditions. We will explore **if statements**, **else statements**, **comparison operators**, and different types of decision structures.

## Key Topics Covered

### 1. Conditional Steps

The first step in understanding conditional execution is to use **if statements** to make decisions. The **Conditional Steps** diagram demonstrates how the program checks whether a condition is true or false and then executes the corresponding block of code.

#### Example:
```python
x = 5
if x < 10:
    print('Smaller')
if x > 20:
    print('Bigger')
print('Finis')
```

Output:
```
Smaller
Finis
```

- **Explanation**: The program checks if `x < 10`, which is true, so it prints "Smaller". Since `x > 20` is false, that part is skipped. Finally, "Finis" is printed.

---

### 2. Comparison Operators

In Python, **comparison operators** are used to compare values and produce boolean expressions (True/False). These expressions help control the flow of a program.

#### Common Comparison Operators:
- `<` : Less than
- `<=` : Less than or equal to
- `==` : Equal to
- `>=` : Greater than or equal to
- `>` : Greater than
- `!=` : Not equal

#### Example:
```python
x = 5
if x == 5:
    print('Equals 5')
if x > 4:
    print('Greater than 4')
if x >= 5:
    print('Greater than or Equals 5')
if x < 6:
    print('Less than 6')
if x <= 5:
    print('Less than or Equals 5')
if x != 6:
    print('Not equal 6')
```

---

### 3. One-Way Decisions

One-way decisions allow the program to execute a block of code only if a particular condition is true.

#### Example:
```python
x = 5
print('Before 5')
if x == 5:
    print('Is 5')
    print('Is Still 5')
    print('Third 5')
print('Afterwards 5')
```

Output:
```
Before 5
Is 5
Is Still 5
Third 5
Afterwards 5
```

- **Explanation**: Since `x == 5` is true, the code block under the `if` statement runs.

---

### 4. Two-Way Decisions

Sometimes we want to do one thing if a condition is true, and something else if the condition is false. This is where **else** comes in, creating a **two-way decision**.

#### Example:
```python
x = 4
if x > 2:
    print('Bigger')
else:
    print('Smaller')
print('All done')
```

Output:
```
Bigger
All done
```

- **Explanation**: Since `x > 2` is true, it prints "Bigger". The `else` block is skipped.

---

### 5. Nested Decisions

**Nested decisions** are when one decision structure is nested inside another. This allows us to handle more complex logic.

#### Example:
```python
x = 42
if x > 1:
    print('More than one')
    if x < 100:
        print('Less than 100')
print('All done')
```

Output:
```
More than one
Less than 100
All done
```

- **Explanation**: The program checks if `x > 1`, which is true, so it prints "More than one". Then it checks if `x < 100`, which is also true, so it prints "Less than 100".

---

### 6. Blocks of Code and Indentation

In Python, **indentation** is crucial for defining blocks of code. Indentation determines which statements belong to the `if` block or other control structures like loops.

#### Example:
```python
x = 5
if x > 2:
    print('Bigger than 2')
    print('Still bigger')
print('Done with 2')

for i in range(5):
    print(i)
    if i > 2:
        print('Bigger than 2')
    print('Done with i', i)
print('All done')
```

Output:
```
Bigger than 2
Still bigger
Done with 2
0
1
2
3
Bigger than 2
Done with i 3
4
Bigger than 2
Done with i 4
All done
```

- **Explanation**: The indentation defines the scope of the `if` block and the `for` loop. Proper indentation ensures that the correct code block is executed.

---

This lesson introduced the basic concepts of conditional execution, comparison operators, and decision structures in Python. By understanding how to use **if**, **else**, and **nested decisions**, you can build programs that react to different conditions and execute the appropriate blocks of code. Up next, we will explore more advanced control structures and logical operators.