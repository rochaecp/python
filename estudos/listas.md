# Python - Listas

- Listas são usadas para gravar múltiplos itens em uma mesma variável.
- Permitem: gravar itens de maneira ordenada, modificar os itens, itens duplicados.
- No Python, são objetos do tipo list.
- Não se pode copiar uma lista fazendo apenas ``` list2 = list1 ```. É necessário usar o método ```copy()```.

## Criando uma lista

~~~python
my_list = []
my_list = [1, 2, 3, 4]
my_list = ["apple", "banana", "cherry"]
~~~

## Criando uma lista com o construtor list()

~~~python
my_list = list("my_string")
my_list = list(my_tuple)
my_list = list(my_set)
~~~

## Acessando os elementos de uma lista

~~~python
item = my_list[0]   # first
item = my_list[-1]  # last
item = my_list[-2]
~~~

##

~~~python

~~~

##

~~~python

~~~

##

~~~python

~~~

##

~~~python

~~~

##

~~~python

~~~

##

~~~python

~~~

##

~~~python

~~~


~~~python

# Range of Indexes
my_list = my_list[2:5] # 2 (included) and end at index 5 (not included)
my_list = my_list[:3] # start at the first item, 3 (not included)
my_list = my_list[0:3]
my_list = my_list[2:] # 2 (included) to the end 
my_list = my_list[-2:]
my_list = my_list[-4:-1]

# Check if Item Exists
if "apple" in my_list:
  print("Yes, 'apple' is in my_list")

# Change Item Value
my_list[0] = "apple"
my_list[1:3] = ["apple", "cherry"] # change a range of item values

# Insert and Add List Items and Extend List
my_list.insert(1, "apple") # inserts an item at the specified index
my_list.append("apple") # add to the end
my_list.extend(my_list2) # add elementsof my_list2 to the end of my_list
my_list.extend(my_tuple) # add any iterable objects (tuple, set, dictionarie, etc)

# Remove List Items
my_list.remove("apple")
my_list.pop(1) # removes the specified index
my_list.pop(-1) # removes the last item
my_list.pop() # removes the last item
del my_list[0] # removes the specified index
del my_list # delete the list completely
my_list.clear()

# Loop Through a List
my_list = ["apple", "banana", "cherry"]
for x in my_list:
  print(x) 

# Loop Through the Index Numbers
my_list = ["apple", "banana", "cherry"]
for i in range(len(my_list)):
  print(my_list[i]) 

# Loop Using a While Loop
my_list = ["apple", "banana", "cherry"]
i = 0
while i < len(my_list):
  print(my_list[i])
  i = i + 1

# Looping Using List Comprehension
my_list = ["apple", "banana", "cherry"]
[print(x) for x in my_list] 

# List Comprehension - a shorter syntax when you want to create a new list based on the values of an existing list.
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
my_list = [x for x in fruits] # copy the list fruits
my_list = [x for x in fruits if "a" in x] # fruits with the letter "a" in the name
my_list = [x for x in fruits if x[0] == "a"]
my_list = [x.upper() for x in fruits] 
my_list = [x * 2 for x in range(10)]
my_list = [x for x in range(10) if x % 2 == 0]
my_list = [x if x != "banana" else "orange" for x in fruits] # returns orange instead of banana

# Sort Lists
my_list.sort() # all capital letters being sorted before lower case letters == case sensitive
my_list.sort(reverse = True)
my_list.reverse()

# Customize Sort Function

## Sort the list based on how close the number is to 50
def myFunction(n):
  return abs(n - 50)
my_list = [100, 50, 65, 82, 23]
my_list.sort(key = myFunction)

## Case Insensitive Sort
my_list = ["banana", "Orange", "Kiwi", "cherry"]
my_list.sort(key = str.lower)

# Copy Lists
my_list_cpy = my_list.copy()

# Copy Lists - another way
my_list_cpy = list(my_list)

# Join Lists
list3 = list1 + list2
list1.extend(list2)

# Join Lists
for x in list2:
  list1.append(x)

# Other methods
counter = my_list.count("apple")
index = my_list.index("apple")
my_len = len(my_list)
my_sum = sum(my_list)
my_max = max(my_list)
my_min = min(my_list)

# Eliminating duplicate items and order
my_list = [5, 1, 1, 2, 2, 3, 4, 4]
my_set = set(my_list)
my_list = list(my_set)
~~~
