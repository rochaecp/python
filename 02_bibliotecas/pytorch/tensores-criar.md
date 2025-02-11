# PyTorch - Tensores

# Criar

```python
import torch

# 0D inserindo valores manualmente
tns_m0 = torch.tensor(5)
print(tns_m0)
print()

# 1D com valores aleat a partir de distrib normal
tns_rn_1d = torch.randn(8)
print(tns_rn_1d)
print()

# 2D com zeros
tns_z = torch.zeros(2, 3)
print(tns_z)
print()

# 2D com uns
tns_o = torch.ones(2, 3)
print(tns_o)
print()

# 2D com valores aleat a partir de distrib normal
tns_rn = torch.randn(2, 3)
print(tns_rn)
print()

# 2D com valores aleat
tns_r = torch.rand(2, 3)
print(tns_r)
print()
```