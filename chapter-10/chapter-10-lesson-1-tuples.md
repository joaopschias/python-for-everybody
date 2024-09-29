# Chapter 10: Tuples in Python

Tuples are immutable data structures similar to lists but cannot be modified after creation. This immutability makes them more efficient in some scenarios compared to lists, especially when data doesn't need to be altered.

## 1. Tuples are Similar to Lists

Tuples are ordered collections of items, much like lists. However, tuples are created using parentheses `()` instead of square brackets `[]`. You can access elements using indexing, just like with lists.

Example:
```python
x = ('Glenn', 'Sally', 'Joseph')
print(x[2])  # Outputs: Joseph
```
Here, `x` is a tuple containing three elements. You can access `"Joseph"` using its index `2`, just like you would in a list.

## 2. Tuples are Immutable

Unlike lists, tuples are **immutable**, meaning their contents cannot be changed after they are created. Attempting to modify a tuple will raise a `TypeError`.

Example:
```python
z = (5, 4, 3)
z[2] = 0  # Raises: TypeError: 'tuple' object does not support item assignment
```

This immutability is a fundamental characteristic of tuples. It allows Python to optimize the memory usage of tuples since their size and contents are fixed once they are created.

## 3. Operations Not Available for Tuples

Because tuples are immutable, many operations available for lists, such as `sort()`, `append()`, and `reverse()`, are not available for tuples. If you try to use any of these methods on a tuple, you'll get an `AttributeError`.

For example:
```python
x = (3, 2, 1)
x.sort()  # Raises: AttributeError: 'tuple' object has no attribute 'sort'
```

You need to be aware that once a tuple is created, you cannot modify it. If you need a mutable sequence, use a list instead.

## 4. Tuples are More Efficient

Due to their immutability, tuples can be stored more efficiently in memory than lists. This makes them a good choice when you need to store constant values, especially for temporary data. Python doesn't need to allocate additional memory for changes, which makes tuples faster and less resource-intensive than lists.

Tuples are often used for:
- **Constant values**: Data that should not be changed.
- **Dictionary keys**: Since tuples are immutable, they can be used as keys in dictionaries (lists cannot).

## 5. Multiple Assignments with Tuples

One useful feature of tuples is that they can be used for multiple assignments. This allows you to assign multiple variables at once in a single line of code using **tuple unpacking**.

Example:
```python
(x, y) = (4, 'fred')
print(y)  # Outputs: fred
```

Here, the tuple `(4, 'fred')` is unpacked into two variables: `x` takes the value `4`, and `y` takes `'fred'`. This is particularly useful when working with functions that return multiple values.

## 6. Tuples and Dictionaries

Tuples are commonly used with dictionaries. The `items()` method in a dictionary returns a list of key-value pairs as tuples, which is useful for iterating through the contents of a dictionary.

Example:
```python
d = {'csev': 2, 'cwen': 4}
for k, v in d.items():
    print(k, v)
```

This loop iterates over the dictionary `d`, unpacking each key-value tuple and printing the key (`k`) and value (`v`).

## 7. Comparing Tuples

Tuples can be compared using comparison operators such as `<`, `>`, `==`, and so on. Python compares tuples element by element, starting from the first element. If the first elements are equal, Python moves to the next element and continues the comparison until a difference is found or all elements are compared.

Example:
```python
(0, 1, 2) < (5, 1, 2)  # Outputs: True
```

In this case, Python compares the first element of each tuple (`0` and `5`), and since `0 < 5`, the result is `True`. The remaining elements are not compared.

## 8. Sorting Lists of Tuples

We can sort a list of tuples in Python. When sorting, Python compares the first element of each tuple. If the first elements are equal, Python compares the second elements, and so on.

Example:
```python
d = {'a': 10, 'c': 22, 'b': 1}
print(sorted(d.items()))  # Outputs: [('a', 10), ('b', 1), ('c', 22)]
```

Here, the dictionary is converted into a list of tuples, which is then sorted by the key (the first element of each tuple).

## 9. Using `sorted()`

The `sorted()` function is a built-in function in Python that returns a sorted list from any iterable. It can be used to sort a dictionary’s items or any other sequence of tuples.

Example:
```python
d = {'b': 1, 'c': 22, 'a': 10}
for k, v in sorted(d.items()):
    print(k, v)
```

This code sorts the dictionary by its keys and prints the key-value pairs in alphabetical order.

## 10. Sort by Values Instead of Key

By default, sorting a dictionary sorts by the keys. However, if you want to sort by the values instead, you can reverse the order of the key-value pairs in each tuple. This way, Python will sort by the values.

Example:
```python
tmp = []
for k, v in d.items():
    tmp.append((v, k))
tmp = sorted(tmp, reverse=True)
print(tmp)  # Outputs: [(22, 'c'), (10, 'a'), (1, 'b')]
```

Here, we create a list of tuples where the values come first, and then we sort that list in descending order using `sorted()` with the `reverse=True` option.

## 11. Finding the Top 10 Most Common Words

A practical use case of sorting tuples by value is finding the most common words in a text. After reading a file and counting word occurrences using a dictionary, you can sort the results by frequency and print the top 10 words.

Example:
```python
counts = dict()
for line in fhand:
    words = line.split()
    for word in words:
        counts[word] = counts.get(word, 0) + 1

lst = list()
for key, val in counts.items():
    lst.append((val, key))

lst = sorted(lst, reverse=True)

for val, key in lst[:10]:
    print(key, val)
```

This code counts the occurrences of each word in a file, stores them in a dictionary, and then sorts the dictionary by word frequency, printing the 10 most common words.

## 12. Even Shorter Version: Using List Comprehension

The same process can be done more concisely using **list comprehension**, which allows you to generate the list of tuples in a single line.

Example:
```python
print(sorted([(v, k) for k, v in counts.items()], reverse=True)[:10])
```

This code creates the list of (value, key) tuples directly within the `sorted()` function call, making the entire process more succinct. The `[:10]` slices the list to show only the top 10 most common words.