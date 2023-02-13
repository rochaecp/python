# Python - Strings

Strings são Arrays de bytes que representam caracteres unicode.  
'hello' é o mesmoq que "hello"  
Python não possui um tipo caractere (usamos uma string com tamanho 1).  

## Criando uma String

~~~python
minha_string_1 = "abcdefg"
minha_string_2 = 'abcdefg'
~~~

## Concatenação

~~~python
minha_string = "bom" + " dia" 
~~~

## Acessando caracteres da String

~~~python
minha_string = "Mauricio"
primeiro_caractere = minha_string[0]
ultimo_caractere = minha_string[-1] 
~~~

## Acessando cada caractere da String

~~~python
for x in minha_string:
  print(x)
~~~

## Obtendo fatias da String

~~~python
minha_string = "Mauricio"
minha_string_2 = minha_string_1[2:5] # posição 2 até a 5 (não incluída)
minha_string_2 = minha_string_1[:5]  # do início
minha_string_2 = minha_string_1[2:]  # até o fim
minha_string_2 = minha_string_1[-3:] # últimos 3
~~~

## Tamanho da String

~~~python
tamanho = len(minha_string)
~~~

## Obtendo o Unicode de uma String

~~~python
meu_unicode = ord("A") 
~~~

## Obtendo um caractere a partir de um Unicode

~~~python
minha_string = chr(35)  # string - character whose Unicode code point is the integer
~~~

## Testando a string

~~~python
minha_string = 'Mauricio'
meu_boolean = "a" in minha_string       # True
meu_boolean = "a" not in minha_string   # False
meu_boolean = "abacate" < "batata"      # True
meu_boolean = "abacate" == "batata"     # False
~~~

## Strings com múltiplas linhas

~~~python
a = """Mauricio
Rocha
"""
~~~

## Algumas funções

~~~python
minha_string_2 = minha_string_1.upper()
minha_string_2 = minha_string_1.lower()
minha_string_2 = minha_string_1.replace("a", "x")
minha_string_2 = minha_string_1.split(" ")
minha_string_2 = minha_string_1.strip() # remove espaços em branco do início e fim
~~~
