# Python - Listas

- Listas são usadas para gravar múltiplos itens em uma mesma variável.
- Permitem: gravar itens de maneira ordenada, modificar os itens, itens duplicados.
- No Python, são objetos do tipo list.
- Não se pode copiar uma lista fazendo apenas ``` list2 = list1 ```. É necessário usar o método ```copy()```.

## Criar uma lista

~~~python
minha_lista = []
minha_lista = [1, 2, 3, 4]
minha_lista = ["apple", "banana", "cherry"]
~~~

## Criar uma lista com o construtor list()

~~~python
minha_lista = list("my_string")
minha_lista = list(minha_tupla)
minha_lista = list(meu_conjunto)
~~~

## Obter o tamanho da lista

~~~python
minha_lista = [1, 2, 3, 4]
my_len = len(minha_lista)   # 4
~~~

## Acessar um elemento de uma lista

~~~python
minha_lista = [1, 2, 3, 4]
item = minha_lista[0]   # 1
item = minha_lista[-1]  # 4
item = minha_lista[-2]  # 3
~~~

## Acessar fatias de uma lista

~~~python
minha_lista = [1, 2, 3, 4, 5, 6, 7, 8]
minha_lista = minha_lista[2:5]      # [3, 4, 5]
minha_lista = minha_lista[:3]       # [1, 2, 3]
minha_lista = minha_lista[0:3]      # [1, 2, 3]
minha_lista = minha_lista[2:]       # [3, 4, 5, 6, 7, 8]
minha_lista = minha_lista[-2:]      # [7, 8]
minha_lista = minha_lista[-4:-1]    # [5, 6, 7]
~~~

## Acessar todos os elementos de uma lista

~~~python
minha_lista = ["apple", "banana", "cherry"]
for x in minha_lista:
    print(x) 
~~~

~~~python
minha_lista = ["apple", "banana", "cherry"]
for i in range(len(minha_lista)):
    print(minha_lista[i]) 
~~~

~~~python
minha_lista = ["apple", "banana", "cherry"]
i = 0
while i < len(minha_lista):
    print(minha_lista[i])
    i = i + 1
~~~

~~~python
minha_lista = ["apple", "banana", "cherry"]
[print(x) for x in minha_lista] 
~~~

## Verificar se um valor está contido na lista

~~~python
if "apple" in minha_lista:
    print("Sim")
~~~

## Modificar o valor de um item

~~~python
minha_lista[0] = "apple"
minha_lista[1:3] = ["apple", "cherry"] # mudar uma fatia da lista
~~~

## Inserindo itens em uma lista

~~~python
minha_lista.insert(1, "apple") # inserts an item at the specified index
minha_lista.append("apple") # add to the end
minha_lista.extend(minha_lista2) # add elementsof minha_lista2 to the end of minha_lista
minha_lista.extend(minha_tupla) # add any iterable objects (tuple, set, dictionarie, etc)
~~~

## Remover itens de uma lista

~~~python
minha_lista.remove("apple")
minha_lista.pop(1) # removes the specified index
minha_lista.pop(-1) # removes the ultimo item
minha_lista.pop() # removes the ultimo item
del minha_lista[0] # removes the specified index
del minha_lista # delete the list completely
minha_lista.clear()
~~~

## List Comprehension

útil para criar uma lista baseada em outra já existente.

~~~python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
minha_lista = [x for x in fruits] # copy the list fruits
minha_lista = [x for x in fruits if "a" in x] # fruits with the letter "a" in the name
minha_lista = [x for x in fruits if x[0] == "a"]
minha_lista = [x.upper() for x in fruits] 
minha_lista = [x * 2 for x in range(10)]
minha_lista = [x for x in range(10) if x % 2 == 0]
minha_lista = [x if x != "banana" else "orange" for x in fruits] # returns orange instead of banana
~~~

## Ordenar Listas

~~~python
minha_lista.sort() # all capital letters being sorted before lower case letters == case sensitive
minha_lista.sort(reverse = True)
minha_lista.reverse()
~~~

Ordena elementos baseado no quão próximos eles estão de 50:

~~~python
def myFunction(n):
    return abs(n - 50)
minha_lista = [100, 50, 65, 82, 23]
minha_lista.sort(key = myFunction)
~~~

Ordena usar case insensitive:

~~~python
minha_lista = ["banana", "Orange", "Kiwi", "cherry"]
minha_lista.sort(key = str.lower)
~~~

## Copiar uma lista

~~~python
minha_lista_cpy = minha_lista.copy()
~~~

~~~python
minha_lista_cpy = list(minha_lista)
~~~

## Juntar duas listas

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

## Eliminar itens duplicados

~~~python
minha_lista = [5, 1, 1, 2, 2, 3, 4, 4]
meu_conjunto = set(minha_lista)
minha_lista = list(meu_conjunto)
~~~

## Contar quantas vezes um elemento aparece na lista

~~~python
counter = minha_lista.count("apple")
~~~

## Obter o índice de um elemento da lista

~~~python
index = minha_lista.index("apple")
~~~

## Obter a soma dos elementos da lista

~~~python
my_sum = sum(minha_lista)
~~~

## Obter o maior elemento da lista

~~~python
my_max = max(minha_lista)
~~~

## Obter o menor elemento da lista

~~~python
my_min = min(minha_lista)
~~~
