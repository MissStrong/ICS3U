## Note – List Comprehensions

### The range() Function

So far we've seen `range()` used to generate a list of numbers from 0 to some value. For example `range(10)` generates the first 10 integers starting at 0, which are `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`.

When there are *two* parameters, `range()` can generate a list of numbers from a start value up to an end value. For example, `range(5, 15)` generates the first 10 integers starting at 5, which are `5, 6, 7, 8, 9 , 10, 11, 12, 13, 14`.

When there are *three* parameters, `range()` can generate a list of numbers from a start value to an end value, increasing or decreasing by a specific increment.

For example:

* `range(0, 10, 2)` generates the numbers `0, 2, 4, 6, 8`.
* `range(10, 0, -1)` generates the numbers `10, 9, 8, 7, 6, 5, 4, 3, 2, 1`.
* `range(10, 0, -2)` generates the numbers `10, 8, 6, 4, 2`.

 

### List Comprehension

We can use `range()` to generate numbers that follow a linear pattern, but what if we want to generate numbers that follow a different pattern?

With **list comprehension**, we can generate lists that follow almost any pattern. Here is the syntax:

```python
list_name = [expression for item in a_list]
```

`list_name` is the  name of the list you are generating, `expression` is the expression for each value in the list based on each `item` in `a_list`. The variable `a_list` (pronounced as "a list") is used instead of `list` since `list` is a keyword in Python.

Suppose we want to generate a list of all the square numbers from 0<sup>2</sup> to 9<sup>2</sup>. One way we could do that is using list comprehension:

```python
square_numbers = [n * n for n in range(10)]
```

Here,  `n` represents each value in `range(10)`, which is the list `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`. Each value `n` becomes `n * n`, giving the new list `[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]`.

 This example is equivalent to this:

```python
a_list = []
for n in range(10):
  a_list.append(n * n)
```

We can do list comprehension with strings too. Here is the syntax:

```python
list_name = [expression for character in string]
```

For example, we can generate a list of all the characters in a string converted to upper case like this:

```python
characters_list = [c.upper() for c in "Hello"]  # generates ['H', 'E', 'L', 'L', 'O']
```

which is equivalent to this:

```python
characters_list = []
for c in "Hello":
  characters_list.append(c.upper())
```

We can also use conditionals in list comprehensions.

For example, we can generate a list of all the vowels in a string like this:

```python
vowels_list = [c for c in "Hello" if c in "aeiou"]  # generates ['e', 'o']
```

We can even use an if-elif-else structure, like this:

```python
vowels_list = [c for c in "Hello" if c in "aeiou" else '']  # generates ['', e', '', '', 'o']
```



### Set Comprehension

The syntax for a **set comprehension** is identical to that of a list comprehension, except we use curly braces instead of square brackets as the delimiters.

```python
square_numbers = {n * n for n in range(5)}  # generates {0, 1, 4, 9, 16}
```

 ```python
characters_set = {c for c in "Hello"}  # generates {'H', 'E', 'L','O'}
 ```



### Dictionary Comprehension

The syntax for a **dictionary comprehension** is identical to that of a set comprehension, except we write expressions for both the key and the value.

```python
square_numbers = {n: n * n for n in range(5)}  # generates {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

