# Python - Exercícios

### 1024 - Criptografia

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