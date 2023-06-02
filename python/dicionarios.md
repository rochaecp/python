# Python - Dicionários

Um dicionário é uma coleção ordenada (a partir do Python 3.7), modificável e não permite itens duplicados.  
São utilizados para gravar dados como pares chave (key) e valor (value).  
Não é possível copiar um dicionário fazendo ```dict2 = dict1```. Isso faria dict2 guardar uma referência para dict-  

## Criar um dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}
~~~

## Obter o tamanho do dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

s = tamanho = len(meu_dicionario) # 3
~~~

## Acessar os valores do dicionário

#### Um valor

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_item = meu_dicionario["nome"]
meu_item = meu_dicionario.get("nome") 
~~~

#### Todos os valores

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

for x in meu_dicionario:
    print(meu_dicionario[x]) 
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

for x in meu_dicionario.values():
    print(x)
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

lista_valores = meu_dicionario.values() 
~~~

## Acessar as chaves do dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

for x in meu_dicionario:
    print(x)
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

for x in meu_dicionario.keys():
    print(x) 
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

lista_chaves = meu_dicionario.keys() 
~~~

## Acessar os itens do dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

lista_de_tuplas_itens = meu_dicionario.items()
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

for x, y in meu_dicionario.items():
    print(x, y) # keys, values
~~~

## Verificar se um item existe

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

if "nome" in meu_dicionario:
    print("Yes") 
~~~

## Modificar um item do dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario['idade'] = 32
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario.update({"idade": 32}) 
~~~

## Adicionar um item ao dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario["signo"] = "Capricórnio"
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario.update({"signo": "Capricórnio"})
~~~

## Remover um item do dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario.pop("linguagens")
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario..popitem() # 3.7
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

del meu_dicionario['idade']
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

del meu_dicionario
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario.clear()
~~~

## Copiar um dicionário

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario_cpy = meu_dicionario.copy()
~~~

~~~python
meu_dicionario = {
    "nome": "Mauricio",
    "idade": 31,
    "linguagens": ["JS", "C#", "Python"]
}

meu_dicionario_cpy = dict(meu_dicionario)
~~~

## Dicionários aninhados

~~~python
meu_dicionario = {
    "filho1" : {
        "nome" : "Filhoquinho",
        "ano" : 2020
    },
    "filho2" : {
        "nome" : "Bill Gates",
        "ano" : 2007
    },
    "filho3" : {
        "nome" : "Linus",
        "ano" : 2011
    }
}

print(meu_dicionario["filho1"]) 
print(meu_dicionario["filho1"]["nome"]) 
~~~

~~~python
filho1 = {
    "nome" : "Filhoquinho",
    "ano" : 2020
}
filho2 = {
    "nome" : "Bill Gates",
    "ano" : 2007
}
filho3 = {
    "nome" : "Linus",
    "ano" : 2011
}

meu_dicionario = {
    "filho1" : filho1,
    "filho2" : filho2,
    "filho3" : filho3
}
~~~
