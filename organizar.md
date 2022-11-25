# Python

## Date

~~~python
# from datetime import date
current_date = date.today()
current_date = date.today().strftime('%d/%m/%Y') 
current_date = datetime.now()
current_date = datetime.now().strftime('%d/%m/%Y - %H:%M:%S')

# from datetime import datetime
current_date = datetime.now()
my_year = current_date.year
my_month = current_date.month
my_weekday = current_date.weekday()
my_day = current_date.day
my_hour = current_date.hour
my_minute = current_date.minute
my_second = current_date.second

my_tuple = ("Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday")
my_day = my_tuple[current_date.weekday()]

my_personal_date = datetime(2021, 3, 24, 15, 40, 20)

date_string = "01/01/2019"
date_formated = datetime.strptime(date_string, "%d/%m/%Y")

# from datetime import time
my_time = time(hour=17, minute=11, second=30)
my_time = time(hour=17, minute=11, second=30).strftime('%H:%M:%S')

# from datetime import datetime, timedelta
my_date = datetime(2021, 3, 30)
new_date = my_date - timedelta(days=365, hours=2, minutes=15)
~~~

## Math

~~~python
x = round(num)
x = floor(num)    # from math import floor
x = ceil(num)     # from math import ceil

x = sum(my_list)
x = max(my_list)
x = min(my_list)
x = len(my_list)

myVar = eval(expression)

x = bin(6)[2:] # binary - returns '110'
~~~

## JSON

~~~python

~~~

## RegEx

~~~python

~~~

## Python PIP

### Packages - Installing packages in python

- Package is a collection of modules.
- Pip is a package manager for Python.

~~~shell
pip --version
pip --help
pip freeze
pip list
pip install requests
~~~

## Exceptions

- [Built-in Exceptions Reference](https://www.w3schools.com/python/python_ref_exceptions.asp)

#### Ex.: exceptions - basic
~~~python
my_list = [1, 10]


try:
  #division = 10 / 0
  #x = my_list[2]
  x = a #
except ZeroDivisionError:
  print("Impossible to divide by zero.")
except IndexError:
  print("Invalid index.")
except BaseException as ex: 
  print("Unknown error. Error: {}".format(ex))
else:
  print("Code executed when there is no exception.")
finally:
  print("Excerpt that is always performed. Good to insert the .close () file here ")
~~~

#### Ex.: exceptions - custom exceptions

~~~python
class Error(Exception):
  pass

class InputError(Error):
  def __init__(self, message):
    self.message = message

while True:
  try:
    x = int(input("Enter a value from 0 to 10 "))
    if x > 10:
      raise InputError("Value cannot be greater than 10. ")
    elif x < 0:
      raise InputError("Value cannot be less than 0. ")
    break
  except ValueError:
    print("Invalid value. Enter numbers only. ")
  except InputError as ex:
    print(ex)
~~~

## User Input

~~~python
x = input("name:  ")        # python 3 - string
x = raw_input("name:  ")    # python 2 - string
a = int(input())
~~~

## User Output

- Formats: %f, %i

~~~python
print("Hi " + nome)
print("s = ", s, "p = ", p)
print("value = " + str(x))
print("value = %i" %x)
print("value = %0.4f" %x)
print("mauricio" * 3)
print(my_list)
print(my_list[0])

print("x = {} e y = {}".format(x, y))
print("MEDIA = {:.1f}".format(media))
print("x = {a} e y = {b}".format(a=x, b=y))
~~~

## String Formatting

~~~python

~~~


## File Handling

- [File Methods Reference](https://www.w3schools.com/python/python_ref_file.asp)

#### Ex.: Text Files - write and update

~~~python
def write_file(name_file, txt):
  my_file = open(name_file, "w")
  my_file.write(txt)
  my_file.close()

def change_file(name_file, txt):
  my_file = open(name_file, "a")
  my_file.write(txt)
  my_file.close()

if __name__ == "__main__":
  change_file("my txt\n")
~~~

#### Ex.: Text Files - read

~~~python
def le_my_file(name_file):
  my_file = open(name_file, "r")
  txt = my_file.read()
  linhas = txt.split("\n")
  print(linhas[0])
  print(linhas[-1])

if __name__ == "__main__":
  le_my_file("notes.txt")
~~~

#### Ex.: Files - copy a file

~~~python
import shutil  # biblioteca
def copy_my_file(name_file):
  shutil.copy(name_file, "./example") # copy o my_file para o diretorio example, renameando: ./example/novoname

if __name__ == "__main__":
  copy_my_file("notes.txt")
~~~

#### Ex.: Files - move a file

~~~python
import shutil  # biblioteca
def move_my_file(name_file):
  shutil.move(name_file, "./example")

if __name__ == "__main__":
  move_my_file("notes.txt")
~~~

- - - 

## How To Random numbers

~~~python
import random

print(random.randrange(1, 10))
~~~

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
