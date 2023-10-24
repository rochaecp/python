# Tuplas

- Uma tupla é uma coleção ordenada e não modificável.  
- Permite elementos duplicados.  
- Para modificar uma tupla podemos transformá-la em uma lista.  

## Criar uma tupla

~~~python
minha_tupla = ("pera", "uva", "melancia")
~~~

#### Construtor (observe os parênteses repetidos)  

~~~python
minha_tupla = tuple(("pera", "uva", "melancia")) 
minha_tupla = tuple((1, 2, 3, 4))
minha_tupla = tuple(minha_lista)
~~~

## Acessar elementos de uma tupla

Acessar um elemento de uma tupla:

~~~python
minha_tupla = ("pera", "uva", "melancia")
item = minha_tupla[0]   # pera
item = minha_tupla[-1]  # melancia 
~~~

#### Acessar uma fatia de uma tupla

~~~python
minha_tupla = ("pera", "uva", "melancia")
minha_tupla = minha_tupla[0:2] # ('pera', 'uva')
~~~

#### Acessar todos elementos de uma tupla

~~~python
minha_tupla = ("pera", "uva", "melancia")
for x in minha_tupla:
    print(x)
~~~

~~~python
minha_tupla = ("pera", "uva", "melancia")
for i in range(len(minha_tupla)):
    print(minha_tupla[i])
~~~

~~~python
minha_tupla = ("pera", "uva", "melancia")
i = 0
while i < len(minha_tupla):
    print(minha_tupla[i])
    i = i + 1 
~~~

## Verificar se um elemento existe na tupla

~~~python
minha_tupla = ("pera", "uva", "melancia")
my_bool = "pera" in minha_tupla
~~~

## Procurar um elemento na tupla:

~~~python
minha_tupla = ("pera", "uva", "melancia")
my_index = minha_tupla.index("melancia") 
~~~

## Modificar valores de uma tupla

~~~python
minha_tupla = ("pera", "uva", "melancia")
minha_lista = list(minha_tupla)
minha_lista[1] = "morango"
minha_tupla = tuple(minha_lista)
~~~

## Juntar duas tuplas

~~~python
minha_tupla = ("pera", "uva", "melancia")
minha_tupla_2 = ("laranja",)
minha_tupla += minha_tupla_2
~~~

~~~python
minha_tupla3 = minha_tupla1 + minha_tupla_2
~~~

## Unpacking

~~~python
fruits = ("pera", "uva", "melancia")
(amarela, roxa, verde) = fruits # "unpacking"
~~~

~~~python
fruits = ("pera", "melancia", "morango", "cereja")
(amarela, verde, *red) = fruits # red == list
~~~

## Multiplicar valores de uma tupla

~~~python
fruits = ("pera", "uva", "melancia")
minha_tupla = fruits * 2
~~~

## Obtendo o tamanho de uma tupla

~~~python
tamanho = len(minha_tupla)
~~~

## Contar quantas vezes um elemento aparece na tupla:

~~~python
total = minha_tupla.count("melancia") 
~~~

## Obtendo o maior elemento de uma tupla

~~~python
maior = max(minha_tupla)
~~~

## Obtendo o menor elemento de uma tupla

~~~python
menor = min(minha_tupla)
~~~