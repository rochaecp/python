# PyTorch - Tensores

# Converter

## Lista em Tensor

```python
import torch

lista = [[1, 2, 3],
         [3, 4, 5]]

# para formato default (float)
tns_f = torch.Tensor(lista)
print(tns_f.dtype)
print(tns_f)
print()

# explicitamente para float
tns_f = torch.FloatTensor(lista)
print(tns_f.dtype)
print(tns_f)
print()

# explicitamente para double
tns_d = torch.DoubleTensor(lista)
print(tns_d.dtype)
print(tns_d)
print()

# explicitamente para long
tns_l = torch.LongTensor(lista)
print(tns_l.dtype)
print(tns_l)
print()
```

## Array Numpy em Tensor

```python
import torch
import numpy as np

# cria array float
arr = np.random.rand(3,4)
print(arr)
print(arr.dtype)
print()

# converte par atensor float
tns = torch.from_numpy(arr)
print(tns)
print(tns.dtype)
print()

# cria array int
arr_int = arr.astype(int)
print(arr_int)
print(arr_int.dtype)
print()

# converte para tensor int
tns_int = torch.from_numpy(arr_int)
print(tns_int)
print(tns_int.dtype)
print()
```

## Tensor em Array Numpy

```python
import torch

tns = torch.randn(2, 3)

arr = tns.data.numpy()
print(arr)
print(type(arr))
```