# Leitura e exibição de um dataset

## Ler e exibir um dataset a partir de um arquivo de texto

sep='\t': usa tabulações como separador

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

O intervalo é fechado no início e aberto no fim.  

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
print(frutas[10:15]) # exibe da linha 10 até a linha 15 (não incluindo o 15)
~~~

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
i = 15
print(frutas[i-5:i]) # exibe da linha 10 até a linha 14
print(frutas[i:i+5]) # exibe da linha 15 até a linha 19
~~~

## Ler e exibir algumas colunas de algumas linahs

~~~python
import pandas as pd

frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t')
i = 15
print(frutas[['mass', 'color_score']][i:i+5]) # exibe mass e color_score da linha 15 a 19
~~~