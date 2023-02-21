# Aprendizado de Máquina - Análise Estatística de um conjunto de dados

## Ler e exibir quantidade de linhas e colunas de um dataset

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.shape) # (linhas, colunas)
~~~

## Realizar análises estatísticas com describe()

Só opera em colunas com valores numéricos.  
25%: indica que 25% dos dados possuem valor menor que o representado na coluna.  

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.describe())
~~~

## Realizar análises estatísticas com describe() em apenas em uma coluna

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.describe()['mass']) 
~~~

## Realizar uma análise estatística específica com describe() em apenas em uma coluna

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.describe()['mass']['mean']) 
~~~