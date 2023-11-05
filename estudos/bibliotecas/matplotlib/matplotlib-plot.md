# Matplotlib

## Plotar retas 2D

~~~python
import matplotlib.pyplot as plt
import numpy as np

# o num de pontos eixos x e y devem ser iguais
x = np.array([1, 2, 6, 8])      # array numpy a partir de lista
y = np.array([4, 8, 1, 10])

# So os pontos
#plt.plot(x, y, 'o')

# so a reta que conecta os pontos
#plt.plot(x, y)

# reta e os pontos
#plt.plot(x, y, marker = 'o')

# Strings de formato fmt
plt.plot(x, y, 'o:g') # o == marker, : == line, r == color

plt.show()
~~~

# Plotar múltiplas retas 2D

~~~python
import matplotlib.pyplot as plt
import numpy as np

x = np.array([1, 2, 6, 8])      # array numpy a partir de lista
y1 = 2 * x
y2 = 2 * x + 4

plt.plot(x, y1, color='b')
plt.plot(x, y2, color='y')

plt.show()
~~~

# Plotar Reta 2D e ponto

~~~python
import numpy as np
import matplotlib.pyplot as plt
~~~

~~~python
a = -1
b = 4
c = 0.4

x = np.linspace(-2, 4, 20)
y = (-a*x - c) / b

# reta
plt.plot(x, y)
plt.grid(True)
plt.axhline(0, -2, 4, color='k', linewidth=1)
plt.axvline(0, -1, 1, color='k', linewidth=1)
plt.title('Reta 2D e ponto')
plt.xlabel('x')
plt.ylabel('f(x)')

# ponto
p = (0, -0.1)
ret = a * p[0] + b * p[1] + c
print('ret = %.2f' % ret)
plt.plot(p[0], p[1], color='r', marker='o', markersize=7)
~~~

# Marcadores, linhas, cores, Format Strings fmt, markersize

- Fonte w3schools: https://www.w3schools.com/python/matplotlib_markers.asp
- Fonte doc oficial: https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html

~~~python
import matplotlib.pyplot as plt
import numpy as np

x = np.array([-2, -1, 0, 1])
y = 2 * x

# Alguns marcadores
# ---------------------

# plt.plot(x, y, marker='o')
#plt.plot(x, y, 'o')
#plt.plot(x, y, '*')
#plt.plot(x, y, '^')
#plt.plot(x, y, '>')
#plt.plot(x, y, '<')
# plt.plot(x, y, 'v')
#plt.plot(x, y, '.')
# plt.plot(x, y, 'x')
# plt.plot(x, y, 'X')
# plt.plot(x, y, 'P')
# plt.plot(x, y, 's')
# plt.plot(x, y, 'D')
# plt.plot(x, y, 'd')
# plt.plot(x, y, 'p')
# plt.plot(x, y, 'H')
# plt.plot(x, y, 'h')
# plt.plot(x, y, '1')
# plt.plot(x, y, '2')
# plt.plot(x, y, '3')
# plt.plot(x, y, '4')
# plt.plot(x, y, '|')
# plt.plot(x, y, '-')

# Algumas linhas
# ---------------------

# plt.plot(x, y, linestyle='dashed') # apelido: ls
# plt.plot(x, y, linestyle='None')
# plt.plot(x, y, '-') # solid (default)
# plt.plot(x, y, ':') # dotted
# plt.plot(x, y, '--') # dashed
# plt.plot(x, y, '-.') # dashdot

# Algumas cores
# ---------------------

# plt.plot(x, y, color = 'r')
# plt.plot(x, y, 'r')
# plt.plot(x, y, 'g')
# plt.plot(x, y, 'b')
# plt.plot(x, y, 'c')
# plt.plot(x, y, 'm')
# plt.plot(x, y, 'y')
# plt.plot(x, y, 'k')
# plt.plot(x, y, 'w')

# Format Strings fmt
# ---------------------

# plt.plot(x, y, 'o:r') #marker line color

# Marker size
# ---------------------

# plt.plot(x, y, 'o', markersize=10) # apelido: ms
# plt.plot(x, y, marker='o', markersize=10)

# Marker color - aceita cores em hexadecimal também, ou 140 color names
# ---------------------

# plt.plot(x, y, marker='o', markersize=20, markeredgecolor='g', markerfacecolor='r') # apelido: ms, mec, mfc

# Line color - aceita cores em hexadecimal também, ou 140 color names
# ---------------------

# plt.plot(x, y, color='r') # apelido: c

# Line Widh
# ---------------------

# plt.plot(x, y, linewidth=10) # apelido: lw

# Labels, Title
# ---------------------
# font1 = {'family': 'serif', 'color' : 'm', 'size': 20} # dicionario de fontes
# font2 = {'color' : 'g', 'size': 15} # dicionario de fontes

# plt.plot(x, y)

# plt.title('Titulo', fontdict=font1, loc='left') # loc = right, left, center (default)
# plt.xlabel('x label', fontdict=font2)
# plt.ylabel('y label', fontdict=font2)

# Grid
# ---------------------

# plt.plot(x, y)
# plt.grid(axis='x', color='g', linestyle='--', linewidth=0.5) # só eixo x
# plt.grid(axis='y', color='g', linestyle='--', linewidth=0.5) # só eixo y

# Exemplo completo
# ---------------------

fig_width, fig_height = plt.gcf().get_size_inches()
plt.figure(figsize=(fig_width*1.2, fig_height*1.2)) # aumenta figura

plt.plot(x, y, linestyle=':', color='r', linewidth=2,  marker='o',
         markersize='15', markeredgecolor='m', markerfacecolor='w')

font = {'family' : 'serif', 'color' : 'k', 'size' : 13}
plt.title('Gráfico', fontdict=font, loc='center')
plt.xlabel('eixo x', fontdict=font)
plt.ylabel('eixo y', fontdict=font)

plt.grid(color='g', linestyle='--', linewidth=0.5) # axis='x' == só eixo x
~~~

# Plotar múltiplos gráficos - Subplot

~~~python
import matplotlib.pyplot as plt
import numpy as np

x1 = np.array([-2, -1, 0, 1])
y1 = 2 * x1

x2 = np.array([-2, -1, 0, 1])
y2 = np.array([1, 2, 0, 1])

plt.figure(figsize=(15, 4))

# plot 1
plt.subplot(1, 2, 1) # linhas, colunas, index
plt.plot(x1, y1)
plt.title('Gráfico 1')

# plot 2
plt.subplot(1, 2, 2) # linhas, colunas, index
plt.plot(x2, y2)
plt.title('Gráfico 2')

plt.suptitle('Gráficos')
plt.show()
~~~
    
~~~python
import matplotlib.pyplot as plt
import numpy as np

x1 = np.array([-2, -1, 0, 1])
y1 = 2 * x1

x2 = np.array([-2, -1, 0, 1])
y2 = np.array([1, 2, 0, 1])

# plot 1
plt.subplot(2, 1, 1) # linhas, colunas, index
plt.plot(x1, y1)
plt.title('Gráfico 1')

plt.subplots_adjust(hspace=0.5) # espaço entre os gráficos

# plot 2
plt.subplot(2, 1, 2) # linhas, colunas, index
plt.plot(x2, y2)
plt.title('Gráfico 2')

plt.show()
~~~
