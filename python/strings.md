# Python - Strings

Strings são Arrays de bytes que representam caracteres unicode.  
'hello' é o mesmoq que "hello"  
Python não possui um tipo caractere (usamos uma string com tamanho 1).  

## Criar strings

~~~python
minha_string_1 = "abcdefg"
minha_string_2 = 'abcdefg'
~~~

## Criar strings com múltiplas linhas

~~~python
a = """Mauricio
Rocha
"""
~~~

## Concatenar strings

~~~python
minha_string = "bom" + " dia" 
~~~

## Acessar caracteres de uma strings

~~~python
minha_string = "Mauricio"
primeiro_caractere = minha_string[0]
ultimo_caractere = minha_string[-1] 
~~~

~~~python
for x in minha_string:
  print(x)
~~~

## Obter fatias de uma string

~~~python
minha_string = "Mauricio"
minha_string_2 = minha_string_1[2:5] # posição 2 até a 5 (não incluída)
minha_string_2 = minha_string_1[:5]  # do início
minha_string_2 = minha_string_1[2:]  # até o fim
minha_string_2 = minha_string_1[-3:] # últimos 3
~~~

## Obter o tamanho de uma string

~~~python
tamanho = len(minha_string)
~~~

## Obter o unicode de uma string

~~~python
meu_unicode = ord("A") 
~~~

## Obter um caractere a partir de um unicode

~~~python
minha_string = chr(35)  # string - character whose Unicode code point is the integer
~~~

## Testar uma string

~~~python
minha_string = 'Mauricio'
meu_boolean = "a" in minha_string       # True
meu_boolean = "a" not in minha_string   # False
meu_boolean = "abacate" < "batata"      # True
meu_boolean = "abacate" == "batata"     # False
~~~

## Tornar uma string maiúscula

~~~python
minha_string = "maurício"
minha_string_maiusc = minha_string.upper()
~~~

## Tornar uma string minúscula

~~~python
minha_string = "maurício"
minha_string_minusc = minha_string.lower()
~~~

## Substituir caracteres de uma string

Substitui todas as ocorrências na string.  

~~~python
minha_string = "mauricio"
minha_string_modif = minha_string.replace('i', 'X')
~~~

## Modificar um caractere em um determinado índice de uma string

~~~python
minha_string = "Mauricio"
minha_lista = list(minha_string)
minha_lista[0] = "X"
minha_string = "".join(minha_lista) # Xauricio
~~~

~~~python
minha_string = "Mauricio"
minha_string = minha_string[:0] + 'X' + minha_string[1:] # Xauricio
~~~

## Transformar uma string em uma lista

~~~python
minha_string = "banana tomate maçã"
minha_lista = minha_string.split(' ') # ' ' é o separador: ['banana', 'tomate', 'maçã']
~~~

## Remover espaços iniciais e finais de uma string

~~~python
minha_string = " mauricio "
minha_string_sem_esp = minha_string.strip()
~~~

## Juntar os elementos de uma lista, tupla ou dicionário em uma string

~~~python
minha_lista = ["Mauricio", "Maria", "Jose"]
minha_string = " ".join(minha_lista)
~~~

~~~python
minha_tupla = ("Mauricio", "Maria", "Jose")
minha_string = " ".join(minha_tupla)
~~~

~~~python
meu_dicionario = {"name": "Mauricio", "country": "Brazil"}
my_join = ' '.join(meu_dicionario)
~~~