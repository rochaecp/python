# Conjuntos (sets)

- Um conjunto (set) é uma coleção não ordenada, **imutável**, não indexada e **não permite itens duplicados**.  
- Os itens de um conjunto podem ser de qualquer tipo.  

## Criar um conjunto

~~~python
meu_conjunto = {"morango", "banana", "uva"}
~~~

#### Com o construtor:

~~~python
meu_conjunto = set(("morango", "banana", "uva")) # note the double round-brackets
~~~

## Converter uma lista em um conjunto

~~~python
minha_lista = ["morango", "banana", "uva"]
meu_conjunto = set(minha_lista)
~~~

## Obter o tamanho de um conjunto

~~~python
tamanho = len(meu_conjunto)
~~~

## Acessar itens de um conjunto

Não é possível utilizar um index ou uma chave.  

#### Acessar todos elementos do conjunto:

~~~python
meu_conjunto = {"morango", "banana", "uva"}
for item in meu_conjunto:
    print(item) 
~~~

## Verificar se um elemento está em um conjunto

~~~python
my_bool = "banana" in meu_conjunto
~~~

## Modificar itens de um conjunto

> Não é possível fazer isso!

## Adicionar itens a um conjunto

Os itens repetidos são removidos.  

#### Adicionar um item:

~~~python
meu_conjunto.add("laranja")
~~~

#### Adicionar todos os itens de outro conjunto

~~~python
meu_conjunto.update(meu_conjunto_2)
~~~

#### Adicionar todos itens de uma lista: 

~~~python
meu_conjunto.update(minha_lista)
~~~

## Remover itens

Lança um erro se o elemento não existir:

~~~python
meu_conjunto.remove("banana") 
~~~

Não lança um erro se elemento não existir:

~~~python
meu_conjunto.discard("banana") 
~~~

Remove um elemento (lembrar: conjuntos não possuem ordem):

~~~python
last_item = meu_conjunto.pop()
~~~

Limpar o conjunto:

~~~python
meu_conjunto.clear()
~~~

Deletar totalmente o conjunto:

~~~python
del meu_conjunto # delete the set completely
~~~

## Remover itens duplicados de uma lista

~~~python
minha_lista = ["banana", "uva", "morango", "uva", "banana"]
meu_conjutno = set(minha_lista) # {'banana', 'morango', 'uva'}
~~~

## Operações entre Conjuntos

#### União

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"laranja", "goiaba", "manga"}
meu_conjunto_3 = meu_conjunto_1.union(meu_conjunto_2) # {'morango', 'goiaba', 'laranja', 'uva', 'banana', 'manga'}
~~~

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"laranja", "goiaba", "manga"}
meu_conjunto_1.update(meu_conjunto_2) # {'manga', 'uva', 'morango', 'banana', 'laranja', 'goiaba'}
~~~

#### Intersecção (mantém apenas os duplicados)

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"banana", "goiaba", "morango"}
meu_conjunto_3 = meu_conjunto_1.intersection(meu_conjunto_2) # {'morango', 'banana'}
~~~

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"banana", "goiaba", "morango"}
meu_conjunto_1.intersection_update(meu_conjunto_2) # {'banana', 'morango'}
~~~

#### Diferença simétrica (mantém todos menos os existentes em ambos)

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"banana", "goiaba", "morango"}
meu_conjunto_3 = meu_conjunto_1.symmetric_difference(meu_conjunto_2) # {'uva', 'goiaba'}
~~~

#### Diferença

~~~python
meu_conjunto_1 = {"morango", "banana", "uva"}
meu_conjunto_2 = {"banana", "goiaba", "morango"}
meu_conjunto_3 = meu_conjunto_1.difference(meu_conjunto_2) # {'uva'}
~~~

#### Subconjunto

Verifica se meu_conjunto_1 é subconjunto do meu_conjunto_2.  

~~~python
meu_conjunto_1 = {"morango", "banana"}
meu_conjunto_2 = {"morango", "banana", "goiaba", "morango"}
ehSubconjunto = meu_conjunto_1.issubset(meu_conjunto_2) # True
~~~

#### Superconjunto

Verifica se meu_conjunto_1 é superconjunto do meu_conjunto_2.  

~~~python
meu_conjunto_1 = {"manga", "banana", "goiaba", "uva"}
meu_conjunto_2 = {"manga", "banana"}
ehSuperconjunto = meu_conjunto_1.issuperset(meu_conjunto_2) # True
~~~
