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

Formatando pontos flutuantes: ```%f```, ```%i```.    

~~~python
print("Hi " + nome)
print("s = ", s, "p = ", p)
print("value = " + str(x))
print("value = %i" %x)
print("value = %0.4f" %x)
print("mauricio" * 3)
print(my_list)
print(my_list[0])

print("x = {} e y = {}".format(x, y))
print("MEDIA = {:.1f}".format(media))
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

# float
print("Salario: %i" %salario)
print("Salario: %0.2f" %salario)
print("Salario: {:.1f}".format(salario))
print()

# listas
print("Linguagens:", linguagens)
print("Linguagem 1: " +  linguagens[0])
print()
~~~
