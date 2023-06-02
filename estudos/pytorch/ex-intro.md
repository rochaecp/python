# Exemplos Introdutórios

~~~python
import torch

a = torch.tensor(2) # cria tensor com valor 2
b = torch.tensor(1) # cria tensor com valor 1

#print(a + b) # soma 2 tensores

# if torch.cuda.is_available():
#     print("Possui cuda")
# else:
#     print("Não possui cuda")    

ones_tensor = torch.ones((2, 2)) # tensor 2x2 com apenas valores 1
#print(ones_tensor)
randan_tensor = torch.rand((2, 2)) # tensor 2x2 com valores aleatorios
#print(randan_tensor)
'''
~~~