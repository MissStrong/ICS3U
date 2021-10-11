# [Link to video.](https://www.youtube.com/watch?v=qEMR2iwa8u4&list=PLVD25niNi0Bm4sxSLHOMjqB7ZTPb7Bjxf&index=8)

### Lambda Functions

So far we've made custom functions using `def`.

```python
def is_an_odd_square(num):
  """Determines whether a number is an odd square number."""
  return 0 <= num and num ** 0.5 % 2 == 1
```
Another way to make custom functions is to use `lambda`. These functions are called **lambda functions**. 

There are a few key differences between a normal function and a lambda function:
* Lambda functions do not have a name.
* Lambda functions must have a return value.
* Lambda functions don't use docstrings.
* Lambda functions are meant to be used only once.
* Lambda functions are usually one line long.
* Lambda functions cannot have multiple steps (e.g. no conditionals or loops).

Here is an example of the same function above, but written as a lambda function.

```python
lambda num: 0 <= num and num ** 0.5 % 2 == 1
```

Lambda functions are often used with `filter()` and `map()`.

```python
numbers = [1, 3, 7, 9, 16, 24, 25, 28, 49, 101]

numbers = list(filter(lambda n: 0 <= n and n ** 0.5 % 2 == 1, numbers))

print(numbers)  # prints [1, 9, 25, 49]
```

```python
strings = ["a", "bc", "de", "fgh"]

strings = list(map(lambda s: s * 3, strings))

print(strings)  # prints ["aaa", "bcbcbc", "dedede", "fghfghfgh"]
```
