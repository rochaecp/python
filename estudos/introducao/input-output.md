# Inputs e Outputs pelo console

## Input

~~~python
x = input("name:  ")        # python 3 - string
x = raw_input("name:  ")    # python 2 - string
a = int(input())
n2 = float(input())
~~~

~~~python
x_str = input("Nome: ")
x_int = int(input("Idade: "))
x_float = float(input("Salario: "))
~~~

## Output

#### Pontos Flutantes

- `.2f`: formata o número com 2 casas decimais

~~~python
variavel = 12.3456
print(f"{variavel:.2f}") #12.35
~~~

~~~python
print("value = %0.4f" %x)
print("MEDIA = {:.1f}".format(media))
~~~

~~~python
salario = 15340.45
print("Salario: %i" %salario)
print("Salario: %0.2f" %salario)
print("Salario: {:.1f}".format(salario))
~~~

##### Alterando para o padrão brasileiro 

- vírgulas para decimais e pontos para milhares

~~~python
import locale

locale.setlocale(locale.LC_ALL, 'pt_BR.UTF-8') # Configurando o locale para o Brasil
numero = 1234567.89
print(locale.format_string("%.2f", numero, grouping=True)) #1.234.567,89
~~~

#### Diversos

~~~python
print("Hi " + nome)
print("s = ", s, "p = ", p)
print("value = " + str(x))
print("value = %i" %x)
print("mauricio" * 3)
print(my_list)
print(my_list[0])
print("x = {} e y = {}".format(x, y))
print("x = {a} e y = {b}".format(a=x, b=y))
~~~

~~~python
nome = "Mauricio"
idade = 31
salario = 15340.45
linguagens = ["JavaScript", "Python", "C#"]

print("Nome: " + nome)
print("Nome " * 3)
print()

print("Nome:", nome, "idade:", idade)
print("Idade: " + str(idade))
print("Nome = {} e Idade = {}".format(nome, idade))
print("Nome = {a} e Idade = {b}".format(a=nome, b=idade))
print()

# listas
print("Linguagens:", linguagens)
print("Linguagem 1: " +  linguagens[0])
print()
~~~
