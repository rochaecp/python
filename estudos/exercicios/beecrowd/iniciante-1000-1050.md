# Python - Beecrowd

### 1000 - Hello World! 

~~~python
print("Hello World!")
~~~

### 1001 - Extremamente Básico

~~~python
a = int(input())
b = int(input())
x = str(a + b)
print("X = " + x)
~~~
      
### 1002 - Área do Círculo

~~~python
r = float(input())
a = 3.14159 * r * r
print("A=%0.4f" %a)
~~~
      
### 1003 - Soma Simples 

~~~python
a = int(input())
b = int(input())
soma = a + b
print("SOMA = {}".format(soma))
~~~
      
### 1004 - Produto Simples 

~~~python
a = int(input())
b = int(input())
prod = a * b
print("PROD = %i" %prod)
~~~
      
### 1005 - Média 1 

~~~python
a = float(input())
b = float(input())
media = (3.5 * a + 7.5 * b) / 11
print("MEDIA = %.5f" %media)
~~~
      
### 1006 - Média 2 

~~~python
a = float(input())
b = float(input())
c = float(input())
media = (2 * a + 3 * b + 5 * c) / 10
print("MEDIA = {:.1f}".format(media))
~~~
      
### 1007 - Diferença 

~~~python
a = int(input())
b = int(input())
c = int(input())
d = int(input())
dif = a * b - c * d
print("DIFERENCA = {}".format(dif))
~~~
      
### 1008 - Salário 

~~~python
s = h * v
print("NUMBER = {}".format(n))
print("SALARY = U$ {:.2f}".format(s))
~~~
      
### 1009 - Salário com Bônus 

~~~python
name = input()
salary = float(input())
v = float(input())
tot = salary + 0.15 * v
print("TOTAL = R$ {:.2f}".format(tot))
~~~

### 1010 - Cálculo simples 

~~~python
linha1 = input().split(" ")
linha2 = input().split(" ")
cod1 = int(linha1[0])
num1 = int(linha1[1])
val1 = float(linha1[2])
cod2 = int(linha2[0])
num2 = int(linha2[1])
val2 = float(linha2[2])
valor = num1 * val1 + num2 * val2
print("VALOR A PAGAR: R$ {:.2f}".format(valor))
~~~

### 1011 - Esfera 

~~~python
r = float(input())
v = (4 / 3) * 3.14159 * r ** 3
print("VOLUME = {:.3f}".format(v))
~~~

### 1012 - Área 

~~~python
linha = input().split()
a = float(linha[0])
b = float(linha[1])
c = float(linha[2])
at = a * c / 2
ac = 3.14159 * c ** 2
atrap = (a + b) * c / 2
aq = b ** 2
ar = a * b
print("TRIANGULO: {:.3f}\nCIRCULO: {:.3f}\nTRAPEZIO: {:.3f}\nQUADRADO: {:.3f}\nRETANGULO: {:.3f}".format(at, ac, atrap, aq, ar))
~~~

### 1013 - O Maior 

~~~python
linha = input().split(" ")
a = int(linha[0])
b = int(linha[1])
c = int(linha[2])
maiorAB = (a + b + abs(a - b)) / 2

if maiorAB > c:
	maior = maiorAB
else:
	maior = c

maior = int(maior)
print("{} eh o maior".format(maior))
~~~

### 1014 - Consumo 

~~~python
d = int(input())
comb = float(input())
consumo = d / comb
print("{:.3f} km/l".format(consumo))
~~~

### 1015 - Distância entre dois pontos 

~~~python
linha1 = input().split(" ")
linha2 = input().split(" ")
x1 = float(linha1[0])
y1 = float(linha1[1])
x2 = float(linha2[0])
y2 = float(linha2[1])
d = (((x2 - x1) ** 2) + ((y2 - y1) ** 2)) ** 0.5
print("{:.4f}".format(d))
~~~

### 1016 - Distância 

~~~python
d = int(input())
t = 2 * d
print("{} minutos".format(t))
~~~

### 1017 - Gasto de Combustível 

~~~python
t = int(input())
v = int(input())
d = v * t
l = d / 12
print("{:.3f}".format(l))
~~~

### 1018 - Cédulas 

~~~python
v = int(input())

print(v)

n100 = n50 = n20 = n10 = n5 = n2 = n1 = 0
n100 = v // 100
v = v - n100 * 100
n50 = v // 50
v = v - n50 * 50
n20 = v // 20
v = v - n20 * 20
n10 = v // 10
v = v - n10 * 10
n5 = v // 5
v = v - n5 * 5
n2 = v // 2
v = v - n2 * 2
n1 = v
print("{} nota(s) de R$ 100,00".format(n100))
print("{} nota(s) de R$ 50,00".format(n50))
print("{} nota(s) de R$ 20,00".format(n20))
print("{} nota(s) de R$ 10,00".format(n10))
print("{} nota(s) de R$ 5,00".format(n5))
print("{} nota(s) de R$ 2,00".format(n2))
print("{} nota(s) de R$ 1,00".format(n1))
~~~

### 1019 - Conversão de Tempo 

~~~python
n = int(input())
h = n // 3600
n = n - h*3600
m = n // 60
n = n - m*60
s = n
print("{}:{}:{}".format(h, m, s))
~~~

### 1020 - Idade em dias

~~~python
n = int(input())

a = n // 365 
n = n - a * 365
m = n // 30
n = n - m * 30
d = n
print("{} ano(s)\n{} mes(es)\n{} dia(s)".format(a, m, d))
 
~~~

### 1021 - Notas e moedas

~~~python
v = float(input())

n100 = n50 = n20 = n10 = n5 = n2 = n1 = 0

n100 = int(v // 100)
v = v - n100 * 100

n50 = int(v // 50)
v = v - n50 * 50

n20 = int(v // 20)
v = v - n20 * 20

n10 = int(v // 10)
v = v - n10 * 10

n5 = int(v // 5)
v = v - n5 * 5

n2 = int(v // 2)
v = v - n2 * 2

moeda1 = int(v // 1)
v = v - moeda1
v = int(100 * v)

moeda50 = v // 50
v = v - moeda50 * 50

moeda25 = v // 25
v = v - moeda25 * 25

moeda10 = v // 10
v = v - moeda10 * 10

moeda5 = v // 5
v = v - moeda5 * 5

moeda01 = v

print("NOTAS:")
print("{} nota(s) de R$ 100.00".format(n100))
print("{} nota(s) de R$ 50.00".format(n50))
print("{} nota(s) de R$ 20.00".format(n20))
print("{} nota(s) de R$ 10.00".format(n10))
print("{} nota(s) de R$ 5.00".format(n5))
print("{} nota(s) de R$ 2.00".format(n2))

print("MOEDAS:")
print("{} moeda(s) de R$ 1.00".format(moeda1))
print("{} moeda(s) de R$ 0.50".format(moeda50))
print("{} moeda(s) de R$ 0.25".format(moeda25))
print("{} moeda(s) de R$ 0.10".format(moeda10))
print("{} moeda(s) de R$ 0.05".format(moeda5))
print("{} moeda(s) de R$ 0.01".format(moeda01))
~~~

### 1035 - Teste de Seleção 1

~~~python
linha = input().split(" ")
a, b, c, d = int(linha[0]), int(linha[1]), int(linha[2]), int(linha[3])

if b > c and d > a and (c + d) > (a + b) and c > 0 and d > 0 and a % 2 == 0:
    print("Valores aceitos")
else:
    print("Valores nao aceitos")
~~~

### 1036 - Fórmula de Bhaskara

~~~python
linha = input().split(" ")

a = float(linha[0])
b = float(linha[1])
c = float(linha[2])

delta = b ** 2 - 4 * a * c

if delta < 0 or a == 0:
  print("Impossivel calcular")
else:
  x1 = (-b + delta ** 0.5 ) / (2 * a)
  x2 = (-b - delta ** 0.5 ) / (2 * a)
  print("R1 = {:.5f}\nR2 = {:.5f}".format(x1, x2))
~~~

### 1037 - Intervalo

~~~python
n = float(input())

if n >= 0 and n <= 25:
  print("Intervalo [0,25]")
elif n > 25 and n <= 50:
  print("Intervalo (25,50]")
elif n > 50 and n <= 75:
  print("Intervalo (50,75]")
elif n > 75 and n <= 100:
  print("Intervalo (75,100]")
else:
  print("Fora de intervalo")
~~~

### 1038 - Lanche

~~~python
linha = input().split(" ")
codigo, quantidade = linha[0], int(linha[1])

if codigo == '1':
  preco = 4.00
elif codigo == '2':
  preco = 4.50
elif codigo == '3':
  preco = 5.0
elif codigo == '4':
  preco = 2.0
elif codigo == '5':
  preco = 1.5  

total = preco * quantidade
print("Total: R$ {:.2f}".format(total))
~~~

### 1040 - Média 3

~~~python
linha = input().split(" ")
n1, n2, n3, n4 = float(linha[0]), float(linha[1]), float(linha[2]), float(linha[3])
media = (2 * n1 + 3 * n2 + 4 * n3 + 1 * n4) / 10

print("Media: {:.1f}".format(media))

if media >= 7.0:
  print("Aluno aprovado.")
elif media < 5.0:
  print("Aluno reprovado.")
elif media >= 5.0 and media < 7.0:
  print("Aluno em exame.")
  nexame = float(input())

  print("Nota do exame: {:.1f}".format(nexame))
  media = (media + nexame) / 2
  if media >= 5.0:
    print("Aluno aprovado.")
  elif media < 4.0:
    print("Aluno reprovado.")
  print("Media final: {:.1f}".format(media))
~~~

### 1041 - Coordenadas de um Ponto

~~~python
linha = input().split(" ")
x, y = float(linha[0]), float(linha[1])

if x == 0.0 and y ==  0.0:
	print("Origem")
elif x != 0.0 and y == 0.0:
	print("Eixo X")
elif y != 0.0 and x == 0.0:
	print("Eixo Y")
elif x > 0.0 and y > 0.0:
	print("Q1")
elif x < 0.0 and y > 0.0:
	print("Q2")
elif x < 0.0 and y < 0.0:
	print("Q3")
elif x > 0.0 and y < 0.0:
	print("Q4")
~~~

### 1042 - Sort Simples

~~~python
linha = input().split(" ")
lista = []
lista = [int(linha[0]), int(linha[1]), int(linha[2])]
lista_ordenada = lista.copy()
lista_ordenada.sort()

for i in lista_ordenada:
	print(i)

print()
	
for i in lista:
	print(i)
~~~

### 1043 - Triângulo

~~~python
linha = input().split(" ")
a, b, c = float(linha[0]), float(linha[1]), float(linha[2])

if (a + b) == c or (a + c) == b or (c + b) == a:
	print("Area = {:.1f}".format(((a + b) * c) / 2))
else:
	print("Perimetro = {:.1f}".format(a + b + c))
~~~

### 1044 - Múltiplos

~~~python

~~~

### 1045 - Tipos de Triângulos

~~~python
linha = input().split(" ")
lista = [float(linha[0]), float(linha[1]), float(linha[2])]

lista.sort()
lista.reverse()

a, b, c = lista

str_out2 = ''

if a >= b + c: 
	str_out = "NAO FORMA TRIANGULO"
elif (a ** 2) == (b ** 2 + c **2):
	str_out = "TRIANGULO RETANGULO"
elif (a ** 2) > (b ** 2 + c **2):
	str_out = "TRIANGULO OBTUSANGULO"
elif (a ** 2) < (b ** 2 + c **2):
	str_out = "TRIANGULO ACUTANGULO"

if a == b and b == c:
	str_out2 = "TRIANGULO EQUILATERO"
elif (a == b and a != c) or (a == c and a != b) or (b == c and b != a): 
	str_out2 = "TRIANGULO ISOSCELES"

print(str_out)
if str_out2 != '':
	print(str_out2)
~~~

### 1046 - Tempo de Jogo

~~~python
linha = input().split(" ")
h_ini, h_fim = int(linha[0]), int(linha[1])


duracao = 24 - h_ini + h_fim

if duracao > 24:
  duracao = duracao % 24

print("O JOGO DUROU {} HORA(S)".format(duracao))
~~~

### 1047 - Tempo de Jogo com Minutos

~~~python
linha = input().split(" ")
hI, mI, hF, mF = int(linha[0]), int(linha[1]), int(linha[2]), int(linha[3])
 
hT = hF - hI

if hT < 0:
  hT += 24

mT = mF - mI

if mT < 0: 
  mT += 60
  hT -= 1
  if hT < 0:
    hT += 24

if mT == 0 and hT == 0:
  print("O JOGO DUROU 24 HORA(S) E 0 MINUTO(S)")
else:
  print("O JOGO DUROU {} HORA(S) E {} MINUTO(S)".format(hT, mT))


~~~

### 1048 - Aumento de Salário

~~~python
def set_salary_increase(salary):
	if salary >= 0 and salary <= 400.0:
		return 0.15
	elif salary > 400.0 and salary <= 800.0:
		return 0.12
	elif salary > 800.0 and salary <= 1200.0:
		return 0.10
	elif salary > 1200.0 and salary <= 2000.0:
		return 0.07
	elif salary > 2000.0:
		return 0.04

salary = float(input())
increase_perc = set_salary_increase(salary)
salary_increase = salary * (1 + increase_perc)

print("Novo salario: {:.2f}".format(salary_increase))
print("Reajuste ganho: {:.2f}".format(salary_increase - salary))
print("Em percentual: {:.0f} %".format(increase_perc * 100))
~~~

### 1049 - Animal

~~~python
def define_type(t1, t2, t3):
  if t1 == "vertebrado":
    if t2 == "ave":
      if t3 == "carnivoro":
        return "aguia"
      elif t3 == "onivoro":
        return "pomba"
    elif t2 == "mamifero":
      if t3 == "onivoro":
        return "homem"
      elif t3 == "herbivoro":
        return "vaca"
  elif t1 == "invertebrado":
    if t2 == "inseto":
      if t3 == "hematofago":
        return "pulga"
      elif t3 == "herbivoro":
        return "lagarta"
    elif t2 == "anelideo":
      if t3 == "hematofago":
        return "sanguessuga"
      elif t3 == "onivoro":
        return "minhoca"

type1 = input()
type2 = input()
type3 = input()

print(define_type(type1, type2, type3))
~~~

### 1050 - 	DDD

~~~python
ddd = {
  61: 'Brasilia',
  71: 'Salvador',
  11: 'Sao Paulo',
  21: 'Rio de Janeiro',
  32: 'Juiz de Fora',
  19: 'Campinas',
  27: 'Vitoria',
  31: 'Belo Horizonte'
}

ddd_input = int(input())

try:
  print(ddd[ddd_input])
except KeyError:
  print('DDD nao cadastrado')
~~~