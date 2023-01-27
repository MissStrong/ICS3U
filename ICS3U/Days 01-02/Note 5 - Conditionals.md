## Note – Conditionals

### Boolean Expressions

A **Boolean expression** is an expression that evaluates to either `True` or `False`. The word "Boolean" is named after George Boole, a logician from the 1800s.

You can create Boolean expressions using **comparison operators**, **equality operators**, and **Boolean operators**.

Here are all the operators you can use in Python to create Boolean expressions.  The convention to write the names of Boolean operators in all capital letters. That's why NOT, AND, OR, and XOR are in all capital letters.

| Operator Name | Operator Symbol | Category | Example | Explanation |
| --- | --- | --- | --- | --- |
| Less Than | `<` | Comparison Operator | `3 < 5 # True` | 3 is less than 5, so the expression is `True`. |
| Greater Than | `>` | Comparison Operator | `3 > 5 # False` | 3 is not greater than 5, so the expression is `False`. |
| Less Than or Equal To | `<=` | Comparison Operator | `3 <= 5 # True`	| 3 is less than or equal to 5, so the expression is `True`.<br /> `<=` is supposed to look like the ≤ symbol. |
| Greater Than or Equal To | `>=` | Comparison Operator | `3 >= 5 # False`	| 3 is neither greater than nor equal to 5, so the expression is false.<br />`>=` is supposed to look like the ≥ symbol. |
| Equals | `==` | Equality Operator | `3 == 5 # False`	| 3 is not equal to 5, so the expression is false.<br/></br>Mixing up `=` and `==` is a notorious error in computer science. This applies to many programming languages, not just Python. |
| Not Equals | `!=` | Equality Operator | `3 != 5 # True`	| 3 is not equal to 5, so the expression is `True`.<br />`!=` is supposed to look like the ≠ symbol.  |
| NOT | `not` | Boolean Operator | `not (3 < 5) # False`	| The statement in the parentheses is `True`, so the expression is the negation of that, which is `False`. |
| AND | `and` | Boolean Operator | `(3 < 5) and (3 > 5) # False`	| At least one of those two statements is `False`, so the expression is `False`. |
| OR | `or` | Boolean Operator | `(3 < 5) or (3 > 5) # True`	| At least one of those two statements is `True`, so the expression is `True`. |

### Conditional Statements

Boolean expressions are often used to check conditions. For example, you may want different blocks of code to run depending on the values of specific variables at specific times.

A conditional statements only run when a condition is met. We use Boolean expressions to create these conditions.

The most common type of conditional statement is called an **if statement.**

Here is an example of an *if* statement.

```python
number = int(input("Pick a number between 1 and 10: "))

if number > 10:
  print("Your number is too high!")
elif number < 1:
  print("Your number is too low!")
else:
  print("Thanks.")
```

* An `if` block runs only if the condition is `True`. 
* `elif` is short for "else if". Any `elif` blocks run only if all the previous conditions in the conditional structure are `False` (the "else" in `elif`) and the new condition is true (the "if" in else if).
* An `else` block runs only if all the previous conditions in the conditional structure are `False`.

In any conditional structure, you may have as many or as few `elif` blocks as you wish. You may have no more than one `else` block. 

If you have multiple `if` blocks followed by an `else` block, the `else` block will run if the condition in the most `if` was `False`. 

In general, if the conditions are mutually exclusive (i.e. they can't hold true at the same time), you should use `if` followed by `elif` rather than `if` followed by another `if`.


### Boolean Operators

When can are use `and` or `or` to combine short Boolean expressions to make longer ones:

```python
if mark < 0 or mark > 100:
  print("That is not a valid mark.")

```

```python
if num % 3 == 0 and num % 5 == 0:
  print("That number is a multiple of 3 and 5")

```

A common mistake is to use `or` the exact same way we use it in English:

```python
if answer == "yes" or "no":  # This does not work as expected; it seems to always be True
  print(answer)
else:
  print("Your answer must be yes or no").
 ```
 
The mistake here is that `or` combines the Boolean expressions `answer == "yes"` and `"no"`. All non-empty strings in Python become `True` when they are converted into a Boolean value. Here is the correction:
 
 
```python
if answer == "yes" or answer == "no":  # This works
  print(answer)
else:
  print("Your answer must be yes or no").
 ```
