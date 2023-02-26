# Introdução ao pré-processamento de dados com Python

## Imputar (injetar dados) dados faltantes

O dataset trabalhado aqui é o fruit_data_with_colors_miss.txt.  
Em algumas colunas há pontos de interrogação e carateres de ponto no lugar de dados faltantes.  
parâmetro ```na_values```: lista de valores faltantes (representados no exemplo pelo ponto e pela interrogação).  

#### Substituir valores faltantes por NaN

~~~python
import pandas as pd

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt',na_values=['.', '?']) 
print(data)
~~~

#### Substituir valores faltantes por zero

~~~python
import pandas as pd

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt',na_values=['.', '?']) 
data.fillna(0)
print(data)
~~~

#### Substituir valores faltantes pela média da coluna

A média de cada coluna é utilizada para imputar os dados faltantes.  
Não funciona bem para colunas textuais (foi utilizado o nome do elemento que mais aparece na coluna).  

~~~python
import pandas as pd

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt',na_values=['.', '?']) 

# colunas com dados faltantes recebe a média da coluna
data = data.fillna(data.mean())

# corrige para colunas textuais com elemento que mais aparece na coluna
data['fruit_subtype'] = data['fruit_subtype'].fillna(data['fruit_subtype'].value_counts().argmax())

print(data)
~~~