# [Link to video.](https://www.youtube.com/watch?v=msXrOlpZkCc&list=PLVD25niNi0Bkrelmc-dxdpMzITt5YTBsc&index=9)

### exec()

Python has a built-in function named `exec()` that takes a string and treats it as Python code.

```python
x = 3
exec("print(23 + x)")   # prints 26
exec("x = x + 1")  
exec("print(23 + x)")   # prints 27
```

Just like with `eval()`, the `exec()` function can be useful when an expression you want to evaluate is stored as as a string, such as when you are getting the expression from user input or from a textfile.

```python
try:
  num_list = input("Enter a list of numbers such as [1, 4, 3]: ")
  exec("length = len(" + num_list + ")")
  print(f"Your list has {length} numbers.")
except:
  # this occurs if exec() raises an error
  print("That is not a valid list of numbers.")
```

In thie example above, even though there is a red squiggly line under the print statement, it is not causing any errors since `length` gets defined when `exec()` is called.

In general, both `eval()` and `exec()` should be used sparingly since there are many ways in which they can go wrong and they often make code more difficult to read.
