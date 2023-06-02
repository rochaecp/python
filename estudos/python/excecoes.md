# Python - Exceptions

~~~python
my_list = [1, 10]

try:
    #division = 10 / 0
    #x = my_list[2]
    x = a #
except ZeroDivisionError:
    print("Impossível dividir por zero")
except IndexError:
    print("Indice inválido")
except BaseException as ex: 
    print("Unknown error. Error: {}".format(ex))
else:
    print("Code executed when there is no exception.")
finally:
    print("Excerpt that is always performed. Good to insert the .close () file here ")
~~~

## Exceção personalizada

~~~python
class Error(Exception):
    pass

class InputError(Error):
    def __init__(self, message):
        self.message = message

while True:
    try:
        x = int(input("Digite um número entre 0 e 10 "))
        if x > 10:
            raise InputError("Valor não pode ser maior do que 10 ")
        elif x < 0:
            raise InputError("Valor não pode ser menor do que 0 ")
        break
    except ValueError:
        print("Valor inválido. Digite apenas números ")
    except InputError as ex:
        print(ex)
~~~
