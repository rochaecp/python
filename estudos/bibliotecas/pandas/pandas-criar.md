# Pandas

## Criar Séries - 1 dimensão

- São equivalentes a 1 coluna de uma tabela

~~~python
import pandas as pd

lista = [10, 20, 30]
labels = ["x", "y", "z"]

# criar
ser = pd.Series(lista, index = labels) # index = arg opcional
print(ser)
print()

print(ser[0])
print(ser["y"]) # nome da coluna é indexável
print()
~~~

~~~python
import pandas as pd

# cria dicionario (objeto)
obj = {"nome1": "Mauricio", "nome2": "Vitoria", "nome3": "Savanah" }

df = pd.Series(obj)
print(df)
print()

# extrair parte
df_2 = pd.Series(obj, index = ["nome1", "nome3"])
print(df_2)
~~~

## Criar DataFrame - 2 dimensões

- são arrays de 2 dimensões

~~~python
import pandas as pd

dados = {
    "frutas": ["Banana", "Morango", "Kiwi"],
    "massas": [10, 1, 5]
}

df = pd.DataFrame(dados)
print(df)
print()
~~~
