# Module 4, Lesson 1: Constants, Variables, and Assignment in Python

## Overview

In this lesson, we introduce basic building blocks of Python such as constants, variables, and how assignment statements work. We’ll discuss naming rules for variables and how to structure expressions in Python.

## Key Topics Covered

### 1. Constants
As shown in the **Constants** slide, constants are fixed values in Python that do not change throughout the program execution. These values can be integers, floating-point numbers, or strings.

#### Example of Constants:
```python
print(123)         # Outputs: 123
print(98.6)        # Outputs: 98.6
print('Hello world')  # Outputs: Hello world
```

- **Numeric constants**: Fixed numeric values like `123` or `98.6`.
- **String constants**: Enclosed in single (`'`) or double (`"`) quotes, such as `'Hello world'`.

### 2. Reserved Words
As shown in the **Reserved Words** slide, Python has a set of reserved keywords that have specific meanings. These keywords cannot be used as variable names.

#### List of Reserved Words:
- `False`, `None`, `True`, `and`, `as`, `assert`, `break`, `class`, `continue`, `def`, `del`, `elif`, `else`, `except`, `finally`, `for`, `from`, `global`, `if`, `import`, `in`, `is`, `lambda`, `nonlocal`, `not`, `or`, `pass`, `raise`, `return`, `try`, `while`, `with`, `yield`

Attempting to use any of these words as variable names will result in an error.

### 3. Variables
As shown in the **Variables** slide, a variable is a named memory location where data can be stored and retrieved. You assign a value to a variable and can change the value later in the program.

#### Example:
```python
x = 12.2
y = 14
```

In this example:
- The variable `x` holds the value `12.2`.
- The variable `y` holds the value `14`.

### 4. Variable Naming Rules
The **Python Variable Name Rules** slide explains the following rules for naming variables:
- Variable names must start with a letter or an underscore (`_`).
- They may contain letters, numbers, and underscores, but cannot start with a number.
- Python is **case-sensitive**, meaning `spam`, `Spam`, and `SPAM` are different variables.

#### Examples of Valid and Invalid Variable Names:
- **Valid names**: `spam`, `eggs`, `spam23`, `_speed`
- **Invalid names**: `23spam`, `#sign`, `var.12`

### 5. Assignment Statements
In Python, an **assignment statement** assigns a value to a variable. This is done with the equal sign (`=`), as shown in the **Sentences or Lines** slide.

#### Example:
```python
x = 2
x = x + 2
print(x)  # Outputs: 4
```

In this example:
- `x` is first assigned the value `2`.
- Then `x` is updated by adding `2` to its previous value.
- Finally, the `print()` statement outputs the updated value of `x`.

### 6. Using Descriptive Variable Names
The **Code Example** slide illustrates that using meaningful variable names, like `hours`, `rate`, and `pay`, makes the code easier to understand, as opposed to using cryptic variable names like `x1q3z9ocd`.

#### Bad Example:
```python
x1q3z9ocd = 35.0
x1q3z9afd = 12.50
x1q3p9afd = x1q3z9ocd * x1q3z9afd
print(x1q3p9afd)
```

#### Better Example:
```python
hours = 35.0
rate = 12.50
pay = hours * rate
print(pay)  # Outputs: 437.5
```

Using descriptive names like `hours` and `rate` improves readability and makes the code easier to maintain.

### 7. Expressions in Assignment Statements
As shown in the **Assignment Statements** slide, assignment statements can contain expressions on the right-hand side. Python evaluates the expression and stores the result in the variable on the left-hand side.

#### Example:
```python
x = 3.9 * x * (1 - x)
```

In this example, the right-hand side is an expression that multiplies `x` by `3.9` and another factor `(1 - x)`. The result is assigned to `x`.

### 8. Updating Variables
As shown in the **Variable Update** slides, a variable’s value can be updated by assigning a new expression to it. The expression is evaluated and replaces the old value in the variable.

#### Example:
```python
x = 0.6
x = 3.9 * x * (1 - x)  # Updates x to 0.936
```

Initially, `x` holds the value `0.6`. After evaluating the expression, `x` is updated to `0.936`. This process of updating the value is common in iterative calculations.