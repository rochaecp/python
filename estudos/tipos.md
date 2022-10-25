# Python - Tipos de Dados

- Numéricos
    - ```int```
    - ```float```
    - ```complex``` (ex.: 1j) 
- String
    - ```str```
- Booleano
  - ```bool```
- Binário
    - ```bytes```
    - ```bytearray```
    - ```memoryview```
- Sequências
    - ```list```
    - ```tuple```
    - ```range```
- Dicionários 	
    - ```dict```
- Conjuntos
    - ```set```
    - ```frozenset```

## Obtendo o tipo de uma variavel

~~~python
myType = type(minhaVariavel)
~~~

## Tipos numéricos

~~~python
x = 1    # int
y = 2.8  # float
z = 1j   # complex
~~~

## Tipo Booleano

- Representam os valores: ```True``` ou ```False```.
- Qualquer string é True, exceto uma string vazia.
- Qualquer número é True, exceto o 0.
- Qualquer list, tuple, set e dict é true, exceto se estiver vazio.
- Valores falsos: ```()```, ```[]```, ```{}```, ```""```, ```0```, ```None```, ```False```.

~~~python
# True
myBool = bool(True)
myBool = True
myBool = bool("Hello")
myBool = bool(15)

# False
myBool = bool(False) 
myBool = False
myBool = bool(None)
myBool = bool(0)
myBool = bool("")
myBool = bool(())
myBool = bool([])
myBool = bool({}) 
~~~
