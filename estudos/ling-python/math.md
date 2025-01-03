# Math

## Funções diversas

~~~python
minha_lista = [1, 2, 3]

a = sum(minha_lista) # 6 
b = max(minha_lista) # 3
c = min(minha_lista) # 1
d = len(minha_lista) # 3
~~~

~~~python
a = eval("2 + 3 * 2") # 8
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
