## Note – Data Types

### Definitions

A **variable** is value that can change over time. 

A **constant** is a value that cannot change over time. 

The **scope** of a variable refers to where and when variable can be used.

A **local variable** is a variable that is declared within a local scope. It may be used only within the context (e.g. a function or a loop) it was declared in. It is lost when its context is completed.

A **global variable** is a variable that is declared within a global scope. It may be used throughout the entire program.

A **data type** is the kind of data that a variable can store.

All data types are either primitive or composite. A **primitive data type** (a.k.a. a **basic data type**) represents a single piece of information. If a data type isn't primitive, it is a **composite data type**. Whether a data type is primitive or composite depends on the programming language. Here are the four primitive data types in Java. 

| Data Type | Explanation                                                  |
| --------- | ------------------------------------------------------------ |
| Integer   | Any integer. There is no upper or lower limit to how high or low it can be. |
| Float     | Any decimal number that can be represented in 32 bits using IEEE 754. |
| String    | Text.  It consists of individual characters. Strings are enclosed in single quotation marks `'` or double quotation marks `"`. |
| Boolean   | The values `True` or `False`.                                |

When you are mentioning a variable or a constant for the first time, you must **assign** a value to it.

```python
height = 10 # we have created the variable height and assigned a value of 10 to it
height = 11 # we have changed the value of height from 10 to 11

person = "Chris" # we have created the variable person and assigned a value of "Chris" to it
```
In general, you should use descriptive names for variables to help create code that is self-explanatory.

### Special Characters

In order to put any of the following special characters in a string, you need to put the **escape character** ``\`` in front of it.

| Name                  | Special Character                                            |
| --------------------- | ------------------------------------------------------------ |
| tab                   | `\t`                                                         |
| new line              | `\n`                                                         |
| backslash             | `\\`                                                         |
| single quotation mark | `\'` (You only need to use this when the string in enclosed in single quotation marks.) |
| double quotation mark | `\"` (You only need to use this when the string in enclosed in double quotation marks.) |

### Casting

A **type conversion** occurs when a value is changed into a value of a different but compatible type. 

**Casting** involves using a function to change a variable's data type. In Python, you do this by wrapping the variable in parentheses and placing either `int`or `str` in front.

```python
num = int("6") # this changes the string "6" into the integer 6
total = str(6) # this changes the integer 6 into the string "6"
```

### Naming Notations

In different programming languages, there are different rules for naming. Here are some of the common notations used.

| Notation Name    | Example                  | Explanation                                                  |
| ---------------- | ------------------------ | ------------------------------------------------------------ |
| Camel Case       | thisIsCamelCase          | Every word begins with a capital, except for the first word.<br/><br/>All other letters are lowercase. |
| Pascal Case      | ThisIsPascalCase         | Every word begins with a capital.<br/><br/>All other letters are lowercase. |
| Snake Case       | this_is_snake_case       | Every letter is lowercase.<br/><br/>Words are separated with underscores. |
| Caterpillar Case | this-is-caterpillar-case | Every letter is lowercase.<br/><br/>Words are separated with hyphens. |

In Python, the convention is to use snake case for variables and functions. (We'll get to what a function is in a later lesson.)


### Mathematical Operators

Python has the following built-in mathematical operators. You can use them to manipulate and calculate numeric values.

| Operator | Example              | New Value of `score`                                         |
| -------- | -------------------- | ------------------------------------------------------------ |
| `=`      | `score = 10`         | Assigns 10 to the value of `score`.                          |
| `+`      | `score = score + 2`  | Adds 2 to the value of `score`.                              |
| `-`      | `score = score - 5`  | Subtracts 5 from the value of `score`.                       |
| `*`      | `score = score * 2`  | Multiplies the value of `score` by 2.                        |
| `//`     | `score = score // 5` | Divides the value of `score` by 5.                           |
| `**`     | `score = score ** 3` | Raises `score` to the power of 3.                            |
| `/`      | `score = score / 5`  | Divides the value of `score` by 5 then takes the dividend.   |
| `%`      | `score = score % 5`  | Divides the value of `score` by 5 then takes the remainder.  |
| `+=`     | `score += 7`         | Adds 7 to the value of `score`.<br><br/>Essentially equivalent to `score = score + 7`. |
| `-=`     | `score -= 2`         | Subtracts 2 from the value of `score`.<br><br/>Essentially equivalent to `score = score - 2;. |
| `*=`     | `score *= 2`         | Multiplies the value of `score` by 2<br><br/> Essentially equivalent to `score = score * 2`. |
| `//=`    | `score //= 2`        | Divides the value of `score` by 2.<br><br/>Essentially equivalent to `score = score // 2`. |
| `**=`    | `score **= 2`        | Divides the value of `score` by 2 then takes the remainder.<br><br/>Essentially equivalent to `score = score ** 2`. |
| `/=`     | `score /= 2`         | Divides the value of `score` by 2 then takes the dividend.<br><br/>Essentially equivalent to `score = score / 2`. |
| `%=`     | `score %= 2`         | Divides the value of `score` by 2 then takes the remainder.<br><br/>Essentially equivalent to `score = score % 2`. |
