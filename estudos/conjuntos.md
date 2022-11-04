# Python - Conjuntos (sets)

- Um conjunto (set) é uma coleção não ordenada, **imutável**, não indexada e **não permite itens duplicados**.
- Os itens de um conjunto podem ser de qualquer tipo.

## Criando um conjunto

~~~python
my_set = {"apple", "banana", "cherry"}
~~~

Com o construtor:

~~~python
my_set = set(("apple", "banana", "cherry")) # note the double round-brackets
~~~

Convertendo lista em conjunto com o construtor:

~~~python
my_set = set(my_list)
~~~

## Obtendo o tamanho de um conjunto

~~~python
my_len = len(my_set)
~~~

## Acessando itens de um conjunto

- Não é possível utilizar um index ou uma chave.

Acessando todos elementos do conjunto:

~~~python
for x in my_set:
    print(x) 
~~~

## Checando se um elemento está no conjunto

~~~python
my_bool = "banana" in my_set
~~~

## Modificando itens de um conjunto

> Não é possível fazer isso!

## Adicionando itens a um conjunto

- Os itens repetidos são removidos.

Adicionando um item:

~~~python
my_set.add("laranja")
~~~

Adicionando todos os itens de outro conjunto:

~~~python
my_set.update(my_set2)
~~~

Adicionando todos itens de uma lista: 

~~~python
my_set.update(my_list)
~~~

## Removendo itens

Lança um erro se o elemento não existir:

~~~python
my_set.remove("banana") 
~~~

Não lança um erro se elemento não existir:

~~~python
my_set.discard("banana") 
~~~

Remove um elemento (lembrando: conjuntos não possuem ordem):

~~~python
last_item = my_set.pop()
~~~

Limpando o conjunto:

~~~python
my_set.clear()
~~~

Deletando totalmente o conjunto:

~~~python
del my_set # delete the set completely
~~~

## Operações entre Conjuntos

União:

~~~python
my_set3 = my_set1.union(my_set2)
~~~

Intersecção (mantém apenas os duplicados):

~~~python
my_set3 = my_set1.intersection(my_set2)
~~~

Diferença simétrica (mantém todos menos os existentes em ambos):

~~~python
my_set3 = my_set1.symmetric_difference(my_set2) 
~~~

Diferença:

~~~python
my_set = my_set.difference(my_set2)
~~~

Subconjunto: 

~~~python
answ = my_set.issubset(my_set2)
~~~

Superconjunto:

~~~python
answ = my_set.issuperset(my_set2)
~~~
