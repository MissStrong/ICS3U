# [Link to video.](https://www.youtube.com/watch?v=qjRvd50v64M&list=PLVD25niNi0Bkrelmc-dxdpMzITt5YTBsc&index=8)

### eval()

Python has a built-in function named `eval()` that takes a string and treats it as a math expression.

```python
print(eval("14 + 8"))   # prints 22
print(eval("1 * 9"))   # prints 9

```

The `eval()` function can be useful when an expression we want to evaluate is stored as as a string, such as when we are getting the expression from user input or from a textfile.

```python
try:
  exp = input("Enter a math expression: ")
  print("The answer is", eval(exp))
except:
  # this occurs if eval() raises an error
  print("That's not a valid math expression.")
```

There aren't that many cases when using `eval()` is the only way of doing something, but it is a useful tool to be aware of.
