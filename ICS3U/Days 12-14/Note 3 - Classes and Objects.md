## Classes and Objects

### Classes 

In order to understand what an **object** is, it's first necessary to know what a **class** is. Classes are used to define the properties and functions for non-primitive data types. For example, there is a built-in class called `str` that has the defintions for `count()`, `lower()`, `join()` and other functions used with strings. We can see all the built-in properties and functions of a class using the `dir()` function. For example, `print(dir(str))` prints the full list of the publicly accessible properties and functions defined within the `str` class.

Functions that are defined inside of a class are called **methods**. Variables that are defined inside of a class are called **fields**.

### Objects

An **object** is an instance of class.  Whenever we create a string, a list, a dictionary, or any data type (including custom ones), we are creating an object.

```python
my_list = [1, 2, 3] # The variable my_list stores the object [1, 2, 3]
my_string = "123" # The variable my_string stores the object "123"
```

All objects are stored in a particular location in memory and the variable name simply points to this location. To see the address in hexadecimal, we can use `hex(id())`.

```python
my_list = [1, 2, 3] 
my_string = "123"

print(hex(id(my_list))) # Prints the address of [1, 2, 3] in hexadecimal
print(hex(id(my_sting)))  # Prints the address of 123" in hexadecimal
```

### Constructors

Every class has a method called a **constructor,** which is used to create a objects. The constructor shares the same name as the class.

To create an empty list, we can use either `my_list = []` or `my_list = list()`. They both do the same thing.

To create an empty set, we cannot use `my_set = {}` since the curly braces indicate that it is a dictionary. Instead, we should use `my_set = set()`.

### "Primitive" Data Types

Although Python is considered to have four primitive data types: `int`, `float`, `bool`, and `str` , these data types are actually defined by classes, which is not how primitives behave in most other programming languages. When we create an integer, a floating point number, a boolean, or a string, we are actually creating objects.

Since each of these "primitive" data types are defined by a class, we can use the constructors `int()`, `float()`, `bool()`, and `str()` to create objects of these data types.

