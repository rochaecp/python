# Python - Conjuntos (sets)

Um conjunto (set) é uma coleção não ordenada, **imutável**, não indexada e **não permite itens duplicados**.  
Os itens de um conjunto podem ser de qualquer tipo.  

## Criar um conjunto

~~~python
my_set = {"morango", "banana", "uva"}
~~~

#### Com o construtor:

~~~python
my_set = set(("morango", "banana", "uva")) # note the double round-brackets
~~~

## Converter uma lista em um conjunto

~~~python
my_set = set(my_list)
~~~

## Obter o tamanho de um conjunto

~~~python
my_len = len(my_set)
~~~

## Acessar itens de um conjunto

Não é possível utilizar um index ou uma chave.  

#### Acessar todos elementos do conjunto:

~~~python
for x in my_set:
    print(x) 
~~~

## Verificar se um elemento está em um conjunto

~~~python
my_bool = "banana" in my_set
~~~

## Modificar itens de um conjunto

> Não é possível fazer isso!

## Adicionar itens a um conjunto

Os itens repetidos são removidos.  

#### Adicionar um item:

~~~python
my_set.add("laranja")
~~~

#### Adicionar todos os itens de outro conjunto

~~~python
my_set.update(my_set2)
~~~

#### Adicionar todos itens de uma lista: 

~~~python
my_set.update(my_list)
~~~

## Remover itens

Lança um erro se o elemento não existir:

~~~python
my_set.remove("banana") 
~~~

Não lança um erro se elemento não existir:

~~~python
my_set.discard("banana") 
~~~

Remove um elemento (lembrar: conjuntos não possuem ordem):

~~~python
last_item = my_set.pop()
~~~

Limpar o conjunto:

~~~python
my_set.clear()
~~~

Deletar totalmente o conjunto:

~~~python
del my_set # delete the set completely
~~~

## Remover itens duplicados de uma lista

~~~python
minha_lista = ["banana", "uva", "morango", "uva", "banana"]
meu_conjutno = set(minha_lista) # {'banana', 'morango', 'uva'}
~~~

## Operações entre Conjuntos

#### União

~~~python
my_set3 = my_set1.union(my_set2)
~~~

#### Intersecção (mantém apenas os duplicados)

~~~python
my_set3 = my_set1.intersection(my_set2)
~~~

#### Diferença simétrica (mantém todos menos os existentes em ambos)

~~~python
my_set3 = my_set1.symmetric_difference(my_set2) 
~~~

#### Diferença

~~~python
my_set = my_set.difference(my_set2)
~~~

#### Subconjunto

~~~python
answ = my_set.issubset(my_set2)
~~~

#### Superconjunto

~~~python
answ = my_set.issuperset(my_set2)
~~~
