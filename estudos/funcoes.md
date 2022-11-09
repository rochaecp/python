# Python - Funções

## Função sem parâmetros

~~~python
def myFunc():
    print("Hello from a function") 

myFunc()
~~~

## Função com parâmetros

~~~python
def myFunc(fname, lname): # parametros
    print("Hi " + name + " " + lname)

myFunc("Mauricio", "Rocha") # argumentos
~~~

## Função com parâmetros default

~~~python
def myFunc(country = "Norway"):
    print("I am from " + country)

myFunc()
myFunc("Brazil") 
~~~

## Função com argumentos nomeados

~~~python
def myFunc(child3, child2, child1):
    print("The youngest child is " + child3)

myFunc(child1 = "Emil", child2 = "Tobias", child3 = "Linus") 
~~~

## Função com quantidade de parâmetros variável

~~~python
def myFunc(*kids):
    print("The youngest child is " + kids[2])

myFunc("Emil", "Tobias", "Linus") 
~~~

~~~python
def myFunc(**kid):
    print("His last name is " + kid["lname"])

myFunc(fname = "Tobias", lname = "Refsnes") 
~~~

## Função recebendo uma lista como parâmetro

~~~python
def myFunc(food):
    for x in food:
        print(x)

fruits = ["apple", "banana", "cherry"]
myFunc(fruits)
~~~

## Função retornando mais de um valor

~~~python
def myFunc(a = 1, b = 2):
    return a + b, a * b

s, p = myFunc()
~~~

## Função acessando variável global

~~~python
x = 10

def mudaNumero():
    global x
    x = 20

mudaNumero()
print(x)
~~~
