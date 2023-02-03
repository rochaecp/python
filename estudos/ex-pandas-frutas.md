# Análise de Dados com Pandas

## Pré-requisitos

- Biblioteca Pandas

Instalando a biblioteca Pandas:

~~~bash
pip install pandas
~~~

## Análise de Dados com Pandas

Pandas é uma biblioteca que pode ser utilizada para efetuar a leitura de um conjunto de dados.  

~~~python
import pandas as pd # as cria apelido

'''
    read_table é um método do pandas para ler arquivos
    sep indica o separador a ser utilizado para distinguir as colunas
'''
frutas = pd.read_table('datasets/fruit_data_with_colors.txt',sep='\t') 

#print(frutas) # ou apenas frutas no jupyter

#print(frutas.shape) # quantidade de linhas e de colunas

#print(frutas.head(5)) # exibe 5 primeiras linhas

'''
    gera tabela com análises estatísticas das 
    colunas númericas do conjunto de dados
    25% dos dados possuem valor menor ao apresentado 
    na linha "25%" (o mesmo para 50% e 75%)
'''
#print(frutas.describe()) 

#print(frutas.describe()['mass']) # pega info apenas da coluna de massas

#print(frutas.describe()['mass']['min']) # pega so min para massa
~~~
