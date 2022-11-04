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

## Obtendo o tamanho de um conjunto

~~~python
my_len = len(my_set)
~~~

## Acessando itens de um conjunto

- Não é possível utilizar um index ou uma chave.

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

~~~python
my_set.add("laranja")
~~~

## 

~~~python

~~~



~~~python
# Add Sets or any iterable object (tuples, lists, dictionaries etc.)
my_set.update(my_set2) # add items from my_set2 set into my_set
my_set.update(my_list) # add items from the list into my_set

# Remove Item
my_set.remove("banana") # raise an error if dont exist
my_set.discard("banana") # dont raise an error if dont exist
last_item = my_set.pop() # remember: the sets are unordered
my_set.clear() # empties the set
del my_set # delete the set completely

# Loop Items
for item in my_set:
  print(item) 

# Join Two Sets - elimine duplicates
my_set3 = my_set1.union(my_set2)
my_set1.update(my_set2) # insert the items in my_set2 into my_set1

# Join Two Sets - Keep ONLY the Duplicates
my_set1.intersection_update(my_set2)
my_set3 = my_set1.intersection(my_set2) # Return a set that contains the items that exist in both set

# Join Two Sets - Keep All, But NOT the Duplicates
my_set3 = my_set1.symmetric_difference(my_set2) # return a new set, that contains only the elements that are NOT present in both sets.

# Other methods
my_set = my_set.difference(my_set2)
answ = my_set.issubset(my_set2)
answ = my_set.issuperset(my_set2)
my_set = set(my_list)
~~~
