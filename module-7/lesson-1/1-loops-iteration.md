
# Loops and Iterations

## Repeated Steps

In this section, we explore how computers perform repetitive tasks. Loops enable us to repeat actions, often iterating over a sequence of numbers or conditions.

```python
n = 5
while n > 0 :
    print(n)
    n = n - 1
print('Blastoff!')
print(n)
```
This loop counts down from 5 and prints `Blastoff!` after reaching 0. The loop's iteration variable `n` changes each time through the loop.
Output:
```
5
4
3
2
1
Blastoff!
0
```

## Infinite Loop

An infinite loop occurs when the iteration variable is not updated inside the loop, causing it to run indefinitely.

```python
n = 5
while n > 0 :
    print('Lather')
    print('Rinse')
print('Dry off!')
```
In this case, the value of `n` is not decreasing, leading to an infinite loop.

## Breaking Out of a Loop

We can use the `break` statement to exit a loop prematurely:

```python
while True:
    line = input('> ')
    if line == 'done':
        break
    print(line)
print('Done!')
```
When the user inputs `done`, the loop is exited. Otherwise, the input is printed.

## Continuing in a Loop

The `continue` statement skips the remainder of the current iteration and moves to the next iteration.

```python
while True:
    line = input('> ')
    if line[0] == '#':
        continue
    if line == 'done':
        break
    print(line)
print('Done!')
```

If a line starts with `#`, it is ignored and the next iteration starts. The loop continues until the user inputs `done`.

