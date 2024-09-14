
# Loop Idioms in Python

Loop idioms allow us to perform specific tasks inside a loop, such as counting, summing, or filtering values. These idioms are useful when working with loops in Python, as they help to simplify and standardize the processes of collecting or evaluating data.

## Counting in a Loop

The idea of **counting in a loop** is simple. We introduce a **counter variable** that starts at 0 and we increment it each time the loop iterates over an element.

### Example of counting elements in a list:
```python
zork = 0
print('Before', zork)
for thing in [9, 41, 12, 3, 74, 15]:
    zork = zork + 1
    print(zork, thing)
print('After', zork)
```

### Output:
```
Before 0
1 9
2 41
3 12
4 3
5 74
6 15
After 6
```

In this example, the variable `zork` acts as the counter, and we increment it by 1 during each iteration of the loop. At the end of the loop, `zork` will store the total number of iterations.

## Summing in a Loop

Another common pattern is **summing values** in a loop. We introduce a **sum variable** that starts at 0, and during each iteration, we add the current value to the sum.

### Example of summing values in a list:
```python
zork = 0
print('Before', zork)
for thing in [9, 41, 12, 3, 74, 15]:
    zork = zork + thing
    print(zork, thing)
print('After', zork)
```

### Output:
```
Before 0
9 9
50 41
62 12
65 3
139 74
154 15
After 154
```

In this example, `zork` acts as the running total. The loop adds each element to `zork`, resulting in the total sum after all iterations.

## Finding the Average in a Loop

**Finding an average** combines the counting and summing idioms. We count how many values are processed and sum them, then divide the sum by the count to get the average.

### Example of finding the average:
```python
count = 0
sum = 0
print('Before', count, sum)
for value in [9, 41, 12, 3, 74, 15]:
    count = count + 1
    sum = sum + value
    print(count, sum, value)
print('After', count, sum, sum / count)
```

### Output:
```
Before 0 0
1 9 9
2 50 41
3 62 12
4 65 3
5 139 74
6 154 15
After 6 154 25.666666666666668
```

Here, we maintain both a counter (`count`) and a running total (`sum`). After the loop finishes, the average is computed by dividing `sum` by `count`.

## Filtering in a Loop

Sometimes, we only want to process values that meet certain criteria. **Filtering** involves using an `if` statement within a loop to only act on values that satisfy a condition.

### Example of filtering large numbers:
```python
print('Before')
for value in [9, 41, 12, 3, 74, 15]:
    if value > 20:
        print('Large number:', value)
print('After')
```

### Output:
```
Before
Large number: 41
Large number: 74
After
```

In this example, the `if` statement filters out numbers less than or equal to 20, only printing the larger numbers.

## Searching with a Boolean Variable

If we want to **search** for a specific value in a loop, we can use a **boolean variable** to track whether we’ve found it.

### Example of searching for a specific value:
```python
found = False
print('Before', found)
for value in [9, 41, 12, 3, 74, 15]:
    if value == 3:
        found = True
    print(found, value)
print('After', found)
```

### Output:
```
Before False
False 9
False 41
False 12
True 3
True 74
True 15
After True
```

In this example, the variable `found` starts as `False` and is set to `True` when the loop encounters the value `3`.

## Finding the Smallest Value

To **find the smallest value** in a sequence, we initialize a variable to hold the smallest value we have seen so far. We then compare each new value to this stored value and update it if the new value is smaller.

### Example:
```python
smallest = None
print('Before')
for value in [9, 41, 12, 3, 74, 15]:
    if smallest is None:
        smallest = value
    elif value < smallest:
        smallest = value
    print(smallest, value)
print('After', smallest)
```

### Output:
```
Before
9 9
9 41
9 12
3 3
3 74
3 15
After 3
```

In this example, the `smallest` variable starts as `None`. The first value encountered is stored as the smallest, and subsequent values are compared against it to find the smallest overall value.