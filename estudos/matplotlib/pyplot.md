# Python - Matplotlib - Pyplot

É um submódulo.  
Geralmente utilizamos o alias ```plt``` na importação do submódulo Pyplot.  

## Plotar uma reta de um ponto inicial até um ponto final - Função plot()

Desenha retas de ponto a ponto.  

~~~python
import matplotlib.pyplot as plt 
import numpy as np

coordenadas_x = np.array([0, 6])
coordenadas_y = np.array([0, 250])

plt.plot(coordenadas_x, coordenadas_y)
plt.show()
~~~

## Plotar 2 pontos sem usar uma reta - Função plot()

~~~python
import matplotlib.pyplot as plt 
import numpy as np

coordenadas_x = np.array([0, 6])
coordenadas_y = np.array([0, 250])

plt.plot(coordenadas_x, coordenadas_y, 'o')
plt.show()
~~~

## Plotar multiplos pontos conectados por retas - Função plot()

> Obs.: o número de pontos nos eixos x e y devem ser iguais!  

~~~python
import matplotlib.pyplot as plt 
import numpy as np

coordenadas_x = np.array([1, 2, 6, 8])
coordenadas_y = np.array([3, 8, 1, 10])

plt.plot(coordenadas_x, coordenadas_y)
plt.show()
~~~

## Plotar múltiplos pontos sem especificar as coordenadas x - Função plot()

> Obs.: por padrão o eixo x receberá os valores: 0, 1, 2, 3, ...

~~~python
import matplotlib.pyplot as plt 
import numpy as np

coordenadas_y = np.array([3, 8, 1, 10])

plt.plot(coordenadas_y)
plt.show()
~~~