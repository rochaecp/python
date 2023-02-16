# Python - Beecrowd

### 1101 - Sequência de Números e Soma

~~~python
def swap(x, y):
    if x > y:
        return y, x
    else:
        return x, y

soma = 0

while True:
    linha = input().split(" ")
    x = int(linha[0])
    y = int(linha[1])
    
    if x <= 0 or y <= 0:
        break
    else:
        x, y = swap(x, y)
        for i in range(x, y + 1):
            print("{} ".format(i), end="")
            soma += i
        print("Sum={}".format(soma))
        soma = 0
~~~

### 1113 - Crescente e Decrescente

~~~python
while True:
    x, y = list(map(int, input().split(" ")))
    if x > y:
        print("Decrescente")
    elif x < y:
        print("Crescente")
    else:
        break
~~~

### 1114 - Senha Fixa

~~~python
senhaLida = 0
while senhaLida != 2002:
    senhaLida = int(input())
    if senhaLida != 2002:
        print("Senha Invalida")
else:
    print("Acesso Permitido")
~~~

### 1115 - Quadrante

~~~python
while True:
    x, y = list(map(int, input().split(" ")))
    if x == 0 or y == 0:
        break
    if x > 0 and y > 0:
        print("primeiro")
    elif x < 0 and y > 0:
        print("segundo")
    elif x < 0 and y < 0:
        print("terceiro")
    elif x > 0 and y < 0:
        print("quarto")
~~~

### 1116 - Dividindo X por Y

~~~python
n = int(input())
div = 0.0

while n != 0:
    n -= 1
    x, y = list(map(int, input().split(" ")))
    try:
        div = x / y
        print("{:.1f}".format(div))
    except ZeroDivisionError:
        print("divisao impossivel")
~~~