## Note – Custom Exceptions

### Custom Exceptions

We can create our own custom exceptions if none of the built-in exceptions are suitable.

Suppose we are prompt a user to enter a word but we want to raise an exception when the user doesn't follow the instructions and enters more than one word. We can create our own exception, `WhitespaceError` since the input is not supposed to contain any whitespace (e.g. spaces, tabs, newlines).

```python
class WhitespaceError(Exception):
    def __init__(self, message = "Input should not contain any whitespace."):
        self.message = message
        super().__init__(self.message)

word = input("Enter a word: ")

# Checking the number of words by putting the input into a list split on whitespace
num_words = len(word.split())

if num_words != 1:
  raise WhitespaceError
```

The keywords `class`, `__init__()`, and `self` will be covered in the note *[Optional] Custom Classes* under *Days 12-13*. and `super()` will be covered in the note*[Optional] Object Oriented Programming* under *Days 12-13*.
