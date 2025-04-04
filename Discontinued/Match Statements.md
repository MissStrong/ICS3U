### Conditionals

We learned about the `if`, `elif`, and `else` statements earlier.

```python
num = int(input("Enter a triangle or square number between 0 and 10: "))
 
if num == 0 or num == 1:
    print("That's a triangle and a square!")
elif num == 3 or num == 6 or num == 10:
    print("That's a triangle!")
elif num == 4 or num == 9:
    print("That's a square!")
elif 0 <= num <= 10:
    print("That's not a triangle or a square!")
else:
    print("That's not between 0 and 10!")
```

There's another type of conditional statement called a **match** statement or **match case** statement.

Here is what the same program as the one above would look like if it used `match` and `case` instead.

```python
num = int(input("Enter a triangle or square number between 0 and 10: "))

match num:
    case 0 | 1:
        print("That's a triangle and a square!")
    case 3 | 6 | 10:
        print("That's a triangle!")
    case 4 | 9:
        print("That's a square!")
    case num if 0 <= num <= 10:
        print("That's not a triangle or a square!")
    case _:
        print("That's not between 0 and 10!")
```

### Match Case

The general structure goes like this:

```python
match variable:
    case pattern:
        do something here
```

If `pattern` is just a single value, such as a number or string, the condition is met if `variable` is equal to that value.

If `pattern` are values separated by pipes `|`, the condition is met if `variable` is equal to any of the values. The pipe means "or".

If `pattern` is `variable if boolean_expression`, the condition is met if `boolean_expression` is `True`. 

If  `pattern` is just an underscore `_`, the condition is met no matter what. This is often used as the last case to catch anything that was previously missed, similar to the way `else` is used.
