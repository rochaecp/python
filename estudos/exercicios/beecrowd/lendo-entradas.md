# Python - Beecrowd

## Lendo uma entrada a partir de um arquivo

- Arquivo **Main.py**:

~~~python
primeira_linha = input()
print(primeira_linha)
~~~

- Para ler a partir de um arquivo **entrada.txt**:

~~~bash
cat .\entrada.txt | python .\Main.py
~~~

## Lendo uma entrada

~~~python
# many values on the same line 
my_line = input().split()
my_list = list(map(int, my_line)) # map function transforms values to integers 

# many values in many lines - lists
my_list = []
for i in range(0, 6): # to read 6 float values
    my_list.append(float(input()))
~~~

## Lendo uma entrada até encontrar um EOF

~~~python
while True:
    try:
        # code here
    except EOFError:
        break
~~~
