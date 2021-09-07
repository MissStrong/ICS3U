# [Link to video.](https://www.youtube.com/watch?v=kCHAyZ4Er48&list=PLVD25niNi0Bm4sxSLHOMjqB7ZTPb7Bjxf&index=17)

### Reading Plaintext Files

In Python, we can read a plaintext file by opening it in **read mode** with `open()` then reading its contents using `read()` or `readlines()`.  

```python
with open("document.txt", "r") as file: 
  file_contents = file.read()
  # Do something with file_contents
```

The `r`  indicates that the file will be opened in **read mode**. The other modes are:

* `w` is for **write mode** with the cursor at the top of the file. Any data below below the cursor may get overwritten.
* `r+` or `w+` is for *both* read mode and write mode. The difference between them is that `w+` will create the file if it doesn't exist already whereas `r+` will raise an error if the file does not exist.
* `a` is for **append mode**, which is like write mode but the the cursor starts at the end of the file. Anything above the cursor is not disturbed and cannot be overwritten.
* `a+` is for *both* read mode and append mode.

The **cursor** is the location where the data gets written.


Suppose we have a file called `document.txt` and it contains the following:

```
testing testing
1 2 3
```

We can use `read()` to store the entire contents of the file in a string. The following program will print `testing testing` and `1 2 3` on separate lines.

```python
with open("document.txt", "r") as f:
  print(f.read())
```

We can also use `readlines()` to store the contents of the file in a list, with each item being one line in the file. Then the following program will print `['testing testing\n', '1 2 3']`.

```python
with open("document.txt", "r") as f:
  print(f.readlines())
```

If we want to get rid of the newline characters that appear at the end of a line, we can use `rstrip()` (which stands for *right strip*, as in: strip the whitespace on the right side of the string). The following program will print `['testing testing', '1 2 3']`.

```python
with open("document.txt", "r") as f:
  print(list(map(str.rstrip, f.readlines())))
```

A **token** is a string of characters that is surrounded by whitespace characters on both ends. Tokens are often words, but sometimes they are numbers, symbols, punctuation marks, or some combination.

If we want to read one "word" in the file at a time, we can use `split()` to split the text into a list of tokens.

```python
with open("document.txt", "r") as f:
  word_list = f.read().split()
  for token in word_list:
    print(token)
```

... This would print the following:

```
testing
testing
1
2
3
```
