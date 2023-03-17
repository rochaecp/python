# Python - Matplotlib - Pyplot - Marcadores

## Marcadores

| Marcador      | Descrição |
| :---:         | :---:     |
| ```'o'```     |           |
| ```'*'```     |           |
| ```'.'```     |           |
| ```','```     |           |
| ```'x'```     |           |
| ```'X'```     |           |
| ```'+'```     |           |
| ```'P'```     |           |
| ```'s'```     |           |
| ```'D'```     |           |
| ```'d'```     |           |
| ```'p'```     |           |
| ```'H'```     |           |
| ```'h'```     |           |
| ```'v'```     |           |
| ```'^'```     |           |
| ```'<'```     |           |
| ```'>'```     |           |
| ```'1'```     |           |
| ```'2'```     |           |
| ```'3'```     |           |
| ```'4'```     |           |
| ```'|'```     |           |
| ```'_'```     |           |

## Linhas

| Linha         | Descrição                     |
| :---:         | :---:                         |
| ```'-'```     | Linha sólida                  |
| ```':'```     | Linha pontilhada              |
| ```'--'```    | Linha tracejada               |
| ```'-.'```    | Linha tracejada/pontilhada    |

## Cores

| Cor           | Descrição |
| :---:         | :---:     |
| ```'r'```     | red       |
| ```'g'```     | blue      |
| ```'b'```     | green     |
| ```'c'```     | cyan      |
| ```'m'```     | magenta   |
| ```'y'```     | yellow    |
| ```'k'```     | black     |
| ```'w'```     | white     |

## Plotar pontos com 'o' conectados por retas

~~~python
import matplotlib.pyplot as plt
import numpy as np

coordenadas_y = np.array([3, 8, 1, 10])

plt.plot(coordenadas_y, marker = 'o')
plt.show()
~~~

## Strings de formato fmt

É uma notação mais curta para especificar: marker line color.

~~~python
import matplotlib.pyplot as plt
import numpy as np

coordenadas_y = np.array([3, 8, 1, 10])
plt.plot(coordenadas_y, 'o:r') # o == pontos, : == linha pontilhada, r == vermelha
plt.show()
~~~

## Alterar o tamanho do marcador

~~~python

~~~