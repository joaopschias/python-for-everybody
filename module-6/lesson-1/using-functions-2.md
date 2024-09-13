
# Module 6 - Lesson 2: Building and Using Functions

## Overview
In this lesson, we explore the definition and use of functions in Python. The key idea is that the `def` statement defines a function, which can then be called or invoked multiple times in a program.

### Key Concepts:
- The `def` statement defines a function but does not execute the function.
- To execute the function, we must **call** or **invoke** it.
- Functions may have **arguments**, which allow the function to operate on different inputs.
- The `return` keyword specifies what value a function should return as output.

---

### Defining a Function
We create a new function using the `def` keyword followed by optional parameters in parentheses.
We indent the body of the function, and this defines the function without executing it.

```python
def print_lyrics():
    print("I'm a lumberjack, and I'm okay.")
    print('I sleep all night and I work all day.')
```

This does **not** execute the function.

---

### Calling a Function
In order to execute a function, we need to call it using its name followed by parentheses.

```python
x = 5
print('Hello')

def print_lyrics():
    print("I'm a lumberjack, and I'm okay.")
    print('I sleep all night and I work all day.')

print('Yo')
x = x + 2
print(x)
```

**Output**:
```
Hello
Yo
7
```

---

### Passing Arguments to Functions
An **argument** is a value passed to the function when calling it. Arguments allow functions to perform different tasks based on the input provided.

```python
big = max('Hello world')
```

Here, `'Hello world'` is the argument passed to the function `max`, and the result is stored in the variable `big`.

### Parameters
A **parameter** is the variable used in the function definition to represent the argument passed to the function. The function can then access this parameter.

```python
def greet(lang):
    if lang == 'es':
        print('Hola')
    elif lang == 'fr':
        print('Bonjour')
    else:
        print('Hello')
```

**Example Calls**:
```python
greet('en')  # Output: Hello
greet('es')  # Output: Hola
greet('fr')  # Output: Bonjour
```

---

### Return Values
A function may compute a value and use the `return` statement to send this value back as the result of the function.

```python
def greet():
    return "Hello"

print(greet(), "Glenn")
print(greet(), "Sally")
```

**Output**:
```
Hello Glenn
Hello Sally
```

The `return` keyword ends the function and "returns" the value back to the caller.

---

### Return Value Example with Parameters
```python
def greet(lang):
    if lang == 'es':
        return 'Hola'
    elif lang == 'fr':
        return 'Bonjour'
    else:
        return 'Hello'

print(greet('en'), 'Glenn')
print(greet('es'), 'Sally')
print(greet('fr'), 'Michael')
```

**Output**:
```
Hello Glenn
Hola Sally
Bonjour Michael
```

---

### Arguments, Parameters, and Results
A function can accept parameters, and its result is specified by the `return` statement.

```python
big = max('Hello world')
print(big)
```

This would return `'w'`, which is the maximum character in the string `'Hello world'`.

---

### Multiple Parameters / Arguments
We can define functions that accept multiple parameters.

```python
def addtwo(a, b):
    added = a + b
    return added

x = addtwo(3, 5)
print(x)
```

**Output**:
```
8
```

---

### Summary
In this lesson, we covered how to define, call, and use functions in Python. We also explored how functions can accept parameters and return values. Using functions helps reduce repetitive code and makes programs easier to understand and maintain.

