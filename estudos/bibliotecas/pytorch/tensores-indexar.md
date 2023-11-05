# PyTorch - Tensores

# Indexação

```python
import torch

# criar
tns = torch.randn(3, 4)
print(tns)
print()

# alterar
tns[0, 1] = 10
print(tns)
print()

# slice
print(tns[0, 0])
print(tns[0:2]) # printa linhas 0 e 1
print(tns[0:2, 0:2]) # até linha 1 e ate col 1
print()

print(tns[1:, 2:]) # linha 1 em diante e coluna 2 em diante
print(tns[:, 1]) # printa todas linhas da coluna 1
print()
```