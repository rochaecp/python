# Python - Classes/Objects

- Everything in Python is an object, with its properties and methods.
- All classes have a built-in function called __init__(), which is always executed when the class is being initiated.
- Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created
- The __init__() function is called automatically every time the class is being used to create a new object.
- The self parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.
  - It does not have to be named self , you can call it whatever you like, but it has to be the first parameter of any function in the class.

~~~python
# Create a Class - The __init__() Function
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
  def myfunc(self):
    print("Hello my name is " + self.name)

# Create Object
p1 = Person("John", 36)
p1.myfunc()

# Modify Object Properties
p1.age = 30

# Delete Object Properties
del p1.age 

# Delete Objects
del p1

# Another example
class Television:
  def __init__(self):
    self.ligada = False
    self.canal = 5
  def power(self):
    if self.ligada == True:
      self.ligada = False
    else:
      self.ligada = True
  def increase_channel(self):
    if self.ligada:
      self.canal += 1
Television = Television()
print(Television.ligada)
Television.power()
print(Television.ligada)
print(Television.canal)
Television.increase_channel()
print(Television.canal)
~~~
