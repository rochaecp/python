# Python - Exercícios

### 1026 - Carrega ou não Carrega?

~~~python
while True:
  try:
    linha = input().split(" ")
    a = int(linha[0])
    b = int(linha[1])
    c = a ^ b
    print(c)
  except EOFError:
    break
~~~