# Math

## Funções diversas

~~~python
x = sum(my_list)
x = max(my_list)
x = min(my_list)
x = len(my_list)
~~~

~~~python
myVar = eval(expression)
~~~

## Convertendo um número para a base binária

~~~python
x = bin(6)[2:] # binary - returns '110'
~~~

## Gerando o gráfico da função cosseno

~~~python
import math
import numpy as np
import matplotlib.pyplot as plt

in_array = np.linspace(-(2 * np.pi), 2 * np.pi, 20)

out_array = []

for i in range(len(in_array)):
    out_array.append(math.cos(in_array[i]))
    i += 1

plt.plot(in_array, out_array, color = 'red', marker = "o")
plt.title("math.cos()")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()
~~~
