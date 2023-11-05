# Numpy

## Criar um array

~~~python
import numpy as np

arr = np.array(42)                          # 0D - escalar
arr = np.array([-2, -1, 0, 1, 2])           # 1D - a partir de lista
arr = np.array((1, 2, 3, 4))                # 1D - a partir de tupla
arr = np.linspace(-2, 2, 10)                # 1D - a partir de intervalo - ini, fim, qtd
arr = np.array([[1, 2, 3], [4, 5, 6]])      # 2D

arr = np.array([[[1, 2, 3], [4, 5, 6]],
                [[7, 8, 9], [10, 11, 12]]]) # 3D

arr = np.array([1, 2, 3, 4], ndmin=5)       # Dimensões maiores
~~~