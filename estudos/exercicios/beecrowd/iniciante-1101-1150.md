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

### 1117 - Validação de Nota

~~~python
media = 0
notas_validas = []

while len(notas_validas) < 2:
    try:
        nota = float(input())
        
        if nota < 0 or nota > 10:
            print("nota invalida")
        else:
            notas_validas.append(nota)
    except ValueError:
        break

media = sum(notas_validas) / 2
print(f"media = {media:.2f}")
~~~

### 1118 - Várias Notas Com Validação

~~~python
notas_validas = []
ind_continua = True
media = 0

while ind_continua:
    try:
        nota = float(input())
        if nota < 0 or nota > 10:
            print("nota invalida")
        else:
            notas_validas.append(nota)
            if len(notas_validas) == 2:
                media = sum(notas_validas) / 2
                print(f"media = {media:.2f}")
                
                opcao = 0
                notas_validas = []
                while opcao != 1 or opcao !=2:
                    print("novo calculo (1-sim 2-nao)")
                    opcao = int(input())
                    if opcao == 1:
                        break
                    elif opcao == 2:
                        ind_continua = False
                        break
    except ValueError:
        break
~~~

~~~python
# solução de um chatbot
while True:
    notas_validas = []

    # Ler e validar notas
    while len(notas_validas) < 2:
        try:
            nota = float(input())
            if 0 <= nota <= 10:
                notas_validas.append(nota)
            else:
                print("nota invalida")
        except ValueError:
            print("nota invalida")

    # Calcular e exibir a média
    media = sum(notas_validas) / 2
    print(f"media = {media:.2f}")

    # Solicitar novo cálculo
    while True:
        print("novo calculo (1-sim 2-nao)")
        try:
            opcao = int(input())
            if opcao == 1:
                break  # Reinicia o programa
            elif opcao == 2:
                exit()  # Encerra o programa
        except ValueError:
            pass  # Continue no loop até o usuário digitar 1 ou 2

~~~

### 1131 - Grenais

~~~python

~~~

### 1132 - Múltiplos de 13

~~~python

~~~

### 1133 - Resto da Divisão

~~~python

~~~

### 1134 - Tipo de Combustível

~~~python

~~~

### 1142 - PUM

~~~python

~~~

### 1143 - Quadrado e ao Cubo

~~~python

~~~

### 1144 - Sequência Lógica

~~~python

~~~

### 1145 - Sequência Lógica 2

~~~python

~~~

### 1146 - Sequências Crescentes

~~~python

~~~

### 1149 - Somando Inteiros Consecutivos

~~~python

~~~

### 1150 - Ultrapassando Z

~~~python

~~~