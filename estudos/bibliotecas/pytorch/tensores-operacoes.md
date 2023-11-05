# PyTorch - Tensores

# Operações

```python
import torch

tns_a = torch.ones(2, 3)
tns_b = torch.randn(2, 3)
print(tns_a)
print(tns_b)
print("-" * 40)
print()

# somar
print(tns_a + tns_b)
print()

# subtrair
print(tns_a - tns_b)
print()

# multiplicar ponto a ponto
print(tns_a * tns_b)
print()

# dividir
print(tns_a / tns_b)
print()
```

```python
import torchgen

tns_a = torch.randn(2, 3)
tns_b = torch.randn(3, 1)
print(tns_a)
print(tns_b)
print("-" * 40)
print()

# produto interno 2D (multiplicação de matrizes "tradicional")
print(torch.mm(tns_a, tns_b))
print()
```