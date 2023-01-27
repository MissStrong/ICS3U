Lesson: Dictionaries
-------

Dictionaries are used to store and quickly look up "pairs" of information.

For example, we could store a grocery list like this.

```python
grocery_list = {"banana": 2, "apple": 5, "orange": 3, "strawberry": 12}
```

Each pair has a **key** and a **value**. For example, the key `banana` has the value 2, which tells us that the grocery list says to buy two bananas. 

The keys must be unique and can be almost any data type, except lists.

Each key and its associated value are separated by a colon.

Unlike lists, dictionaries have curly braces ```{}``` as delimiters instead of square brackets ```[]```.

Like lists, dictionaries can be iterated through using a *for* loop.

```python
grocery_list = {"banana": 2, "apple": 5, "orange": 3, "strawberry": 12}

for item in grocery_list:
  print(item)  # prints each fruit one at a time on separate lines
  
for item in grocery_list:
  print(grocery_list[item])  # prints each number one at a time on separate lines
```

Notice that the keys might not be printed in the order you would expect. This is because dictionaries do not have indices like lists do. The order in which the keys are outputted depends on where they are stored in memory, which could be different every time the program is run.

We can add information to dictionaries like this:

```python
grocery_list = {"banana": 2, "apple": 5, "orange": 3, "strawberry": 12}

grocery_list["kiwi"] = 3  # adds "kiwi":3 to the dictionary
grocery_list["grapefruit"] = 1  # adds "grapefruit":1 to the dictionary

print(grocery_list)  # prints {"kiwi": 3, "apple": 5, "orange": 3, "strawberry": 12, "banana": 2, "grapefruit": 1}
```

We look up information in dictionaries like this:

```python
grocery_list = {"banana": 2, "apple": 5, "orange": 3, "strawberry": 12}

print(grocery_list["apple"])  # prints the value of the key apple, 5
print(grocery_list["strawberry"])  # prints the value of the key strawberry, 12
```

If we try to print the value of a key that does not exist, we will get a ```KeyError```.

Here are some other things we can do with dictionaries:


```python
grocery_list = {"banana": 2, "apple": 5, "orange": 3, "strawberry": 12}

print (len(grocery_list))  # prints the length of grocery_list, which is the number of key:value pairs
print ("banana" in grocery_list)  # prints true, since "banana" is a key in grocery_list
print ("potato" in grocery_list)  # prints false, since "potato" is not a key in grocery_list
del grocery_list["orange"]  # removes "orange":3 from grocery_list
print (grocery_list)  # prints the updated grocery list with banana and potato but not orange

```

