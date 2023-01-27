## Note – Generator Expressions

**Generator expressions** in Python are expressions that are generated using syntax resembling that of list comprehensions. They are especially useful to use with `max()`, `min()`, `sum()`, `prod()`, and other similar functions that involve iteration.

Consider a program that adds the integers from 0 to 100. 

We could accomplish this by calling `sum()` on a list comprehension:

```python
sum([n for n in range(101)])
```

We could also accomplish this by using a generator expression with `sum()`:

```python
sum(n for n in range(101))
```

The difference is that the first approach creates a list and sums up all the items in the list, whereas the second approach generates the expression `0 + 1 + 2 + ... + 99 + 100`.

We can also use conditional statements in generator expressions. For example, this generates an expression for the sum of all the odd numbers from 1 to 100:

```python
sum(n for n in range(101) if n % 2 == 1)
```

Consider a program that finds the largest value in a dictionary, `d`.

We could accomplish this by calling the following:

```python
max(d.values())
```

...but it is more efficient (in terms of both memory usage and runtime) to use a generator expression: 

```python
max(d[key] for key in d)
```
