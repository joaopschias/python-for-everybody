# Loops and Iteration

Loops (repeated steps) have **iteration variables** that change each time through a loop. Often, these iteration variables go through a sequence of numbers.

```python
n = 5
while n > 0 :
    print(n)
    n = n - 1
print('Blastoff!')
```

### Output:
```
5
4
3
2
1
Blastoff!
0
```

---

## An Infinite Loop

An infinite loop occurs when the iteration variable is not updated in the loop, causing the condition to never become false.

```python
n = 5
while n > 0 :
    print('Lather')
    print('Rinse')
print('Dry off!')
```

### What is wrong with this loop?

- The value of `n` is never changed, causing the loop to run infinitely.

---

## Breaking Out of a Loop

The `break` statement ends the current loop and jumps to the statement immediately following the loop. It’s like a loop test that can happen anywhere in the body of the loop.

```python
while True:
    line = input('> ')
    if line == 'done' :
        break
    print(line)
print('Done!')
```

### Output:
```
> hello there
hello there
> finished
finished
> done
Done!
```

---

## Continue Statement

The `continue` statement ends the current iteration and jumps to the top of the loop, starting the next iteration.

```python
while True:
    line = input('> ')
    if line[0] == '#' :
        continue
    if line == 'done' :
        break
    print(line)
print('Done!')
```

### Output:
```
> hello there
hello there
> # don't print this
> print this!
print this!
> done
Done!
```

---

Next, we'll discuss **definite loops** using the `for` statement.