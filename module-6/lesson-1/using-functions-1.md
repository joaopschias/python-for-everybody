# Module 6 - Lesson 1: Stored and Reused Steps (Functions)

In this lesson, we will discuss **storing and reusing code**, which is a fundamental practice in programming. This prevents unnecessary repetition of code, which can be a source of errors if maintenance is needed. To achieve this, we use **functions** in Python, which allow blocks of code to be defined and reused.

## Defining Functions
The keyword `def` is used to define a function in Python. This starts a **function definition**. Here's an example:

```python
def thing():
    print('Hello')
    print('Fun')
```

In this case, the function `thing()` does not execute immediately; rather, Python remembers the code associated with `thing()` until it is called later.

### Key Points:
- The function definition begins with the keyword `def`.
- The function name is followed by parentheses `()`. Parameters can be passed here, but in this case, there are no parameters.
- The body of the function is indented.
- When you "call" the function later in the code, it runs the indented block.

### Calling a Function:
```python
thing()
print('Zip')
thing()
```

When `thing()` is called, it executes the stored block of code. The output of this code will be:

```
Hello
Fun
Zip
Hello
Fun
```

As you can see, the function can be called multiple times without rewriting the code. This is the essence of **not repeating yourself** (DRY - Don't Repeat Yourself).

## Using Built-in Functions
We have been using several **built-in functions** in Python like `print()`, `input()`, `type()`, `float()`, and `int()`. These are examples of reusable code that Python provides, and we call these functions by using their names followed by parentheses.

### Example of the `max()` Function:
```python
big = max('Hello world')
print(big)
```

The `max()` function returns the largest character in the string, which in this case is `'w'`. Similarly, the `min()` function returns the smallest character, which is the space character `' '`.

### Type Conversion:
Type conversion functions like `int()` and `float()` are essential when dealing with input data that needs to be converted into a different type. For example, using `input()` always returns a string, so we use `int()` or `float()` to convert the input into a number.

```python
sval = '123'
ival = int(sval)
print(ival + 1)
```

This will output `124`, as the string `'123'` has been converted to an integer.

## Next Steps:
Now that we've covered the basics of **defining** and **calling functions**, in the next lesson, we will learn how to define and use our own functions effectively in Python.