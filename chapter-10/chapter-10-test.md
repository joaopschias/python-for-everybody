### Question 1: What is the difference between a Python tuple and Python list?

- A) Tuples can be expanded after they are created and lists cannot
- B) Lists maintain the order of the items and tuples do not maintain order
- C) Lists are indexed by integers and tuples are indexed by strings
- D) **Lists are mutable and tuples are not mutable**

**Explanation**:
- In Python, **lists** are mutable, meaning their elements can be changed, added, or removed after the list is created. On the other hand, **tuples** are immutable, meaning once a tuple is created, it cannot be modified in any way. This is a key distinction between the two.

### Question 2: Which of the following methods work both in Python lists and Python tuples?

- A) **index()**
- B) append()
- C) sort()
- D) reverse()
- E) pop()

**Explanation**:
- The `index()` method works for both **lists** and **tuples** in Python. It returns the index of the first occurrence of a specified value. Other methods like `append()`, `sort()`, `reverse()`, and `pop()` work only on **lists** because lists are mutable, while tuples are not.

### Question 3: What will end up in the variable `y` after this code is executed?

```python
x, y = 3, 4
```

- A) A two item list
- B) A two item tuple
- C) **4**
- D) 3
- E) A dictionary with the key 3 mapped to the value 4

**Explanation**:
- The code assigns `3` to the variable `x` and `4` to the variable `y`. After the execution, the value of `y` will be **4**.

### Question 4: In the following Python code, what will end up in the variable `y`?

```python
x = { 'chuck': 1, 'fred': 42, 'jan': 100 }
y = x.items()
```

- A) A list of strings
- B) **A list of tuples**
- C) A list of integers
- D) A tuple with three integers

**Explanation**:
- The `items()` method in Python returns a view object that displays a **list of tuples**. Each tuple contains a key-value pair from the dictionary. In this case, `y` will contain a list of tuples: `[('chuck', 1), ('fred', 42), ('jan', 100)]`.

### Question 5: Which of the following tuples is greater than `x` in the following Python sequence?

```python
x = (5, 1, 3)
if ??? > x:
    ...
```

- A) (0, 1000, 2000)
- B) (5, 0, 300)
- C) (4, 100, 200)
- D) **(6, 0, 0)**

**Explanation**:
- Python compares tuples element by element. It compares the first element, then the second if the first elements are equal, and so on. In this case, `(6, 0, 0)` is greater than `(5, 1, 3)` because the first element `6` is greater than `5`. All other tuples have smaller or equal first elements.

### Question 6: What does the following Python code accomplish, assuming `c` is a non-empty dictionary?

```python
tmp = list()
for k, v in c.items():
    tmp.append((v, k))
```

- A) It computes the average of all of the values in the dictionary
- B) It sorts the dictionary based on its key values
- C) **It creates a list of tuples where each tuple is a value, key pair**
- D) It computes the largest of all of the values in the dictionary

**Explanation**:
- The code creates an empty list `tmp` and iterates through the dictionary `c`. For each key-value pair in the dictionary, it appends a tuple to `tmp`, but with the value first and the key second. This essentially creates a list of **value-key pairs**.

### Question 7: If the variable `data` is a Python list, how do we sort it in reverse order?

- A) data = sortrev(data)
- B) data.sort.reverse()
- C) **data.sort(reverse=True)**
- D) data = data.sort(-1)

**Explanation**:
- To sort a list in reverse order in Python, you use the `sort()` method with the parameter `reverse=True`. This sorts the list in descending order, modifying the list in place.

### Question 8: Using the following tuple, how would you print 'Wed'?

```python
days = ('Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun')
```

- A) print(days[1])
- B) print(days{2})
- C) print(days(2))
- D) **print(days[2])**
- E) print(days{2})
- F) print(days.get(1, -1))

**Explanation**:
- Tuples in Python are indexed starting at 0. To access 'Wed', which is the third element in the tuple, you need to use index 2. Therefore, the correct syntax is `print(days[2])`.

### Question 9: In the following Python loop, why are there two iteration variables (`k` and `v`)?

```python
c = {'a': 10, 'b': 1, 'c': 22}
for k, v in c.items():
    ...
```

- A) **Because the items() method in dictionaries returns a list of tuples**
- B) Because for each item we want the previous and current key
- C) Because the keys for the dictionary are strings
- D) Because there are two items in the dictionary

**Explanation**:
- The `items()` method in Python dictionaries returns a view object containing **tuples** of key-value pairs. The two iteration variables, `k` and `v`, represent the key and value of each tuple, respectively.

### Question 10: Given that Python lists and Python tuples are quite similar - when might you prefer to use a tuple over a list?

- A) For a list of items that will be extended as new items are found
- B) For a list of items you intend to sort in place
- C) For a list of items that want to use strings as key values instead of integers
- D) **For a temporary variable that you will use and discard without modifying**

**Explanation**:
- Tuples are immutable, meaning they cannot be changed after creation. They are often used for temporary variables or when the data should not be modified. Lists, on the other hand, are mutable and can be modified freely.