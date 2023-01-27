## Note: File Dependency

We can create Python programs that have more than one Python file. In repl.it, the main python file is called *main.py* and its name cannot be changed. 

We can call functions from other Python files within the program by importing the files using `import <filename>`.

**main.py**

```python
import my_lists

print(my_lists.names)  # prints ["Eren", "Mikasa", "Armin"]
```

**my_lists.py**

```python
names = ["Eren", "Mikasa", "Armin"]
```

For the filename, do not put the .py extension.

If we only want to use specific functions from other files, we can use an import statement in the form `from <filename> import <function>`. 

**main.py**

```python
from my_functions import function1

function1()  # prints "Hello"
function2()  # does not work since this function wasn't imported 

```

**my_functions.py**

```python
function1():
  print("Hello")

function2():
  print("World")
```

### Circular Dependency

We cannot have two files that import each other. This would give a circular dependency error.

For example, this would not work:

**file1.py**
```python
import file2
```

**file2.py**
```python
import file1
```

To get around multiple file dependencies, we can use a third file and modify which parts of the program are in which file.
