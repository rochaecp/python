# Numpy

## Indexar / Slicing

~~~python
import numpy as np

# Arrays 1D
arr = np.array([1, 2, 3, 4])
elem = arr[0] # primeiro
elem = arr[-1] # ultimo

# Arrays 2D
arr = np.array([[1, 2, 3], [4, 5, 6]])
elem = arr[0][0] # na linha 0, o primeiro elemento
elem = arr[0, 0] # na linha 0, o primeiro elemento
elem = arr[0, -1] # na linha 0, o último elemento
elem = arr[-1, -1] # na última linha, o último elemento

# Arrays 3D
arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
elem = arr[0, 1, 2] # primeira dimensão, segunda, terceira

elem
~~~

~~~python
import numpy as np

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

slc = arr[0, 1:] # na linha 0, os elem de indice 1 pra cima
slc = arr[0, :] # na linha 0, todos elementos
slc = arr[:, 0] # em todas as linhas, todos elementos de indice 0
slc = arr[:, 1] # em todas as linhas, todos elementos de indice 1
slc = arr[:, :] # todos elementos de todas linhas e colunas
~~~

