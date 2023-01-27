Note – Aliasing
-------

### Storing Variables

Programs store variables in **memory**. Each location in memory has an **address**, typically represented in hexadecimal.

To find the address of a variable in Python, we can use `id()`. This returns the number as a base 10 value, but we can convert it to hexadecimal using `hex()`.

```python
x = 3
print(hex(id(x))  # prints the address where 3 is stored (e.g. 0x7fdc369ef720)
```

### Mutable Versus Immutable Variables

The four primitive data types in Python: `int`, `float`, `bool`, and `str`. These are **immutable** data types, meaning these variables *move addresses* when they are given a new value.

```python
x = 3
print(hex(id(x)))  # prints the address where 3 is stored (e.g. 0x7f10fda70720)

x = x + 1
print(hex(id(x)))  # prints the address where 4 is stored (e.g. 0x7f10fda70740)
```

Notice that the address of `x` changed when its value was reassigned. This behaviour happens with all primitive data types in Python.

Non-primitive data types (a.k.a. composite data types) are all other data types such as `list`, `dict`, and `set`. Most non-primitive data types are **mutable** data types, meaning these variables *don't move addresses* when they are given a new value. Exceptions include `tuple`, `decimal`, and `range`.

```python
my_list = [1, 2]
print(hex(id(my_list))) # prints the address where [1, 2] is stored (e.g. 0x7efdf846d600)

my_list.append(3)
print(hex(id(my_list))) # prints the address where [1, 2, 3] is stored (e.g. 0x7efdf846d600)
```

Notice that the address of `my_list` did not change when the list was updated. This behaviour happens with all non-primitive data types in Python.

### Aliasing

**Aliasing** occurs when when two variable names point to the same location in memory. In other words, they can be used interchangeably. This can be an issue with non-primitive data types.

```python
list_1 = [1, 2]
list_2 = list_1
list_1.append(3)

print(list_1)  # prints [1, 2, 3]
print(list_2)  # also prints [1, 2, 3], not [1, 2]
```

In this example `list_1` and `list_2` are **aliases** of each other. Whenever we update `list_1`, we also update `list_2`, and vice versa. We can confirm this by checking their locations in memory (they will be the same address).

If we don't want this to happen, we can call the `list()` function to make a new list in at a new location in memory.

```python
list_1 = [1, 2]
list_2 = list(list_1)  # makes a new list at a new location in memory
list_1.append(3)

print(list_1) # prints [1, 2, 3]
print(list_2) # prints [1, 2], not [1, 2, 3]
```

