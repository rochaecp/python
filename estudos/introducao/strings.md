# Strings

- Strings são Arrays de bytes que representam caracteres unicode
- 'hello' é o mesmo que "hello"
- Python não possui um tipo caractere (usamos uma string com tamanho 1)

## Criar uma string

~~~python
minha_string_1 = "abcdefg"
minha_string_2 = 'abcdefg'
~~~

## Criar uma string com múltiplas linhas

~~~python
a = """Mauricio
Rocha
"""
~~~

## Concatenar uma string

- Só é possível concatenar uma string com outra string

~~~python
minha_string = "bom" + " dia" 
~~~

## Acessar caracteres de uma uma string

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

## Preencher com zeros o início de uma string

~~~python
meu_valor = 5
meu_valor_modif = str(meu_valor).zfill(3) # 005
~~~

## Remover espaços iniciais e finais de uma string

~~~python
minha_string = " mauricio "
minha_string_sem_esp = minha_string.strip()
~~~

## Transformar uma string em uma lista

~~~python
minha_string = "banana tomate maçã"
minha_lista = minha_string.split(' ') # ' ' é o separador: ['banana', 'tomate', 'maçã']
~~~

## Juntar os elementos de uma lista, tupla ou dicionário em uma string

~~~python
lista_str = ["5", "4", "3", "2", "1"]
str_num = ''.join(lista_str) # 54321
str_num_com_sep = ' '.join(lista_str) # 5 4 3 2 1
~~~

~~~python
minha_lista = ["Mauricio", "Maria", "Jose"]
minha_string = " ".join(minha_lista) # Mauricio Maria Jose
~~~

~~~python
minha_tupla = ("Mauricio", "Maria", "Jose")
minha_string = " ".join(minha_tupla) # Mauricio Maria Jose
~~~

~~~python
meu_dicionario = {"name": "Mauricio", "country": "Brazil"}
my_join = ' '.join(meu_dicionario) # name country
~~~

## Slice

- `sequencia[início:fim:passo]`
    - início: Índice inicial (inclusivo). Define onde o slicing começa.
        - se não for especificado, o Python assume o valor padrão None, ou seja, o início da string
    - fim: Índice final (exclusivo). Define onde o slicing termina.
        - se não for especificado, o Python assume o valor padrão None, ou seja, até o final da string.
    - passo: Define o intervalo entre os elementos selecionados (pode ser negativo).
        - O valor -1 significa que a sequência será percorrida de trás para frente, invertendo a ordem dos caracteres.

~~~python
nome = "Mauricio"
print(nome[2:5]) # pos 2 incluso, pos 5 nao incluso
print(nome[:5])
print(nome[2:])
print(nome[-3:]) # ultimos 3
nome_invert = texto[::-1]     # slice: inverter string

nome = "Mauricio"

# Slicing detalhado
print(nome[::1])   # "Mauricio" - Percorre na ordem normal
print(nome[::2])   # "Muiri"   - Pega um caractere a cada dois
print(nome[::-1])  # "oiciruaM" - Inverte a string
~~~

## Alterar

~~~python
# jeito 1
nome = "Mauricio"
lista = list(nome)
lista[0] = "X"
nome = "".join(lista)
print(nome)

# jeito 2
nome = "Mauricio"
nome = nome[:0] + 'X' + nome[1:]
print(nome)
~~~

## Métodos para strings

- capitalize() - Converte o primeiro caractere em maiúsculas
- casefold() -  Converte string em minúsculas 
- center() - Retorna uma string centralizada 
- count() -  Retorna o número de vezes que um valor especificado ocorre em uma string 
- encode() -  Retorna uma versão codificada da string 
- endswith() -  Retorna true se a string terminar com o valor especificado 
- expandtabs() -  Define o tamanho da tabulação da string 
- find() -  Procura na string um valor especificado e retorna a posição de onde foi encontrado 
- format() - Formata os valores especificados em uma string 
- format_map() - Formata valores especificados em uma string 
- index() - Procura na string um valor especificado e retorna a posição de onde foi encontrado 
- isalnum() - Retorna True se todos os caracteres na string forem alfanuméricos 
- isalpha() - Retorna True se todos os caracteres na string estão no alfabeto 
- isdecimal() - Retorna True se todos os caracteres na string forem decimais 
- isdigit() -  Retorna True se todos os caracteres na string forem dígitos 
- isidentifier() - Retorna True se a string for um identificador 
- islower() - Retorna True se todos os caracteres em a string está em letras minúsculas 
- isnumeric() - Retorna True se todos os caracteres na string são numéricos 
- isprintable() - Retorna True se todos os caracteres na string são imprimíveis 
- isspace() - Retorna True se todos os caracteres na string são espaços em branco 
- istitle() - Retorna True se a string segue as regras de um título 
- isupper() -  Retorna True se todos os caracteres na string forem maiúsculos 
- join() - Une os elementos de um iterável ao final da string 
- ljust() -  Retorna uma versão justificada à esquerda da string lower( ) Converte uma string em letras minúsculas 
- lstrip() - Retorna uma versão à esquerda da string 
- maketrans() - Retorna uma tabela de tradução para ser usada nas traduções 
- partition() - Retorna uma tupla onde a string é dividida em três partes 
- replace() - Retorna uma string onde um valor especificado é substituído por um valor especificado 
- rfind() -  Procura na string por um valor especificado e retorna a última posição de onde foi encontrado 
- rindex() - Procura na string por um valor especificado e retorna a última posição de onde foi encontrado 
- rjust() -  Retorna uma versão justificada à direita da string 
- rpartition() -  Retorna uma tupla onde a string é dividida em três partes 
- rsplit() -  Divide a string no separador especificado e retorna uma lista 
- rstrip() - Retorna uma versão aparada à direita da string 
- split() -  Divide a string no separador especificado e retorna uma lista 
- splitlines() -  Divide a string nas quebras de linha e retorna uma lista 
- startswith() - Retorna verdadeiro se a string começar com o valor especificado 
- strip() -  Retorna uma versão aparada de a string 
- swapcase() - Troca maiúsculas e minúsculas e vice-versa 
- title() - Converte o primeiro caractere de cada palavra para maiúscula 
- translate() - Retorna uma string traduzida 
- upper() - Converte uma string para maiúscula 

#### Alguns Exemplos

~~~python
nome_maiusc = nome.upper()              # upper: passar para maiúsculo
nome_minusc = nome.lower()              # lower: passar para minúsculo
nome_modif = nome.replace("i", "x")     # replace: substituir caractere
nome_sem_esp = nome.strip()             # strip: remover espaços vazios início e fim
str_com_zeros = "5".zfill(3)            # zfill: preencher com zeros à esquerda: 005
str_nros = ' '.join(["3", "2", "1"])    # join: juntar elementos em uma string: 3 2 1
lista = "uva pera manga".split(' ')     # split: transformar string em lista
contagem = nome.count("i")              # count: contar ocorrências
indice_find = nome.find("i")            # find: Retorna a posição do primeiro 'i'
termina = nome.endswith("io")           # endswith: Verifica se termina com 'io': True
comeca = nome.startswith("Mau")         # startswith: Verifica se começa com 'ex': True
eh_alpha = nome.isalpha()               # isalpha: Verifica se é alfabético
eh_decimal = nome.isdecimal()           # isdecimal: Verifica se é decimal
eh_digito = nome.isdigit()              # isdigit: Verifica se é dígito
eh_numerico = nome.isnumeric()          # isnumeric: Verifica se é numérico

indice = nome.index("i")                # index: Retorna a posição do primeiro 'i'
retirar_esq = nome.lstrip()             # lstrip: Remove espaços à esquerda
retirar_dir = nome.rstrip()             # rstrip: Remove espaços à direita: exemplo
nome_capit = nome.capitalize()          # capitalize: converter o primeiro caractere em maiúsculas
nome_cent = nome.center(20, "-")        # center: centralizar string preenchendo com caractere
eh_alfanum = nome.isalnum()             # isalnum: Verifica se é alfanumérico
eh_minus = nome.islower()               # islower: Verifica se todos são minúsculos
eh_print = nome.isprintable()           # isprintable: Verifica se todos caracteres são imprimíveis: True
eh_maiusc = nome.isupper()              # isupper: Verifica se todos são maiúsculos
just_esq = nome.ljust(10, "-")          # ljust: Justifica à esquerda preenchendo com '-': exemplo---
ultimo_find = nome.rfind("i")           # rfind: Retorna última posição do 'i'
ultimo_index = nome.rindex("i")         # rindex: Retorna última posição do 'i'
just_dir = nome.rjust(10, "-")          # rjust: Justifica à direita preenchendo com '-': ---exemplo
troca_maiusc = "ExEmPlO".swapcase()          # swapcase: Troca maiúsculas por minúsculas e vice-versa: eXeMpLo
como_titulo = "exemplo de título".title()    # title: Converte para formato de título: Exemplo De Título
traduzir = "abc".translate({"a": "x"})       # translate: Aplica uma tradução: xbc
so_maiusc = "exemplo".upper()                # upper: Converte para maiúsculas: EXEMPLO
~~~