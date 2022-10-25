# Python - Strings

- Strings são Arrays de bytes que representam caracteres unicode.
- 'hello' é o mesmoq que "hello"
- Python não possui um tipo caractere (usamos uma string com tamanho 1)

## Criando uma String

~~~python
minhaString = "abcdefg"
minhaString = 'abcdefg'
~~~

## Concatenação

~~~python
minhaString = "bom" + " dia" 
~~~

## Acessando caracteres da String

~~~python
primeiroCaractere = minhaString[0]
~~~

## Acessando cada caractere da String

~~~python
for x in myString:
  print(x)
~~~

## Obtendo fatias da String

~~~python
minhaString2 = minhaString[-1]  # último
minhaString2 = minhaString[2:5] # posição 2 até a 5 (não incluída)
minhaString2 = minhaString[:5]  # do início
minhaString2 = minhaString[2:]  # até o fim
minhaString2 = minhaString[-3:] # últimos 3
~~~

## Tamanho da String

~~~python
tamanho = len(string)
~~~

## Obtendo o Unicode da String

~~~python
meuUnicode = ord("A") 
~~~

## Obtendo um caractere a partir do Unicode

~~~python
minhaString = chr(35)  # string - character whose Unicode code point is the integer
~~~

## Testando a string

~~~python
meuBool = "a" in minhaString 
meuBool = "a" not in minhaString
meuBool = "aaa" < "bbb"  
meuBool = "aaa" == "bbb" 
~~~

## Strings com múltiplas linhas

~~~python
a = """Mauricio
Rocha
"""
~~~

## Algumas funções

~~~python
minhaString2 = minhaString.upper()
minhaString2 = minhaString.lower()
minhaString2 = minhaString.replace("a", "x")
minhaLista = minhaString.split(" ")
minhaString2 = minhaString.strip() # remove espaços em branco do início e fim
~~~
