# Python - Conjuntos (sets)

- Set is a collection which is unordered and unindexed. No duplicate members.
- Sets are unordered, so you cannot be sure in which order the items will appear.
- Set items are unordered, unchangeable, and do not allow duplicate values.
- Set items can be of any data type.
- [Set Methods Reference](https://www.w3schools.com/python/python_ref_set.asp)

~~~python
# Creating a set
my_set = {"apple", "banana", "cherry"}

# The set() Constructor
my_set = set(("apple", "banana", "cherry")) # note the double round-brackets

# Duplicates Not Allowed
my_set = {"apple", "banana", "cherry", "apple"}
my_set = {1, 2, 3, 3, 3}

# Get the Length of a Set
my_len = len(my_set)

# Access Items
## You cannot access items in a set by referring to an index or a key.
for x in my_set:
  print(x) 

# Check if "banana" is present in the set
my_bool = "banana" in my_set

# Change Items
## Once a set is created, you cannot change its items, but you can add new items.

# Add Items
my_set.add("orange")

# Add Sets or any iterable object (tuples, lists, dictionaries etc.)
my_set.update(my_set2) # add items from my_set2 set into my_set
my_set.update(my_list) # add items from the list into my_set

# Remove Item
my_set.remove("banana") # raise an error if dont exist
my_set.discard("banana") # dont raise an error if dont exist
last_item = my_set.pop() # remember: the sets are unordered
my_set.clear() # empties the set
del my_set # delete the set completely

# Loop Items
for item in my_set:
  print(item) 

# Join Two Sets - elimine duplicates
my_set3 = my_set1.union(my_set2)
my_set1.update(my_set2) # insert the items in my_set2 into my_set1

# Join Two Sets - Keep ONLY the Duplicates
my_set1.intersection_update(my_set2)
my_set3 = my_set1.intersection(my_set2) # Return a set that contains the items that exist in both set

# Join Two Sets - Keep All, But NOT the Duplicates
my_set3 = my_set1.symmetric_difference(my_set2) # return a new set, that contains only the elements that are NOT present in both sets.

# Other methods
my_set = my_set.difference(my_set2)
answ = my_set.issubset(my_set2)
answ = my_set.issuperset(my_set2)
my_set = set(my_list)
~~~
