
# Practical Exercise: Hourly Message Distribution from `mbox-short.txt`

## Problem Statement:
Write a program to read through the `mbox-short.txt` file and determine the distribution of messages by the hour of the day. The program should extract the hour from the 'From ' lines in the file, and count the occurrences of each hour. Finally, the program should print the counts, sorted by hour.

### Input:
The program should read from the `mbox-short.txt` file.

### Expected Output:
```
04 3
06 1
07 1
09 2
10 3
11 6
14 1
15 2
16 4
17 2
18 1
19 1
```

---

## Solution:

```python
# Solicita o nome do arquivo e define um arquivo padrão
name = input("Enter file:")
if len(name) < 1:
    name = "mbox-short.txt"

# Abre o arquivo
handle = open(name)

# Dicionário para armazenar a contagem de horas
hours_count = {}

# Itera pelas linhas do arquivo
for line in handle:
    # Procura as linhas que começam com 'From '
    if line.startswith('From '):
        # Divide a linha em palavras
        words = line.split()
        # Pega a parte que contém a hora (quinto item)
        time = words[5]
        # Divide o tempo no formato HH:MM:SS e pega a hora
        hour = time.split(':')[0]
        # Atualiza o dicionário com a contagem da hora
        hours_count[hour] = hours_count.get(hour, 0) + 1

# Fecha o arquivo
handle.close()

# Ordena o dicionário por hora e imprime a saída
for hour, count in sorted(hours_count.items()):
    print(hour, count)
```

---

## Explanation:

1. **Opening the File**: The program asks for a file name, defaulting to `mbox-short.txt` if no input is provided.
2. **Processing Lines**: It iterates through each line, looking for those that start with `From `, which indicate email metadata lines.
3. **Extracting the Hour**: It splits the line by spaces, taking the 5th word, which contains the time in `HH:MM:SS` format. The hour is extracted by splitting this time string by the colon (`:`).
4. **Counting Occurrences**: A dictionary is used to count how many times each hour appears.
5. **Sorting and Printing**: The dictionary is then sorted by hour and printed in ascending order.

---

## Output:

Running the program with the file `mbox-short.txt` produces the following output:

```
04 3
06 1
07 1
09 2
10 3
11 6
14 1
15 2
16 4
17 2
18 1
19 1
```

This output shows the number of email messages sent during each hour, sorted by hour.
