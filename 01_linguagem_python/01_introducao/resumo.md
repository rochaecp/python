# Console

~~~python
variavel = 12.3456
print(f"{variavel:.2f}") # 12.35
~~~

# Números Aleatórios

~~~python
import random

num_aleat = random.randrange(1, 10) # 1 a 9
~~~

# Strings

~~~python
nome = "Mauricio"                       # criar
msg = "Bem vindo " + nome               # concatenar
tamanho = len(nome)                     # tamanho
primeira_letra = nome[0]                # indexar
ultima_letra = nome[0]                  # indexar
uma_fatia = nome[2:3]                   # slice: 2 (incluso), 3 (não incluso)
uma_fatia = nome[-3]                    # slice: últimos 3
uma_fatia = nome[:3]                    # slice: até terceira posição
nome_inv = nome[::-1]                   # slice: inverter string
meu_unicode = ord("A")                  # caractere em unicode
letra = chr(35)                         # unicode em caractere
meu_boolean = "a" in nome               # testar string
meu_boolean = "a" not in nome           # testar string

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

# Modificar um caractere em uma posição
lista = list(nome)
lista[0] = "J"
nome_modif = "".join(lista)
~~~

# Datas

~~~python

~~~

# Funções

~~~python

~~~

# Listas

~~~python

~~~

# Dicionários

~~~python

~~~

# Arquivos

~~~python

~~~

# Exceções

~~~python

~~~

# POO

~~~python

~~~