# Python - Beecrowd

# Lendo uma entrada a partir de um arquivo

- Nome do arquivo com as entradas: entradas.txt
- Comando: 
    - ```cat .\entrada.txt | python .\main.py```
- Arquivo main.py    

~~~python
primeira_linha = input()
print(primeira_linha)
~~~

# Lendo vários valores em uma mesma linha

~~~python
my_line = input().split()
my_list = list(map(int, my_line)) # map function transforms values to integers 
~~~

# Lendo várias linhas

~~~python
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
