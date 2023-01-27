## Lesson: Sets

A **set** is a non-ordered collection of unique items.

A set cannot contain duplicate items, unlike a list. If you add an item to a set that is already in the set, it doesn't change the set.

A set does not have indices, unlike a list. For example, you cannot get the "first item" in a set, since there is no order to the items.

A set uses curly braces ```{}``` as delimiters, like a dictionary.

 To intialize a set with particular items, you can write the items inside curly braces.

```python
numbers = {1, 4, 7, 12, 19}
```

If you want to initialize an empty set, you need to use `set()`.

```
numbers = set()
```

If we try to initialize an empty set using `numbers = {}`, it won't work as intended because the program will treat it like a dictionary.

To add items to a set, we can use `.add()`. To remove items from a set, we can use `.remove()`.

```python
numbers = {1, 4, 7, 12, 19}

numbers.add(5)  # adds 5 to the set
numbers.add(7)  # doesn't do anything since 7 is alredy in the set
numbers.remove(12)  # removes 12 from the set

print(numbers)  # prints {1, 4, 5, 7, 19} (the order could be different)
```

Since the items in a set aren't in any particular order,  the items might not get printed in the same order as were added in. The order in which the items are outputted depends on where they are stored in memory, which could be different every time the program is run.

Sets can be iterated through using a *for* loop.

```python
numbers = {1, 4, 7, 12, 19}
sum = 0

for n in numbers:
  sum += n  # adds together all the numbers in the set
```

We can check whether a set contains a particular item using `in`.

```python
numbers = {1, 4, 7, 12, 19}

print(4 in numbers)  # prints True
print(5 in numbers)  # prints False
```

