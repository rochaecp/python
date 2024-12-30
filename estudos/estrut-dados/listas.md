# Listas

- Listas são usadas para gravar múltiplos itens em uma mesma variável.  
- Permitem: gravar itens de maneira ordenada, Alterar os itens, itens duplicados.  
- No Python, são objetos do tipo list.  
- Não se pode copiar uma lista fazendo apenas ``` list2 = list1 ```. É necessário usar o método ```copy()```.  
- List Comprehension
    - Útil para criar uma lista baseada em outra já existente
- Em Python é possível adicionar variáveis de mais de um tipo em uma mesma lista

## Criar uma lista

~~~python
minha_lista = []
minha_lista = [1, 2, 3, 4]
minha_lista = ["apple", "banana", "cherry"]
~~~

~~~python
minha_lista = list("my_string") # construtor list()
minha_lista = list(minha_tupla)
minha_lista = list(meu_conjunto)
~~~

## Obter o tamanho de uma lista

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

## Acessar uma fatia de uma lista

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

## Alterar um item de uma lista

~~~python
minha_lista = ["Maçã", "Banana", "Tomate"]
minha_lista[0] = "Pera" # ['Pera', 'Banana', 'Tomate']
~~~

## Alterar uma fatia de uma lista

~~~python
minha_lista = ["Maçã", "Banana", "Tomate", "Pera"]
minha_lista[1:3] = ["Mamão", "Abacate"] # ['Maçã', 'Mamão', 'Abacate', 'Pera']
~~~

## Inserir um item em uma lista

~~~python
minha_lista = ['Mauricio']
minha_lista.append('Tesla') # ['Mauricio', 'Tesla']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_lista.insert(0, 'Turing')     # ['Turing', 'Mauricio', 'Tesla']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_lista.insert(1, 'Turing')     # ['Mauricio', 'Turing', 'Tesla']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_lista2 = ['Turing']
minha_lista.extend(minha_lista2) # ['Mauricio', 'Tesla', 'Turing']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_tupla = ('Turing', 'Newton')
minha_lista.extend(minha_tupla) # ['Mauricio', 'Tesla', 'Turing', 'Newton']
~~~

## Remover um item de uma lista

remove(): não retorna nenhum valor.  
pop(): retorna o item removido.  

~~~python
minha_lista = ['Mauricio', 'Tesla', 'Newton', 'Turing']
minha_lista.remove('Mauricio') # ['Tesla', 'Newton', 'Turing']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla', 'Newton', 'Turing']
item_removido = minha_lista.pop(0) # 'Mauricio'
item_removido = minha_lista.pop(-1) # 'Turing'
~~~

## Limpar uma lista

~~~python
minha_lista = ['Mauricio', 'Tesla', 'Newton', 'Turing']
minha_lista.clear() # []
~~~

## Ordenar uma lista de strings de modo crescente (case sensitive)

O método sort() é case sensitive.  

~~~python
minha_lista = ['Newton', 'Mauricio', 'mauricio', 'Tesla']
minha_lista.sort() # ['Mauricio', 'Newton', 'Tesla', 'mauricio']
~~~

## Ordenar uma lista de strings de modo crescente (case insensitive)

~~~python
minha_lista = ['Newton', 'Mauricio', 'mauricio', 'Tesla']
minha_lista.sort(key = str.lower) # ['Mauricio', 'mauricio', 'Newton', 'Tesla']
~~~

## Ordenar uma lista de inteiros de modo decrescente

~~~python
minha_lista = [0, 3, 1, 2]
minha_lista.sort(reverse = True) # [3, 2, 1, 0]
~~~

## Ordenar os elementos de uma lista baseado no quão próximos eles estão de 50

~~~python
def myFunction(n):
    return abs(n - 50)
minha_lista = [100, 50, 65, 82, 23]
minha_lista.sort(key = myFunction)
~~~

## Inverter a ordem dos elementos de uma lista

~~~python
minha_lista = [0, 3, 1, 2]
minha_lista.reverse() # [2, 1, 3, 0]
~~~

## Copiar uma lista

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_lista_copy = minha_lista.copy() # ['Mauricio', 'Tesla']
~~~

~~~python
minha_lista = ['Mauricio', 'Tesla']
minha_lista_copy = list(minha_lista) # ['Mauricio', 'Tesla']
~~~

## Juntar duas listas

~~~python
minha_lista_1 = ['Mauricio', 'Tesla']
minha_lista_2 = ['Newton', 'Turing']
minha_lista_3 = minha_lista_1 + minha_lista_2     # ['Mauricio', 'Tesla', 'Newton', 'Turing']
~~~

~~~python
minha_lista_1 = ['Mauricio', 'Tesla']
minha_lista_2 = ['Newton', 'Turing']
minha_lista_1.extend(minha_lista_2)     # ['Mauricio', 'Tesla', 'Newton', 'Turing']
~~~

~~~python
minha_lista_1 = ['Mauricio', 'Tesla']
minha_lista_2 = ['Newton', 'Turing']
for item in minha_lista_2:
    minha_lista_1.append(item) # ['Mauricio', 'Tesla', 'Newton', 'Turing']
~~~

## Eliminar itens duplicados

~~~python
minha_lista = [5, 1, 1, 2, 2, 3, 4, 4]
meu_conjunto = set(minha_lista)
minha_lista = list(meu_conjunto)
~~~

## Contar quantas vezes um elemento aparece na lista

O método count() é case sensitive.  

~~~python
minha_lista = ['Newton', 'Mauricio', 'Mauricio', 'Tesla']
nro_repetidos = minha_lista.count("Mauricio") # 2
~~~

## Obter o índice de um elemento da lista

O método index() retorna a posição da primeira correspondência.  

~~~python
minha_lista = ['Newton', 'Mauricio', 'Mauricio', 'Tesla']
indice = minha_lista.index('Mauricio') # 1
~~~

## Obter a soma dos elementos da lista

~~~python
minha_lista = [1, 3, 6, 5]
soma = sum(minha_lista) # 15
~~~

## Obter o maior elemento da lista

~~~python
minha_lista = [1, 3, 6, 5]
maior = max(minha_lista) # 6
~~~

## Obter o menor elemento da lista

~~~python
minha_lista = [1, 3, 6, 5]
menor = min(minha_lista) # 1
~~~

## Juntar os elementos de uma lista em uma string

~~~python
lista_str = ["5", "4", "3", "2", "1"]
str_num = ''.join(lista_str) # 54321
str_num_com_sep = ' '.join(lista_str) # 5 4 3 2 1
~~~

## List Comprehension: copiar uma lista

~~~python
minha_lista = ["banana", "morango", "laranja"]
minha_lista_2 = [x for x in minha_lista] # ['banana', 'morango', 'laranja']
~~~

## List Comprehension: tornar cada elemento da lista maiúsculo

~~~python
minha_lista = ["banana", "morango", "laranja"]
minha_lista_2 = [x.upper() for x in minha_lista] # ['BANANA', 'MORANGO', 'LARANJA']
~~~

## List Comprehension: criar uma nova lista a partir de um range

~~~python
minha_lista = [x for x in range(1, 6)] # [1, 2, 3, 4, 5]
~~~

## List Comprehension: criar uma nova lista a partir de uma antiga eliminando algum item

~~~python
minha_lista = ["banana", "uva", "laranja", "pera", "uva"]
minha_lista_2 = [x for x in minha_lista if x != "uva"] # ['banana', 'laranja', 'pera']
~~~

## List Comprehension: criar uma nova lista a partir de uma antiga eliminando itens que contenham a letra 'n'

~~~python
minha_lista = ["banana", "uva", "laranja", "pera", "uva"]
minha_lista_2 = [x for x in minha_lista if "n" not in x] # ['uva', 'pera', 'uva']
~~~

## List Comprehension: criar uma nova lista a partir de uma antiga modificando algum item

~~~python
minha_lista = ["banana", "uva", "laranja", "pera"]
minha_lista_2 = [x if x != "banana" else "Banana" for x in minha_lista ] # ['Banana', 'uva', 'laranja', 'pera']
~~~

## Unpack de uma lista

~~~python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
~~~