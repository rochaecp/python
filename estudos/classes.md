# Python - Classes e Objects

- Tudo em Python são objetos com propriedades e métodos.
- Todas as classes têm uma função chamada ```__init__()``` que é sempre executada quando a classe é instanciada.
- Use a função __init__() como método construtor.
- O parâmetro self é uma referência a instáncia corrente da classe e é usado para acessar variáveis que pertencem a classe.

## Criando uma classe

~~~python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def myfunc(self):
        print("Hello my name is " + self.name)
~~~   

~~~python
class Television:
    def __init__(self):
        self.ligada = False
        self.canal = 5
    def power(self):
        if self.ligada == True:
            self.ligada = False
        else:
            self.ligada = True
    def increase_channel(self):
        if self.ligada:
            self.canal += 1
~~~

## Criando um objeto

~~~python
p1 = Person("Mauricio", 30)
p1.myfunc()
~~~

~~~python
Television = Television()

print(Television.ligada)
Television.power()
print(Television.ligada)

print(Television.canal)
Television.increase_channel()
print(Television.canal)
~~~

## Modificando propriedades do objeto

~~~python
p1.age = 30
~~~

## Deletando uma propriedade de um objeto

~~~python
del p1.age 
~~~

## Deletando um objeto

~~~python
del p1
~~~
