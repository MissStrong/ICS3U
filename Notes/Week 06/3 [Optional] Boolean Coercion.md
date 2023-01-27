## Note - Boolean Coercion

### Type Conversion

A **type conversion** occurs when a value is changed into a value of a different but compatible type. 

There are two categories of type conversion: **explicit conversion** and **implicit conversion**.

Explicit conversion is also known as **casting**. In Python, you can cast variables from one data type to another using functions such as `int()`, `str()`, `bool`, and `list()`.

```python
num = int("6") # this changes the string "6" into the integer 6
total = str(6) # this changes the integer 6 into the string "6"
```

Implicit conversion is also known as **coercion**. In Python, coercion can happen when you perform an operation or function on two values that belong to different data types when they should be the same data type.

```python
total = 4 + 5.3 # 4 is converted to 4.0 before the two numbers are added
```

This doesn't work in every situation though.

```python
result = "The answer is " + 6 # this raises an error
```

Coercion can also happen on operations that take one value, such as the boolean operator `not`.

### Boolean Casting

All values that belong to primitive data types can be converted into a boolean value.

The golden question is, which values get converted to `True` and which ones get converted to `False`?

We can check that out by using casting using `bool()`.

```python
print(bool(0)) # prints False
print(bool(1)) # prints True
print(bool(-1)) # Prints True
print(bool(0.0)) # Prints False
print(bool(-3.5)) # Prints True
print(bool(6)) # Prints True
```

For numeric data types, `0` and `0.0` convert to `False` and all other values convert to `True`.

```python
print(bool("")) # prints False
print(bool("hello")) # prints True
print(bool("world")) # Prints True
print(bool("True")) # Prints True
print(bool("False")) # Prints True
```

For strings, the empty string `""` converts to `False` and all other values convert to `True` (even the string `"False"`).

Just as a sanity check:

```python
print(bool(True)) # prints True
print(bool(False)) # prints False
```

Good. No surprises here.

We can also cast certain collection types such as lists, tuples, dictionaries, and sets to booleans.

```python
print(bool([])) # prints False
print(bool([1])) # prints True
print(bool(tuple())) # prints False
print(bool((1))) # prints True
print(bool({})) # Prints False
print(bool({1:1})) # Prints True
print(bool(set())) # Prints False
print(bool({1})) # Prints True
```

For these data types, they convert to `False` if they are empty and `True` otherwise.

### Boolean Coercion

Knowing that we can convert between common data types and booleans, we can write some interesting conditional expressions.

One common way of checking whether a string or list is empty is to check that its length is zero:

```python
if len(string) == 0:
  print("That's an empty string.")
```

However, we now know when that a string gets converted to a boolean value, it becomes `False` if and only if the string is empty. That let's us do this:

```python
if not string:
  print("That's an empty string.")
```

This may look unusual at first glance, but this is a common "trick" used in Python programs.

Suppose we are checking whether a number is a multiple of 5. Here's a straight-forward way to do this:

```python
if num % 5 == 0:
  print("That's a multiple of 5.")
```

However, we now know that when a number gets converted to a boolean value, it becomes `False` if and only if the number is equivalent to zero. That let's us do this:

```python
if not num % 5: # if num is a multiple of 5, we get the boolean expression `not 0`, which is `True`
  print("That's a multiple of 5.")
```

This is not common practice in every programming langauge. However, if you continue to learn Python after this course, chances are that you'll encounter boolean expressions like this in other people's code.
