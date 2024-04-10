# PyTorch - Tensores

## Propriedades

~~~python
import torch

tns = torch.randn(3, 4)

# tipo
print(tns.dtype)
print()

# dimensões x e y
print(tns.shape)
print(tns.shape[0]) # dimensão x
print(tns.shape[1]) # dimensão x
print()
~~~

## Métodos

~~~python
import torch

tns = torch.randn(2, 2, 3)
print(tns)
print()

# dimensões x, y, z
print(tns.size())
print(tns.size(0))
print(tns.size(1))
print(tns.size(2))
print()

# redimensionar
print(tns.view(12))
print()

# redimensionar mantendo a primeira dimensão e achatando o restante
print(tns.view(tns.size(0), -1))
print()

# item()

~~~

# GPU Cast

- Incluir GPU no Collab:
    - Editar -> Configurações do Notebook

~~~python
import torch

tns = torch.randn(10)
print(tns)

# verifica se gpu está disponível
if torch.cuda.is_available():
    device = torch.device('cuda')
else:
    device = torch.device('cpu')
print(device)
print()

# jogar informações na gpu
tensor = tns.to(device)
print(tns)
~~~

# Exercícios

## Usando view

- Crie um tensor aleatório tns1 com a dimensionalidade 7 x 7 x 3 e um outro tensor aleatório tns2 de 147 x 1. Modificando apenas tns1 some os dois tensores.

~~~python
import torch

tns1 = torch.randn(7, 7, 3)
tns2 = torch.randn(147, 1)

tns1_modific = tns1.view(-1, 1) # achata o tensor
print(tns1_modific + tns2)
~~~
