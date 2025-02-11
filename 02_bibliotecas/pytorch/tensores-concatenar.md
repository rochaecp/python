# PyTorch - Tensores

# Concatenar

```python
import torch

tns_a = torch.randn(2)
tns_b = torch.randn(3)

tns_concat = torch.cat((tns_a, tns_b), dim=0)
print(tns_concat)
```