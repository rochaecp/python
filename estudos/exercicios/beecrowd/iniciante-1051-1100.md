# Python - Beecrowd

### 1051 - Imposto de Renda

~~~python
salary = float(input())
taxes = 0

if salary >= 0 and salary <= 2000:
    print("Isento")
elif salary > 2000 and salary <= 3000:
    salary = salary - 2000 # isento
    taxes = salary * 0.08
    print("R$ {:.2f}".format(taxes))    
elif salary > 3000 and salary <= 4500: 
    salary = salary - 3000
    taxes = salary * 0.18 + 1000 * 0.08
    print("R$ {:.2f}".format(taxes))
elif salary > 4500:
    salary = salary - 4500
    taxes = salary * 0.28 + 1500 * 0.18 + 1000 * 0.08
    print("R$ {:.2f}".format(taxes))    
~~~

### 1052 - Mês

~~~python
months = {
    '1' : 'January',
    '2' : 'February',
    '3' : 'March',
    '4' : 'April',
    '5' : 'May',
    '6' : 'June',
    '7' : 'July',
    '8' : 'August',
    '9' : 'September',
    '10' : 'October',
    '11' : 'November',
    '12' : 'December'
}

the_month = input()
print(months[the_month])
~~~

### 1059 - Números Pares

~~~python
for i in range(1, 101):
    if i % 2 == 0:
        print(i)
~~~

### 1060 - Números Positivos

~~~python
positives = 0
for i in range(0, 6):
    inp = float(input())
    if inp > 0:
        positives += 1
print("{} valores positivos".format(positives))
~~~

### 1061 - Tempo de um Evento

~~~python
#!/usr/bin/python3

x, d_ini = input().split("Dia ")
h_ini, m_ini, s_ini = input().split(" : ")

x, d_fim = input().split("Dia ")
h_fim, m_fim, s_fim = input().split(" : ")

d_ini = int(d_ini)
h_ini = int(h_ini)
m_ini = int(m_ini)
s_ini = int(s_ini)

d_fim = int(d_fim)
h_fim = int(h_fim)
m_fim = int(m_fim)
s_fim = int(s_fim)

s_tot, m_tot, h_tot, d_tot = 0, 0, 0, 0

if s_fim >= s_ini:
    s_tot = s_fim - s_ini
else:
    s_tot = 60 - s_ini + s_fim
    m_tot -= 1

if m_fim >= m_ini:
    m_tot += m_fim - m_ini
else:
    m_tot += 60 - m_ini + m_fim
    h_tot -= 1

if h_fim >= h_ini:
    h_tot += h_fim - h_ini
else:
    h_tot += 24 - h_ini + h_fim
    d_tot -= 1

if h_tot < 0:
    h_tot = 24 + h_tot
    d_tot -= 1

d_tot += d_fim - d_ini


# saidas
print("{} dia(s)".format(d_tot))
print("{} hora(s)".format(h_tot))
print("{} minuto(s)".format(m_tot))
print("{} segundo(s)".format(s_tot))
~~~

### 1064 - Positivos e Média

~~~python
positivos = 0
qtd_positivos = 0

for i in range(0, 6):
    valor_lido = float(input())
    if valor_lido > 0:
        positivos += valor_lido
        qtd_positivos += 1

print("{} valores positivos".format(qtd_positivos))
print("{:.1f}".format(positivos / qtd_positivos))
~~~

### 1065 - Pares entre Cinco Números

~~~python
pares = 0

for i in range(0, 5):
    valor_lido = int(input())
    if valor_lido % 2 == 0:
        pares += 1

print("{} valores pares".format(pares))
~~~

### 1066 - Pares, Ímpares, Positivos e Negativos

~~~python
pares = 0
impares = 0
positivos = 0
negativos = 0

for i in range(0, 5):
    x = int(input())
    if x % 2 == 0:
        pares += 1
    else:
        impares += 1
    if x > 0:
        positivos += 1
    elif x < 0:
        negativos += 1

print("{} valor(es) par(es)".format(pares))
print("{} valor(es) impar(es)".format(impares))
print("{} valor(es) positivo(s)".format(positivos))
print("{} valor(es) negativo(s)".format(negativos))
~~~

### 1067 - Números Ímpares

~~~python
num = int(input())

for i in range(1, num + 1):
    if i % 2 != 0:
        print(i)
~~~

### 1070 - Seis Números Ímpares

~~~python
x = int(input())
impares = 0
i = x

while impares < 6:
    if i % 2 != 0: 
        impares += 1
        print(i)
    i += 1
~~~

### 1071 - Soma de Impares Consecutivos I

~~~python
def swap(x, y):
    if x <= y:
        return x, y
    else:
        return y, x

x = int(input())
y = int(input())
total = 0

x, y = swap(x, y)

if x == y:
    print("0")
else:
    for i in range(x+1, y):
        if i % 2 != 0:
            total += i

print(total)
~~~

### 1072 - Intervalo 2

~~~python
n = int(input())

in_values = 0
out_values = 0

while n != 0:
    n -= 1
    x = int(input())
    if x >= 10 and x <= 20:
        in_values += 1
    else:
        out_values += 1

print("{} in".format(in_values))
print("{} out".format(out_values))
~~~

### 1073 - Quadrado de Pares

~~~python
n = int(input())
square = 0

for i in range(2, n + 1):
    if i % 2 == 0:
        square = i ** 2
        print("{}^2 = {}".format(i, i ** 2))
~~~

### 1074 - Par ou Ímpar

~~~python
n = int(input())

while n != 0:
    n -= 1
    x = int(input())
    if x == 0:
        print("NULL")
    else:
        if x % 2 == 0:
            saida1 = "EVEN" 
        else:
            saida1 = "ODD"
        if x > 0:
            saida2 = "POSITIVE"
        else:
            saida2 = "NEGATIVE"
        print("{} {}".format(saida1, saida2))
~~~

### 1075 - Resto 2

~~~python
n = int(input())

for i in range(1, 10001):
    if i % n == 2:
        print(i)
~~~

### 1078 - Tabuada

~~~python
n = int(input())
for i in range(1, 11):
    print("{} x {} = {}".format(i, n, i * n))
~~~

### 1079 - Médias Ponderadas

~~~python
n = int(input())
while n != 0:
    n -= 1
    line = input().split(" ")
    x, y, z = float(line[0]), float(line[1]), float(line[2])
    media = (2 * x + 3 * y + 5 * z) / 10
    print("{:.1f}".format(media))
~~~

### 1080 - Maior e Posição

~~~python
maior = 0
index_maior = 0

for i in range(1, 100 + 1):
    num_lido = int(input())
    if num_lido > maior:
        maior = num_lido
        index_maior = i

print(maior)
print(index_maior)
~~~

### 1094 - Experiências

~~~python
total_cobaias = 0
coelhos = 0
ratos = 0
sapos = 0
n = int(input())
while n != 0:
    n -= 1
    linha = input().split(" ")
    if linha[1] == 'C':
        coelhos += int(linha[0])
    elif linha[1] == 'R':
        ratos += int(linha[0])
    elif linha[1] == 'S':
        sapos += int(linha[0])
total_cobaias = coelhos + ratos + sapos
print("Total: {} cobaias".format(total_cobaias))
print("Total de coelhos: {}".format(coelhos))
print("Total de ratos: {}".format(ratos))
print("Total de sapos: {}".format(sapos))
print("Percentual de coelhos: {:.2f} %".format(100 * coelhos / total_cobaias))
print("Percentual de ratos: {:.2f} %".format(100 * ratos / total_cobaias))
print("Percentual de sapos: {:.2f} %".format(100 * sapos / total_cobaias))
~~~

### 1095 - Sequencia IJ 1

~~~python
j = 60
i = 1
while j >= 0:
    print("I={} J={}".format(i, j))
    j -= 5
    i += 3
~~~

### 1096 - Sequencia IJ 2

~~~python
i = 1
while i <= 9:
    print("I={} J=7".format(i))
    print("I={} J=6".format(i))
    print("I={} J=5".format(i))
    i += 2
~~~

### 1097 - Sequencia IJ 3

~~~python
i = 1
a = 7
while i <= 9:
    print("I={} J={}".format(i, a))
    print("I={} J={}".format(i, a - 1))
    print("I={} J={}".format(i, a - 2))
    a += 2
    i += 2
~~~

### 1098 - Sequencia IJ 4

~~~python
i = 0.0
while i <= 2.0:
    if i == 0.0 or i == 1.0 or i > 1.9:
        print("I={:.0f} J={:.0f}".format(i, i + 1))
        print("I={:.0f} J={:.0f}".format(i, i + 2))
        print("I={} J={:.0f}".format(round(i), i + 3))        
    else:
        print("I={:.1f} J={:.1f}".format(i, i + 1))
        print("I={:.1f} J={:.1f}".format(i, i + 2))
        print("I={:.1f} J={:.1f}".format(i, i + 3))
    i += 0.2
~~~

### 1099 - Soma de Ímpares Consecutivos II

~~~python
def swap(a, b):
    if a < b:
        return a, b
    else:
        return b, a

n = int(input())
soma = 0

while n != 0:
    n -= 1
    linha = input().split(" ")
    x = int(linha[0])
    y = int(linha[1])
    x, y = swap(x, y)
    if x != y:
        for i in range(x + 1, y):
            if i % 2 != 0:
                soma += i
    print(soma)
    soma = 0
~~~
