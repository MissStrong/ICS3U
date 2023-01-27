## Lesson: Lists and Tuples

### Lists

A list is a data structure that stores an ordered set of items.

In Python, we can initialize a list by putting the items in square brackets. For example:

```python
groceries = ["bread", "milk", "potato"]
```

 In many programming languages, a list is allowed to store only one data type. However, in Python, a list can store different data types. 

```python
stuff = [2, "potato", True, 7.2, "c"]
```

  

### Accessing Items in a List

Each item in a list is assigned an **index**. The index tells us which position the item is at. The first position is index 0, the second position is index 1, the third position is index 2, and so on.

**In computer science, we often start counting at 0 instead of 1**. Being "off by one" is a common phenomenon when programming.

When we want to access an item in a list, we can do that by calling the name of the list and putting the item's index in square brackets. For example:

```python
groceries = ["bread", "milk", "potato"]

print(groceries[1])  # prints "milk"
```



If we want to access the very last item in the list we can use `[-1]`. For example:

```python
groceries = ["bread", "milk", "potato"]

print(groceries[-1])  # prints "potato"
```



If we want to check the index of an item, we can use the `index()` function. For example:

```python
groceries = ["bread", "milk", "potato"]

print(groceries.index("milk"))  # prints 1
```

 

### Adding or Removing Items to/from a List

We can add items to a list or remove items from a list at any point after we initialize it. We can add items using the `append()` function and we can remove them using the `remove()` function.

```python
groceries = ["bread", "milk", "potato"]

groceries.append("banana")

print(groceries)  # prints ["bread", "milk", "potato", "banana"]

groceries.remove("milk")

print(groceries)  # prints ["bread", "potato", "banana"]
```

 

If we want to add an item to a particular index, we can use `insert()`.

```python
groceries = ["bread", "milk", "potato"]

groceries.insert(0, "cereal")  # this puts "cereal" at index 0 and pushes the other items over one spot

print(groceries)  # prints ["milk", "potato"]
```



If we want to remove an item at a particular index, we can use `pop()`.

```python
groceries = ["bread", "milk", "potato"]

groceries.pop(0)  # this removes the item at index 0, which is "bread"

print(groceries)  # prints ["milk", "potato"]
```

 

### Combining Lists

We can combine two or more lists into one long list by using `extend()`. For example:

```python
groceries = ["bread", "milk", "potato"]
more_groceries = ["banana", "cereal"]

groceries.extend(more_groceries)

print(groceries)  # prints ["bread", "milk", "potato", "banana", "cereal"]
```

 

### Searching Through Lists

We can use a *for* loop to iterate through a list by looking at each item one by one.

```python
groceries = ["bread", "milk", "potato"]
  
for item in groceries {
  print(item)  # prints each item in the list
}
```

If we wanted to print the indices (plural of index) too, we could use the `range()` function. We can use the `len()` function to get the **len**gth of a list.

```python
groceries = ["bread", "milk", "potato"]
  
for index in range(len(groceries)) {
  print(index, groceries[index])  # prints each index in the list and its corresponding item
}
```

 

### Sorting Lists

It's sometimes convenient when a list is in alphanumeric order. We can make a list sorted by using the `sort()` function.

```python
groceries = ["bread", "milk", "potato", "banana", "cereal"]
 
groceries.sort()

print(groceries)  # prints ["banana", "bread", "cereal", milk", "potato"]
```



We can also reverse the items in a list using `reverse()`. If we want the items to be in reverse alphanumeric order, we can use `sort()` followed by `reverse()`.

```python
groceries = ["bread", "milk", "potato", "banana", "cereal"]
 
groceries.sort().reverse()

print(groceries)  # prints ["potato", "milk", "cereal", "bread", "banana"]
```



N.B.: When you sort a list, the characters are sorted based on the order of their individual [ASCII](http://www.asciitable.com) characters. In the ASCII chart, all upper case letters come before all lower case letters, so your items may not be in alphabetical order if some begin with a lower case letter and others begin with an upper case letter.

  

### Tuples

A tuple (pronounced "too-pull") is also a data structure that stores an ordered set of items, but the key difference is that they cannot be changed once they are initiated. They also use round brackets instead of square brackets.

```python
coordinate = (4, -5)
```

We can use square brackets to get an item of a tuple at a particular index.

```python
coordinate = (4, -5)

print(coordinate[0])  # prints 4
print(coordinate[1])  # prints -5
```

We can also get the index of a particular item in a tuple using `index()`.

```python
coordinate = (4, -5)

print(coordinate.index(4))  # prints 0
print(coordinate.index(-5))  # prints 1
print(coordinate.index(7))  # gives an error
```

That's about it for tuples. There aren't nearly as many built-in functions for tuples as there are for lists.

