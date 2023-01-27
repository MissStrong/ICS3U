## Note – Eval and Exec

### Eval

Python has a built-in function named `eval()` that takes a string and treats it as a math expression.

```
print(eval("14 + 8"))   # prints 22
print(eval("1 * 9"))   # prints 9

```

The `eval()` function can be useful when an expression you want to evaluate is stored as as a string, such as when you are getting the expression from user input or from a textfile.

```
exp = input("Enter a math expression: ")
print("The answer is", eval(exp))

``

### Exec

Python has a built-in function named `exec()` that takes a string and treats it as Python code.

```
x = 3
exec("print(23 + x)")   # prints 26
exec("x = x + 1")  
exec("print(23 + x)")   # prints 27

```

Just like with `eval()`, the `exec()` function can be useful when an expression you want to evaluate is stored as as a string, such as when you are getting the expression from user input or from a textfile.

```
num_list = input("Enter a list of numbers: ")
exec("length = len(" + num_list + ")")
print("Your list has", length, "numbers.")

``
In thie example above, even though there is a red squiggly line under the print statement, it is not causing any errors since `length` gets defined when `exec()` is called.


In general, both `eval()` and `exec()` should be used sparingly since there are many ways in which they can go wrong and they often make code more difficult to read. 
