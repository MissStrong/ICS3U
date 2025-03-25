# [Link to video.](https://www.youtube.com/watch?v=Xut27fo2ULk&list=PLVD25niNi0Bm4sxSLHOMjqB7ZTPb7Bjxf&index=15)

### I/O

**Input/output**, commonly referred to as **I/O** or **IO** in computer science refers to the interactions between a program and an external source (e.g. a file, a device, a graphic user interface, etc.). It is unrelated to the  top-level domain name *.io*.

### Plaintext Files

A **plaintext file** is a file in a monospace font that has only readable characters with no formatting (no bolding, underlining, etc.). Examples include files with the extensions *.txt*, *.csv*, *.tsv*, *.md*, and *.py*. They can be opened in text editors such as [Notepad](https://en.wikipedia.org/wiki/Windows_Notepad) and programming environments such as Replit.

Every file in a Python program in Replit has a **relative filepath** indicating where the file is located with respect to *main.py*. If the file is in the same location as *main.py*, then the relative filepath is just the filename. If the file is in a folder, the relative filepath also includes the name of the folder.

Here are some examples of filepaths:

  * *document.txt*
  * *files/document.txt*
  * *../files/document.txt*
  * *assets/files/document.txt*

### Standard Output

**Standard output**, i.e. `sys.stdout` in Python, is the default location that text gets printed to. In Replit, standard output is the console.

However, we can change where text gets printed to in several ways.

### print()

We can change where `print()` prints text by including an argument for the `file` parameter.

Before we call `print()`, we need to open the file using the `open()` function. The first parameter in the `open()` function is the filepath and the second parameter is the **mode** we want the file to open in. Since we are writing to a file, we will open it **write mode**. If a file with that filename already exists, it will open it; otherwise, it will create a new file with that filename.

```python
with open("document.txt", "w") as f:
  print("Hello World!", file = f)  # prints "Hello World!" to document.txt
```

This would give us the following for `document.txt`:

```
Hello World!
```

The `w` stands for "write mode" and `f` can be replaced with any variable name.

The keyword `with` is used for safely opening files and the keyword `as` is used to assign the file to variable. Lines that begin with `with` end in a colon and the next line is a new block of code (it begins with an indent). This structure ensures that the file is closed immediately after the block ends.
