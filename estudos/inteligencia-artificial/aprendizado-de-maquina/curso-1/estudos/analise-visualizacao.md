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