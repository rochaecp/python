# Tipos de dados

| Categoria | Tipo              | Tamanho   | Exemplo |
| ---       | ---               | ---       | ---     |
| Numérico  | ```int```         |           | x = 1   |
| Numérico  | ```float```       |           | y = 2.8 |
| Numérico  | ```complex```     |           | z = 1j  |
| String    | ```str```         |           | x = "Olá mundo" |
| Booleano  | ```bool```        |           | x = True |
| Binário   | ```bytes```       |           |         |
| Binário   | ```bytearray```   |           |         |
| Binário   | ```memoryview```  |           |         |
| Sequência | ```list```        |           | x = [1, 2] |
| Sequência | ```tuple```       |           | x = (1, 2) |
| Sequência | ```range```       |           |         |
| Dicionário| ```dict```        |           |         |
| Conjunto  | ```set```         |           |         |
| Conjunto  | ```frozenset```   |           |         |


## Obtendo o tipo de uma variavel

~~~python
myType = type(minhaVariavel)
~~~

## Tipo Booleano

Representam os valores: ```True``` ou ```False```.   
Qualquer string é True, exceto uma string vazia.   
Qualquer número é True, exceto o 0.   
Qualquer list, tuple, set e dict é true, exceto se estiver vazio.   
Valores falsos: ```()```, ```[]```, ```{}```, ```""```, ```0```, ```None```, ```False```.   

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