# Python - Lambda

- Uma função lambda é uma função anônima. 
- Pode ter muitos argumentos mas apenas uma expressão
- Sintaxe:
    - ```lambda argumentos : expressão```

~~~python
my_sum = lambda a, b: a + b 
x = my_sum(5, 10)
~~~

~~~python
square = lambda a: a ** 2
x = square(9)
~~~

~~~python
min = lambda a, b: a if a < b else b
x = min(10, 20)
~~~

~~~python
def myfunc(n):
    return lambda a : a * n

mydoubler = myfunc(2)
print(mydoubler(11))
~~~

~~~python
letter_counter = lambda my_list: [len(x) for x in my_list] # output == list
my_list_animais = ["dog", "cat", "horse"]
print(letter_counter(my_list_animais))
~~~

Calculadora com dicionários:

~~~python
my_dict = {
    'my_sum': lambda a, b: a + b,
    'subtraction': lambda a, b: a - b,
    'multiplication': lambda a, b: a * b,
    'division': lambda a, b: a / b,
}

my_sum = my_dict['my_sum']
my_mult = my_dict['multiplication']

print(type(my_dict))

print(my_sum(10, 5))
print(my_mult(10, 5))
~~~

Ordenação com dicionários:

~~~python
my_list = {1: 2, 3: 4, 4: 3, 2: 1, 0: 0}
my_ordered_list = {k: v for k, v in sorted(my_list.items(), key=lambda item: item[1])}

print(my_ordered_list)
~~~
