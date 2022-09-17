# [Link to video.](https://www.youtube.com/watch?v=Kk4AJiAMhPc&list=PLVD25niNi0BmSZoy7atetbgODmero31pR)

### Assertions

One way to enforce specific conditions is to use the keyword `assert`. After the keyword, we write the condition that we want to enforce. Whenever the condition is not true, an `AssertionError` is raised.

```python
num = input("Enter a positive integer:" )
assert num.isdecimal()  # raises an error if num has any non-digit characters
```

```python
def add_numbers(a, b):
  assert type(a) in [int, float]  # raises an error if a is not a number
  assert type(b) in [int, float]  # raises an error if b is not a number
  return a + b
```
