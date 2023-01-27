## Note – Eval and Exec

### Eval

Python has a built-in function named `eval()` that takes a string and treats it as a math expression.

```python
print(eval("14 + 8"))   # prints 22
print(eval("1 * 9"))   # prints 9

```

The `eval()` function can be useful when an expression you want to evaluate is stored as as a string, such as when you are getting the expression from user input or from a textfile.

```python
exp = input("Enter a math expression: ")
print("The answer is", eval(exp))

```

The `eval()` function also works for parsing lists and dictionaries. For example, if the user enters `"[1, 2, 3, 4]"`, it will get stored as the list `[1, 2, 3, 4]`.

```python
a_list = eval(input("Enter a list: "))

print("Your list has", len(a_list), "items.")
```


### Exec

Python has a built-in function named `exec()` that takes a string and treats it as Python code.

```python
x = 3
exec("print(23 + x)")   # prints 26
exec("x = x + 1")  
exec("print(23 + x)")   # prints 27

```
In many situations, a program that uses `exec()` can be rewritten so that it doesn't use `exec()`, although there are some situations in which `exec()` is beneficial to use.

For example, `exec()` is useful when you are checking whether a string contains a valid piece of code.

```python
command = input("Enter some code:" )

try:
  exec(command)
except:
  print("That is not valid code")
```

In general, both `eval()` and `exec()` should be used sparingly since there are many ways in which they can go wrong and they often make code more difficult to read. 
