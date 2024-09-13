# Module 5 - Lesson 2: Conditional Execution Patterns

## Introduction
In this lesson, we explore more complex patterns for conditional execution in Python. By building on what we learned with basic `if` statements, we introduce new concepts such as `elif` (else if) and `try/except` for error handling. As always, it’s important to visualize how these blocks work together to control the flow of the program.

---

## Visualizing Blocks

We start by understanding how blocks of code work within an `if` statement. Think of a block as starting with the `if` and ending after the last indented line. The key is that each block has one entrance and one exit. These blocks create the logic in our programs.

**Example:**
```python
x = 4
if x > 2:
    print("Bigger")
else:
    print("Smaller")
print("All Done")
```

**Visual Representation:**

---
The logic here checks if `x` is greater than 2. If it is, it prints "Bigger", otherwise, it prints "Smaller". The program always prints "All Done" at the end.
---

## Multi-way if-elif-else

The next step in complexity is the multi-way decision using `elif`. The structure checks conditions in sequence, and only one condition will run.

**Example:**
```python
x = 5
if x < 2:
    print("small")
elif x < 10:
    print("Medium")
else:
    print("LARGE")
print("All done")
```

**Visual Representation:**

---
In this code, we check multiple conditions, but only the first `True` condition will be executed. If `x` is less than 2, "small" is printed, and so on.
---

### Multi-way Example (x = 5)

If `x` is 5, the condition checks will skip the first but execute the second (`x < 10`).

**Example:**
```python
x = 5
if x < 2:
    print("small")
elif x < 10:
    print("Medium")
else:
    print("LARGE")
print("All done")
```

**Visual Representation:**

```
The program evaluates the first condition, which is false. Then it moves to the second condition (`x < 10`), which is true, printing "Medium".
```

---

### Multi-way Example (x = 20)

When `x` is set to 20, the program runs through all conditions until it reaches the `else`.

**Example:**
```python
x = 20
if x < 2:
    print("small")
elif x < 10:
    print("Medium")
else:
    print("LARGE")
print("All done")
```

**Visual Representation:**

```
In this case, "LARGE" is printed, as `x` does not meet any of the other conditions.
```

---

## Handling Errors with `try/except`

Python provides a way to handle errors gracefully using the `try/except` block. This allows us to attempt to run code that might fail, and catch the failure to avoid a crash (traceback).

### Without `try/except`

When no error handling is used, a traceback will occur when an invalid operation is attempted.

**Example:**
```python
astr = "Hello Bob"
istr = int(astr)  # This will cause a ValueError
print('First', istr)
```

**Output:**
```bash
Traceback (most recent call last):
ValueError: invalid literal for int() with base 10: 'Hello Bob'
```

---

### With `try/except`

By wrapping the problematic line in a `try/except` block, we can handle the error gracefully.

**Example:**
```python
astr = "Hello Bob"
try:
    istr = int(astr)
except:
    istr = -1
print('First', istr)
```

**Output:**
```bash
First -1
```

The program catches the error and sets the value to -1 instead of crashing.

---

## Final Example

Here’s a more practical use case of `try/except`. We prompt the user for a number, attempt to convert it, and handle any errors gracefully.

**Example:**
```python
rawstr = input('Enter a number: ')
try:
    ival = int(rawstr)
except:
    ival = -1

if ival > 0:
    print('Nice work')
else:
    print('Not a number')
```

**Output:**
```bash
$ python tryexcept.py
Enter a number: 42
Nice work
```

**Alternative Output:**
```bash
$ python tryexcept.py
Enter a number: forty-two
Not a number
```

---

## Conclusion

In this lesson, we’ve learned how to manage multiple conditions using `if`, `elif`, and `else`. We’ve also explored how to handle potential errors using the `try/except` block, ensuring our programs don’t crash unexpectedly.

Next, we’ll dive into more conditional execution techniques in the following lessons. Keep practicing with conditional statements, as they are key to controlling the flow of your programs!
