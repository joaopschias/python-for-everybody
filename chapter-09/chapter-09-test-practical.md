
# Practical Exercise: Finding the Most Prolific Sender

## Problem Statement:
Write a program to read through the `mbox-short.txt` file and figure out who has sent the greatest number of mail messages. The program should look for lines starting with 'From ' and take the second word of those lines as the email address of the person who sent the mail. It should then create a Python dictionary that maps the sender's email address to a count of the number of times they appear in the file. Finally, the program should find and print the sender with the highest count.

### Input:
The program should read from the `mbox-short.txt` file.

### Expected Output:
```
cwen@iupui.edu 5
```

---

## Solution:

```python
# Solicitando o nome do arquivo
name = input("Enter file:")
if len(name) < 1:
    name = "mbox-short.txt"

# Abrindo o arquivo
handle = open(name)

# Criando um dicionário para armazenar os remetentes e o número de e-mails
senders = {}

# Iterando pelas linhas do arquivo
for line in handle:
    # Procurando apenas pelas linhas que começam com 'From '
    if line.startswith('From '):
        # Dividindo a linha em palavras
        words = line.split()
        # O remetente é a segunda palavra (o endereço de e-mail)
        sender = words[1]
        # Atualizando o dicionário com a contagem de e-mails
        senders[sender] = senders.get(sender, 0) + 1

# Fechando o arquivo
handle.close()

# Inicializando as variáveis para encontrar o remetente com mais e-mails
max_count = None
max_sender = None

# Iterando pelo dicionário para encontrar o remetente mais ativo
for sender, count in senders.items():
    if max_count is None or count > max_count:
        max_sender = sender
        max_count = count

# Imprimindo o resultado
print(max_sender, max_count)
```

---

## Explanation:

1. **Reading the file**: The program asks for a file name. If no name is provided, it defaults to `mbox-short.txt`.
2. **Processing lines**: It opens the file and processes each line. It only looks for lines starting with `From `, which contain the sender's email.
3. **Extracting email addresses**: The second word in each `From ` line is the email address, which is extracted and counted.
4. **Building the dictionary**: A dictionary is used to keep track of how many times each sender appears in the file.
5. **Finding the top sender**: The dictionary is then processed to find the email address with the highest count.
6. **Printing the result**: Finally, the most prolific sender and their email count is printed.

---

## Output:

Running the program with the file `mbox-short.txt` produces the following output:

```
cwen@iupui.edu 5
```

This means that `cwen@iupui.edu` sent 5 messages, which is the highest number of messages sent by any sender in this file.
