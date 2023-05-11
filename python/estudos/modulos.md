# Python - Módulos

Cada arquivo .py é um módulo.  
Em um módulo podemos ter diversas classes.  
Uma classe não precisa possuir o mesmo nome do módulo que a contém.  
Importamos módulos omitindo a extensão .py.  

## Criando de uma classe em um módulo

Arquivo Television.py:

~~~python
class Television:
    def __init__(self):
        self.tv_is_on = False
        self.canal = 5
    def power(self):
        if self.tv_is_on == True:
            self.tv_is_on = False
        else:
            self.tv_is_on = True
    def increase_channel(self):
        if self.tv_is_on:
            self.canal += 1
~~~

Rodando o exemplo no terminal:

~~~bash
python3
import Television
t = Television.Television()
t.tv_is_on
t.power()
~~~

Rodando o exemplo no terminal (outra forma):

~~~bash
python3
from Television import Television
t = Television()
t.tv_is_on
~~~

#### Ex.: modules

~~~python
## File Television.py
class Television:
    def __init__(self):
        self.tv_is_on = False
        self.canal = 5
    def power(self):
        if self.tv_is_on == True:
            self.tv_is_on = False
        else:
            self.tv_is_on = True
    def increase_channel(self):
        if self.tv_is_on:
            self.canal += 1

print(__name__)

if __name__ == '__main__':
    Television = Television()
    print(Television.tv_is_on)
    Television.power()
    print(Television.tv_is_on)
    print(Television.canal)
    Television.increase_channel()
    print(Television.canal)

## ## on Terminal - test 1
python3 Television.py

## ## on Terminal - test 2
python3
import Television
~~~

#### Ex.: modules - import classes - File myTest.py

~~~python
from Television import Television
t = Television()
print(t.tv_is_on)
t.power()
print(t.tv_is_on)
~~~

#### Ex.: modules - import classes - File myTest.py

~~~python
from nameModule import nameFunction1, nameFunction2
x = nameFunction1()
y = nameFunction2()
~~~