# Python - Exercícios

# 1024 - Criptografia

~~~python
n = int(input())

for x in range(0, n):
  linha = input()
  
  lista = list(linha) # converte string em lista

  # primeira passada - incrementa 3 o ascii de letras
  for i in range(0, len(lista)):
    num_letra = int(ord(lista[i]))
    if(num_letra >= 65 and num_letra <= 90) or (num_letra >= 97 and num_letra <= 122):
      lista[i] = chr(num_letra + 3)

  # segunda passada - inverte string
  lista.reverse()

  # terceira passada
  metade = int(len(lista) // 2)
  
  for i in range(metade, len(lista)):
    num_letra = int(ord(lista[i]))
    lista[i] = chr(num_letra - 1)
  
  linha = ''.join(lista)
  print(linha)
~~~

# 1768 - Árvore de Natal

~~~python
def printa_arvore(num_ast):
    qtd_espacos = num_ast // 2
    for qtd in range(1, numero_asteriscos + 1):
        if qtd % 2 != 0:
            print(" " * qtd_espacos + "*" * qtd)
            qtd_espacos -= 1
    qtd_espacos = num_ast // 2
    print(" " * qtd_espacos + "*")
    qtd_espacos -= 1
    print(" " * qtd_espacos + "*" * 3)

# ler entrada até encontrar um EOF
while True:
    try:
        numero_asteriscos = int(input())
        if (numero_asteriscos >= 2 and numero_asteriscos % 2 != 0):
            printa_arvore(numero_asteriscos)
            print()
    except EOFError:
        break
~~~

# 2591 - HameKameKa

~~~python
def retorna_total_as(str):
    str_split_lst = str.split('k')
    num1 = str_split_lst[0].count('a')
    num2 = str_split_lst[1].count('a')
    return num1 * num2

qtd = int(input())

for i in range(0, qtd): 
    entrada = input()
    total = retorna_total_as(entrada)
    print("k" + "a" * total)
~~~

# 2694 - Problema com a Calculadora

~~~python
repeticoes = int(input())

for _ in range(0, repeticoes):
    linha = input()
    x1 = int(''.join(linha[2:4]))
    x2 = int(''.join(linha[5:8]))
    x3 = int(''.join(linha[11:13]))
    print(x1 + x2 + x3)
~~~