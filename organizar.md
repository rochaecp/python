# Python

## How To use webservice viacep

~~~python
import requests

response = requests.get("http://viacep.com.br/ws/91786599/json/")

print(response.status_code)   # 200 == sucess, 400 == not found
print(response.text)          
data_cep = response.json()   
print(data_cep["logradouro"])
~~~

### How To use API pokemons

~~~python
import requests

def retorna_data_pokemon(pokemon):
  response = requests.get("https://pokeapi.co/api/v2/pokemon/{}/".format(pokemon))
  data_pokemon = response.json()
  return data_pokemon

data_pokemon = retorna_data_pokemon("pikachu")
print(data_pokemon)
print(data_pokemon['sprites']['front_shiny']) # img
~~~

### How To get source code for any page

~~~python
import requests

def retorna_response(url):
  response = requests.get(url)
  return response.text

response = retorna_response('https://www.inf.ufrgs.br/site')
print(response)
~~~

### How read in URI

~~~python
# many values on the same line 
my_line = input().split()
my_list = list(map(int, my_line)) # map function transforms values to integers 

# many values in many lines - lists
my_list = []
for i in range(0, 6): # to read 6 float values
  my_list.append(float(input()))
~~~

### How To EOF in URI

~~~python
while True:
  try:
    # code here
  except EOFError:
    break
~~~

### .venv

~~~python
# criar uma venv
python3 -m venv .venv 

# ativar uma venv
. .venv/bin/activate
pip install --upgrade pip
make install-dependencies

jupyter notebook

# desativar uma venv
deactivate
~~~


## Links

- [Built in Functions Reference](https://www.w3schools.com/python/python_ref_functions.asp)
- [Google Colab](#)
- [Jupyter Notebook](https://jupyter.org/)
- [Kaggle](https://www.kaggle.com/)
- [Kaggle - Análise de dados do IBGE (Manaus-AM)](https://www.kaggle.com/maurciorocha/an-lise-de-dados-do-ibge-manaus-am/edit)
- [doc](https://docs.python.org/pt-br/3/library/)
- [oficial tutorial](https://docs.python.org/pt-br/3/tutorial/index.html)
- [w3schools](https://www.w3schools.com/python/)
- [Viacep](http://viacep.com.br/ws/91786599/json/) - webservice CEPs
- [pokeapi](https://pokeapi.co/api/v2/pokemon) - api

 To be continued

- [Youtube - Trybe](https://www.youtube.com/playlist?list=PLP6Z8YhN_d5QsIWuVqVFXqjHBssxqvp89)
- [ler PDFs - link Ricardo](https://colab.research.google.com/drive/1VLpWnbukrw9OgIvuBFtmDSOTZO4Mmkl_?usp=sharing)
- [GUI programming](https://www.tutorialspoint.com/python/python_gui_programming.htm)
- faster code in python 
- Data Structures in Python

https://www.w3schools.com/python/python_inheritance.asp
