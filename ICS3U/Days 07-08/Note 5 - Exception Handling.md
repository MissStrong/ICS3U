## Note: Exception Handling

### Exceptions/Errors

Whenever you run a program that has errors, you may have noticed that repl.it attempts to tells you what kind of error it is. 

For example, if you try to divide by zero, you get a message in the console saying that there was an error called `ZeroDivisionError`.

![](../../Images/Zero_Division_Error.png)

An **exception** is a problem that occurs while a program is running. When an exception occurs in Python, it is **raised**. When this happens and your program doesn't handle it, the program terminates abruptly. 


In order to avoid a program from terminating abruptly, you should consider possible exceptions that could occur in your program.

Here is an example of a method that handles a division by zero error.

```python
def divide_three_ints(a, b, c):
  try:
    return a/b/c
  except:
    if (b == 0):
      print("Error. B cannot be zero.")
    if (c == 0):
      print("Error. C cannot be zero.")
```

The content in the `try` block is run first. It tries to run the lines in the block; if an exception occurs, the exception is "thrown" and the rest of the block does not run. 

The content in the `except` block runs only when an exception such as `ZeroDivisionError` has been thrown. It "catches" the exception and prevents the program from abruptly terminating and giving you a red error message.

###Type Checking

You can check the type of a variable using `type()`. This can be useful for ensuring that a variable is a particular data type.

```python
print(type(3))  # prints "int"
print(type(3.0))  # prints "float"
print(type("hi"))  # prints "str"
print(type(True))  # prints "bool"
print(type([]))  # prints "list"
print(type({}))  # prints "dict"
```

### Assert

You can assert that a condition is true by using `assert()`. Whenever an `assert` statement is false, the program terminates abruptly.

```python
user_input = input("Enter an integer:")

assert(type(user_input) == int)
```

### Raising Exceptions

You can raise an exception at any time using the keyword `raise`.

```python
user_input = input("Enter a positive integer: ")

if type(user_input) !=  int:
  raise Exception("Your input was not an integer!")
elif user_input < 0:
  raise Exception("Your input was not a positive number!")
```

