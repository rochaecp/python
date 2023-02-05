# Python - Listas

- Listas são usadas para gravar múltiplos itens em uma mesma variável.
- Permitem: gravar itens de maneira ordenada, modificar os itens, itens duplicados.
- No Python, são objetos do tipo list.
- Não se pode copiar uma lista fazendo apenas ``` list2 = list1 ```. É necessário usar o método ```copy()```.

## Criando uma lista

~~~python
my_list = []
my_list = [1, 2, 3, 4]
my_list = ["apple", "banana", "cherry"]
~~~

## Criando uma lista com o construtor list()

~~~python
my_list = list("my_string")
my_list = list(my_tuple)
my_list = list(my_set)
~~~

## Acessando um elemento de uma lista

~~~python
item = my_list[0]   # first
item = my_list[-1]  # last
item = my_list[-2]
~~~

## Acessando todos os elementos de uma lista

~~~python
my_list = ["apple", "banana", "cherry"]
for x in my_list:
    print(x) 
~~~

~~~python
my_list = ["apple", "banana", "cherry"]
for i in range(len(my_list)):
    print(my_list[i]) 
~~~

~~~python
my_list = ["apple", "banana", "cherry"]
i = 0
while i < len(my_list):
    print(my_list[i])
    i = i + 1
~~~

~~~python
my_list = ["apple", "banana", "cherry"]
[print(x) for x in my_list] 
~~~

## Obtendo fatias da lista

~~~python
my_list = my_list[2:5]  # 2 (included) and end at index 5 (not included)
my_list = my_list[:3]   # start at the first item, 3 (not included)
my_list = my_list[0:3]
my_list = my_list[2:]   # 2 (included) to the end 
my_list = my_list[-2:]
my_list = my_list[-4:-1]
~~~

## Verificando se um valor está contido na lista

~~~python
if "apple" in my_list:
    print("Sim")
~~~

## Modificando o valor de um item

~~~python
my_list[0] = "apple"
my_list[1:3] = ["apple", "cherry"] # mudando uma fatia da lista
~~~

## Inserindo itens em uma lista

~~~python
my_list.insert(1, "apple") # inserts an item at the specified index
my_list.append("apple") # add to the end
my_list.extend(my_list2) # add elementsof my_list2 to the end of my_list
my_list.extend(my_tuple) # add any iterable objects (tuple, set, dictionarie, etc)
~~~

## Removendo itens de uma lista

~~~python
my_list.remove("apple")
my_list.pop(1) # removes the specified index
my_list.pop(-1) # removes the last item
my_list.pop() # removes the last item
del my_list[0] # removes the specified index
del my_list # delete the list completely
my_list.clear()
~~~

## List Comprehension

útil para criar uma lista baseada em outra já existente.

~~~python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
my_list = [x for x in fruits] # copy the list fruits
my_list = [x for x in fruits if "a" in x] # fruits with the letter "a" in the name
my_list = [x for x in fruits if x[0] == "a"]
my_list = [x.upper() for x in fruits] 
my_list = [x * 2 for x in range(10)]
my_list = [x for x in range(10) if x % 2 == 0]
my_list = [x if x != "banana" else "orange" for x in fruits] # returns orange instead of banana
~~~

## Ordenando Listas

~~~python
my_list.sort() # all capital letters being sorted before lower case letters == case sensitive
my_list.sort(reverse = True)
my_list.reverse()
~~~

Ordena elementos baseado no quão próximos eles estão de 50:

~~~python
def myFunction(n):
    return abs(n - 50)
my_list = [100, 50, 65, 82, 23]
my_list.sort(key = myFunction)
~~~

Ordena usando case insensitive:

~~~python
my_list = ["banana", "Orange", "Kiwi", "cherry"]
my_list.sort(key = str.lower)
~~~

## Copiando uma lista

~~~python
my_list_cpy = my_list.copy()
~~~

~~~python
my_list_cpy = list(my_list)
~~~

## Juntando duas listas

~~~python
list3 = list1 + list2
~~~

~~~python
list1.extend(list2)
~~~

~~~python
for x in list2:
    list1.append(x)
~~~

## Eliminando itens duplicados

~~~python
my_list = [5, 1, 1, 2, 2, 3, 4, 4]
my_set = set(my_list)
my_list = list(my_set)
~~~

## Contando quantas vezes um elemento aparece na lista

~~~python
counter = my_list.count("apple")
~~~

## Obtendo o índice de um elemento da lista

~~~python
index = my_list.index("apple")
~~~

## Obtendo o tamanho da lista

~~~python
my_len = len(my_list)
~~~

## Obtendo a soma dos elementos da lista

~~~python
my_sum = sum(my_list)
~~~

## Obtendo o maior elemento da lista

~~~python
my_max = max(my_list)
~~~

## Obtendo o menor elemento da lista

~~~python
my_min = min(my_list)
~~~
