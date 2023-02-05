# Python - Api Pokemon

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
