Lesson: Documentation
-------

### Why Write Comments?

Documentation refers to writing comments alongside your code. They serve as explanations for what your code does and why it works.

When you are working as a member of a team, good documentation is cricital for your team members understanding your code and you understanding your team members' code.

When you are working on a large project, good documentation is cricital for understanding and remembering what particular blocks of code do in case you don't remember writing it.

###What is a Good Comment?

Good comments don't point out obvious things, like this:

![](../../Images/Stop_Sign.jpg)

![](../../Images/Cat.jpg)



The images above are similar to the code below.

```python
for i in range(10): # this is a for loop
  print(i) # prints the number
```



Good comments help make your code clear when it's not obvious what is going on. They can help explain your thinking so that someone reading it can understand how it works. Here is an example:

```python
def is_a_square_number(n):
  if (n < 0):
    return False # negative numbers can't be squares
  sqrt = (int)Math.sqrt(n) # takes the square root of n and rounds it down to the nearest whole number
  return sqrt*sqrt == n # if the rounded square root squared is n, n must be a square
```

Without the line comments in this case, the reader may not understand why this algorithm works.

