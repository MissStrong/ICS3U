## Note: Testing

### Testing

When we test a program to check whether it works, we should consider all the possible ways it can go wrong. It's usually impossible to check whether complex programs work 100% of the time, but we can do our best by designing solid test cases.

### Base Cases

**Base cases** are the simplest cases. They often include empty string, empty lists, and the number 0. These can often go wrong because we might assume that a list has at least one item, or a string has at least one character.

```python
def highest_num(num_list):
  highest_num_so_far = num_list[0]
  for num in num_list:
    if num > highest_num_so_far:
      highest_num_so_far = num
  return num
```

The problem with the function above is that it ignores the possibility that the list of number is empty. The function will throw an exception on the second line of the function if we call `highest_num([])`. We often need to write a conditional at the beginning of a function to handle these kinds of cases.


### Edge Cases

**Edge cases** (a.k.a. **Corner cases**) refer to cases involving extreme ends of a range of numbers. For example, if we are doing something with all the numbers between 1 and 100, the edge cases will include 1 and 100.

```python
def print_1_to_100():
  for i in range(1, 100):
    print i
```

This problem with this function is that `range(1, 100)` is an list of all the numbers between 1 and 99, not 1 and 100. 

These mistakes can also happen when we mix up `<` and `<=`.

```python
def is_between_0_and_10(n):
  return(0 < n and n < 10)
```

Depending on whether we wanted to include the numbers 0 and 10, this program may not do what we want it to. If we want to include 0 and 10, we would want to change `<` to `<=` (which is equivalent to ≤).

### Blackbox and Whitebox Testing

**Blackbox Testing** refers to testing a program without looking at the code. We just look at what it's supposed to do and design tests around that.

**Whitebox Testing** refers to testing a program based on how it was implemented. We consider the design of the algorithm and design tests that we think may go wrong based on the algorithm.

Both blackbox testing and whitebox testing can be useful for both manual and automated tests.