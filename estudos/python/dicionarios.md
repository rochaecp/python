# Python - Dicionários

- Um dicionário é uma coleção ordenada (a partir do Python 3.7), modificável e não permite itens duplicados.
- São utilizados para gravar dados como pares chave (key) e valor (value).
- Não é possível copiar um dicionário fazendo ```dict2 = dict1```. Isso faria dict2 guardar uma referência para dict1.

## Criando um dicionário

~~~python
my_dict = {
    "model": "Mustang",
    "electric": False,
    "year": 1964,
    "colors": ["red", "white", "blue"]
}
~~~

## Obtendo o tamanho do dicionário

~~~python
my_len = len(my_dict)
~~~

## Acessando os valores do dicionário

Acessando um valor:

~~~python
my_item = my_dic["model"]
my_item = my_dic.get("model")
~~~

~~~python
my_item = my_dic["model"]
my_item = my_dic.get("model")
~~~

Acessando todos os valores:

~~~python
values_list = my_dict.values() 
~~~

~~~python
for x in my_dict:
    print(my_dict[x]) 
~~~

~~~python
for x in my_dict.values():
    print(x)
~~~

## Acessando as chaves do dicionário

~~~python
keys_list = my_dict.keys() 
~~~

~~~python
for x in my_dict:
    print(x) # keys
~~~

~~~python
for x in my_dict.keys():
    print(x) 
~~~

## Acessando os itens do dicionário

~~~python
items_list_of_tuples = my_dict.items()
~~~

~~~python
for x, y in my_dict.items():
    print(x, y) # keys, values
~~~

## Verificando se um item existe

~~~python
if "model" in my_dict:
    print("Yes") 
~~~

## Modificando um item do dicionário

~~~python
my_dict['age'] = 30
~~~

~~~python
my_dict.update({"age": 31}) 
~~~

## Adicionando um item ao dicionário

~~~python
car["brand"] = "Ford"
~~~

~~~python
my_dict.update({"brand": "Ford"})
~~~

## Removendo um item do dicionário

~~~python
my_dict.pop("age")

~~~

~~~python
my_dict..popitem() # 3.7 - random item
~~~

~~~python
del my_dict['age']
~~~

~~~python
del my_dict
~~~

~~~python
my_dict.clear()
~~~

## Copiando um dicionário

~~~python
my_dict_cpy = my_dict.copy()
~~~

~~~python
my_dict_cpy = dict(my_dict)
~~~

## Dicionários aninhados

~~~python
myfamily = {
    "child1" : {
        "name" : "Emil",
        "year" : 2004
    },
    "child2" : {
        "name" : "Tobias",
        "year" : 2007
    },
    "child3" : {
        "name" : "Linus",
        "year" : 2011
    }
}

print(myfamily["child1"]) # {'name': 'Emil', 'year': 2004}
print(myfamily["child1"]["name"]) # Emil
~~~

~~~python
child1 = {
    "name" : "Emil",
    "year" : 2004
}
child2 = {
    "name" : "Tobias",
    "year" : 2007
}
child3 = {
    "name" : "Linus",
    "year" : 2011
}

myfamily = {
    "child1" : child1,
    "child2" : child2,
    "child3" : child3
}
~~~
