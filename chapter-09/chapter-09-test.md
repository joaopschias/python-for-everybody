
# Study List

## Questions with Explanations

### Question 1: How are Python dictionaries different from Python lists?

A) Python lists can store strings and dictionaries can only store words  
B) **Python lists are indexed using integers and dictionaries can use strings as indexes**  
C) Python lists store multiple values and dictionaries store a single value  
D) Python dictionaries are a collection and lists are not a collection

**Explanation**: Python lists are ordered collections indexed by integers, while dictionaries use custom keys, such as strings, to map to values.

```python
my_list = [10, 20, 30]
print(my_list[1])  # Output: 20

my_dict = {'name': 'Alice', 'age': 25}
print(my_dict['name'])  # Output: Alice
```

---

### Question 2: What is a term commonly used to describe the Python dictionary feature in other programming languages?

A) Closures  
B) Iterables  
C) **Associative arrays**  
D) Lambdas

**Explanation**: Python dictionaries are often referred to as **associative arrays** in other languages, such as PHP.

```php
$my_array = ["name" => "Alice", "age" => 25];
echo $my_array["name"];  // Output: Alice
```

---

### Question 3: What would the following Python code print out?

```python
stuff = dict()
print(stuff['candy'])
```

A) 0  
B) None  
C) **It would fail with a traceback**  
D) 'candy'

**Explanation**: Accessing a non-existent key without using `get()` raises a **KeyError**.

```python
my_dict = {}
print(my_dict['candy'])  # KeyError: 'candy'
```

---

### Question 4: What would the following Python code print out?

```python
stuff = dict()
print(stuff.get('candy', -1))
```

A) 0  
B) None  
C) **-1**  
D) 'candy'

**Explanation**: The `get()` method safely returns a default value if the key does not exist, avoiding a **KeyError**.

```python
my_dict = {}
print(my_dict.get('candy', -1))  # Output: -1
```

---

### Question 5: Which of the following is a common use of Python dictionaries?

A) Storing a list of ordered values  
B) **Building a histogram counting the occurrences of various strings in a file**  
C) Sorting a list of names into alphabetical order  
D) Calculating an average of a list of numbers

**Explanation**: Python dictionaries are often used to build histograms that count the occurrences of items.

```python
word_count = {}
words = ['apple', 'banana', 'apple']
for word in words:
    word_count[word] = word_count.get(word, 0) + 1
print(word_count)  # Output: {'apple': 2, 'banana': 1}
```

---

### Question 6: Which line of code is equivalent to the following sequence of statements assuming that `counts` is a dictionary?

```python
if key in counts:
    counts[key] = counts[key] + 1
else:
    counts[key] = 1
```

A) counts[key] = counts[key] + 1  
B) **counts[key] = counts.get(key, 0) + 1**  
C) counts.get(key, 0) = counts[key] + 1  
D) counts[key] = (key in counts) + 1

**Explanation**: The line `counts[key] = counts.get(key, 0) + 1` is a concise equivalent to checking if a key exists and incrementing it if it does, or initializing it if it doesn't.

```python
counts[key] = counts.get(key, 0) + 1
```

---

### Question 7: In the following Python code, what does the `for` loop iterate through?

```python
x = { "a": 1, "b": 2, "c": 3 }
for y in x:
    print(y)
```

A) It loops through the values in the dictionary  
B) It loops through the keys and values in the dictionary  
C) It loops through the integers in the range from 0 to len(x)  
D) **It loops through the keys in the dictionary**

**Explanation**: A `for` loop over a dictionary iterates over its **keys**.

```python
my_dict = {'apple': 1, 'banana': 2}
for key in my_dict:
    print(key)  # Output: apple, banana
```

---

### Question 8: Which method in a dictionary object gives you a list of the values in the dictionary?

A) keys()  
B) **values()**  
C) items()  
D) all()

**Explanation**: The `values()` method returns a list-like object containing the values of the dictionary.

```python
my_dict = {'apple': 1, 'banana': 2}
print(list(my_dict.values()))  # Output: [1, 2]
```

---

### Question 9: What is the purpose of the second parameter of the `get()` method for Python dictionaries?

A) To set the value of the key in the dictionary  
B) To return a default value if the key is not found  
C) To remove a key from the dictionary  
D) **To provide a default value if the key is not found**

**Explanation**: The second parameter of `get()` provides a **default value** if the key is not found.

```python
my_dict = {'apple': 1}
print(my_dict.get('banana', 0))  # Output: 0
```

