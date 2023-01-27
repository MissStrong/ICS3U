## Lesson: Scope

### Scope

Scope refers to the places where a variable can be accessed. Not all variables can be accessed from anywhere inside of your program.

### Global Variables

**Global variables** can be accessed from anywhere within a program. They are initialized outside of a structure such as outside a function or a loop.

```python
int days_left = 81

def update_days_left(n):
  days_left = n
```

Since the variable `days_left` is not within a structure, we can access and modify it from within any function.

### Local Variables

Local variables cannot be accessed from anywhere within program. They are initialized inside a structure, such as a function or loop, and can only be accessed from within that structure. 

```python
def foo():
  my_list = [1, 2, 3]
  return my_list
  
print(my_list)  # this does not work; the program claims that my_list is not defined
```

Since `my_list` is defined within the function `foo()`, it can only be accessed within that function. We can say that the **scope** of `my_list` is the function `foo()`. 

N.B.: `foo()` is a common name for a function that doesn't accomplish anything meaningful.

