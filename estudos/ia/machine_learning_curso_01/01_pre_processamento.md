# Ler e exibir um dataset

## Ler e exibir um dataset a partir de um arquivo de texto

- `sep='\t'`: usa tabulações como separador

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas)
~~~

## Ler e exibir as primeiras n linhas de um dataset

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.head(5))
~~~

## Ler e exibir apenas uma coluna de um dataset

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas['color_score']) # exibe somente a coluna color_score
~~~

## Ler e exibir 2 ou mais colunas de um dataset

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas[['mass', 'color_score']])
~~~

## Ler e exibir um intervalo de linhas de um dataset

- O intervalo é fechado no início e aberto no fim.

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas[10:15]) # exibe da linha 10 até a linha 15 (não incluindo o 15)

import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
i = 15
print(frutas[i-5:i]) # exibe da linha 10 até a linha 14
print(frutas[i:i+5]) # exibe da linha 15 até a linha 19
~~~

## Ler e exibir algumas colunas de algumas linhas

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
i = 15
print(frutas[['mass', 'color_score']][i:i+5]) # exibe mass e color_score da linha 15 a 19
~~~

# Análise Estatística de um conjunto de dados

## Ler e exibir quantidade de linhas e colunas de um dataset

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas.shape) # (linhas, colunas)
print(frutas.shape[0]) # (linhas)
~~~

## Realizar análises estatísticas com describe()

- Só opera em colunas com valores numéricos.  
- 25%: indica que 25% dos dados possuem valor menor que o representado na coluna.

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

# Análise e visualização de um Conjunto de Dados

## Exibir quantas vezes uma variável aparece no conjunto de dados

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
freq = frutas['fruit_name'].value_counts()
print(freq)
~~~

## Exibir apenas linhas do dataset que representam maçãs

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
macas = frutas['fruit_name'] == 'apple'
print(frutas[macas])
~~~

## Exibir apenas linhas do dataset que representam maçãs com uma massa maior que 175

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
macas = frutas['fruit_name'] == 'apple'
pesadas = frutas['mass'] > 175
print(frutas[macas & pesadas])
~~~

## Exibir um gráfico com o eixo x == largura e o y == altura de maçãs com massa maior que 175

~~~python
import matplotlib.pyplot as plt
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
macas = frutas['fruit_name'] == 'apple'
pesadas = frutas['mass'] > 175
X1 = frutas[macas & pesadas]['width']
X2 = frutas[macas & pesadas]['height']

plt.scatter(X1, X2)
plt.xlabel('Comprimento')
plt.ylabel('Altura')
plt.show()
~~~

## Exibir um gráfico com todas as informações de comprimento e altura de todas as frutas

~~~python
import matplotlib.pyplot as plt
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
X1 = frutas['width']
X2 = frutas['height']

plt.scatter(X1, X2)
plt.xlabel('Comprimento')
plt.ylabel('Altura')
plt.show()
~~~

## Exibir um gráfico com todas as informações de comprimento e altura de todas as frutas com rótulos coloridos

~~~python
import matplotlib.pyplot as plt
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
X1 = frutas['width']
X2 = frutas['height']
y = frutas['fruit_label']

plt.scatter(X1, X2, c=y)
plt.xlabel('Comprimento')
plt.ylabel('Altura')
plt.show()
~~~

# Introdução ao pré-processamento de dados com Python

## Imputar (injetar dados) dados faltantes

- O dataset trabalhado aqui é o **fruit_data_with_colors_miss.txt**.  
- Em algumas colunas há pontos de interrogação e carateres de ponto no lugar de dados faltantes.  
- parâmetro ```na_values```: lista de valores faltantes (representados no exemplo pelo ponto e pela interrogação).
- É **ineficiente** quando estão faltando muitos dados no conjunto.

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

- A média de cada coluna é utilizada para imputar os dados faltantes.  
- Não funciona bem para colunas textuais (foi utilizado o nome do elemento que mais aparece na coluna).

~~~python
import pandas as pd

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt',na_values=['.', '?'])

# colunas com dados faltantes recebe a média da coluna
data = data.fillna(data.mean())

# corrige para colunas textuais com elemento que mais aparece na coluna
data['fruit_subtype'] = data['fruit_subtype'].fillna(data['fruit_subtype'].value_counts().argmax())

print(data)
~~~

## Eliminação de Colunas

- Pode ser usada quando faltam muitos dados em uma coluna.  
- Exemplo de abordagem: se a % de dados faltantes for superior a 25% então eliminar a coluna.

~~~python
import pandas as pd

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt',na_values=['.', '?'])

print(data.shape[0])                                # total de dados
print(data.isnull().sum())                          # colunas x total de dados faltantes na coluna
print(data.isnull().sum() / data.shape[0] * 100)    # % de dados faltantes

# eliminando a coluna
data = data[['fruit_label', 'fruit_name', 'fruit_subtype', 'width', 'height', 'color_score']] # colunas que desejamos manter
~~~

## Transformar a escala dos dados

- Para cada coluna iremos escalar os valores para o intervalo [0; 1]:   
- ```valor_escalado = (valor_para_transformar - menor_valor_coluna) / (maior_valor_coluna - menor_valor_coluna)```  
- Descartar colunas que possuam todos os valores iguais.  
- Utilizaremos o sklearn.

~~~python
import pandas as pd
from sklearn.preprocessing import MinMaxScaler # classe que transforma a escala dos dados

data = pd.read_table('datasets/fruit_data_with_colors_miss.txt', na_values=['.', '?'])
data = data.fillna(data.mean())                         # imputação dos dados faltantes com a média
data = data[['mass', 'width', 'height', 'color_score']] # seleciona apenas colunas com dados numéricos

#print(data.describe()) # observar que dados estão em escalas diferentes

mm = MinMaxScaler()
mm.fit(data) # obtem maximo e minimo do dataset
data_escalados = mm.transform(data) # obtem dados escalados
print(data_escalados)
~~~