# Python - Tuplas

- Uma tupla é uma coleção ordenada e não modificável.
- Permite elementos duplicados.
- Para modificar uma tupla podemos transformá-la em uma lista.

## Criando uma tupla

~~~python
my_tuple = ("apple", "banana", "cherry")
~~~

Construtor:
- Observe os parênteses repetidos

~~~python
my_tuple = tuple(("apple", "banana", "cherry")) 
myTuple = tuple((1, 2, 3, 4))
my_tuple = tuple(my_list)
~~~

## Acessando elementos de uma tupla

Acessando um elemento da tupla:

~~~python
item = my_tuple[0] # first
item = my_tuple[-1] # last 
~~~

Acessando um range da tupla:

~~~python
my_tuple = my_tuple[0:3]
~~~

Acessando todos elementos da tupla:

~~~python
my_tuple = ("apple", "banana", "cherry")
for x in my_tuple:
    print(x)
~~~

~~~python
my_tuple = ("apple", "banana", "cherry")
for i in range(len(my_tuple)):
    print(my_tuple[i])
~~~

~~~python
my_tuple = ("apple", "banana", "cherry")
i = 0
while i < len(my_tuple):
    print(my_tuple[i])
    i = i + 1 
~~~

## Verificando se um elemento existe na tupla

~~~python
my_bool = "apple" in my_tuple
~~~

## Procurando um elemento na tupla:

~~~python
my_index = my_tuple.index("myValue") # finds the first occurrence of the specified value
~~~

## Modificando valores de uma tupla

~~~python
my_tuple = ("apple", "banana", "cherry")
my_list = list(my_tuple) # convert into lista
my_list[1] = "kiwi"
my_tuple = tuple(my_list)
~~~

## Juntando duas tuplas

~~~python
my_tuple = ("apple", "banana", "cherry")
my_tuple2 = ("orange",)
my_tuple += my_tuple2
~~~

~~~python
my_tuple3 = my_tuple1 + my_tuple2
~~~

## Unpacking

~~~python
fruits = ("apple", "banana", "cherry")
(green, yellow, red) = fruits # "unpacking" == extract the values back into variables
~~~

~~~python
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")
(green, yellow, *red) = fruits # red == list
~~~

## Multiplicando valores de uma tupla

~~~python
fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2
~~~

## Obtendo o tamanho de uma tupla

~~~python
my_len = len(my_tuple)
~~~

## Contando quantas vezes um elemento aparece na tupla:

~~~python
my_count = my_tuple.count("myValue") 
~~~

## Obtendo o maior elemento de uma tupla

~~~python
my_max = max(my_tuple)
~~~

## Obtendo o menor elemento de uma tupla

~~~python
my_min = min(my_tuple)
~~~




