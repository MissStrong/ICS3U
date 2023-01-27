## Note – Functions

### Built-in Functions

A function takes an input and performs a sequence of steps to give an output. They have a name and are followed by a pair of parentheses. When a function is **called**, the inputs are placed inside the parentheses.

So far, you've seen the following functions:

* `print()`
* `input()`

These are all examples of **built-in** functions, since they are built into Python. You can find the full list of built-in functions here: https://docs.python.org/3/library/functions.html.

You've also seen the following functions used to convert data types:

* `str()`
* `int()`
* `float()`

These are called **constructors**.  They create new **objects**. (We'll get to what that means in a later lesson.) 

### Custom Functions

You can create your own functions when there aren't any built-in functions that suit your needs.

Here is an example of a custom function:

````python
def slope(x1, x2, y1, y2): 
  return (y2 - y1) / (x2 - x1)
````

The keyword `def` indicates that we are **defining** a function. The function name here is `slope` and it takes four **parameters** (i.e. inputs), *x1*, *x2*, *y1*, and *y2*. 

The keyword `return` indicates what value the function returns. In this case, the function returns the slope of a line given two coordinates: (x1, y1) and (x2, y2). The tab space before the return statement is necessary since it is a part of the body of the function.

We can call this function within the same program to find the slope a line.

````python
print(slope(2, 3, 0, 9)) # prints -3
````

**Parameters** are the variable names used in a function. **Arguments** are the values of the parameters you use when you are calling a function. In the example at the bottom of the previous table, the parameters are *x1*, *x2*, *y1*, and *y2* and the arguments are 2, 3, 0, and 9.

### Functions in Math versus Functions in Computer Science

**If you haven't taken the Grade 11 math course *Functions* (MCR3U) or *Functions and Applications* (MCF3M), you can skip this section.**

In math, a relation is a relationship involving one or more variables. A function is a relation in which each independent variable value has only one corresponding dependent variable value.

For example, *f(x) = x<sup>2</sup> + 4* is a function, in which:

* *f* is the name of the function
* *f(x)* is the dependent variable
* *x* is the independent variable
* *x<sup>2</sup> + 4* is how to compute the value of the dependent variable given the value for the independent variable.

Functions can have more than one independent variable. For example, *f(x, y, z) = 4x + 2y - 1/z* is also a function.

Functions in computer science may look different to functions in math, but they are fundamentally similar.


| .                                          | Math Example                                         | Python Example                                               |
| ------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------------ |
| Function                                   | f(x, y, z) = 4x + 2y - 1/z                           | `def foo(x, y, z): `<br></br>&nbsp;&nbsp;&nbsp;&nbsp;`return 4*x + 2*y - 1/z;` |
| Function name                              | *f*                                                  | `foo`                                                        |
| Parameters (Independent Variables)         | *x*, *y*, *z*                                        | `x`, `y`, `z`                                                |
| Return Value (Value of Dependent Variable) | *4x + 2y - 1/z*                                      | `4*x + 2*y - 1/z`                                            |
| Example                                    | *f(7, -3, 1) = 4(7) + 2(-3) - 1/1 = 28 - 6 - 1 = 21* | `a = foo(7, -3, 1)`<br/></br>`// the value of a is initialized to 21` |

In math, *f*, *g*, and *h* are generic names for functions. In computer science, `foo`, `bar`, and `baz` are generic names for functions. You can also come up with your own dummy names for functions that aren't supposed to be meaningful. I'm quite fond of `bloop`.


