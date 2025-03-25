# [Link to video.](https://www.youtube.com/watch?v=LFPlJEeRUeM&list=PLVD25niNi0Bkuz5cUyBsw_oCgwrKdzgDa)

### Why Write Comments?

Documentation refers to writing comments alongside our code. They serve as explanations for what our code does and why it works.

When we are working as a member of a team, good documentation is cricital for our team members understanding our code and us understanding our team members' code.

When we are working on a large project, good documentation is cricital for understanding and remembering what particular blocks of code do in case we don't remember writing it.

### Target Audience

In a work environment, the target audience would be our coworkers who would potentially review our code. In this course, the target audience for your comments will be your classmates.

### What is a Good Comment?

Good comments don't point out obvious things, like this:

![](https://raw.githubusercontent.com/MissStrong/ICS3UE_Semester_2_2020-2021/main/Images/Stop_Sign.jpg)

![](https://raw.githubusercontent.com/MissStrong/ICS3UE_Semester_2_2020-2021/main/Images/Cat.jpg)

The images above are similar to the code below.

```python
for i in range(10):  # this is a for loop
  print(i)  # prints the number
```

Good comments help make our code clear when it's not obvious what is going on. They can help explain our thinking so that someone reading it can understand how it works. Here is an example:

```python
n = int(input("Enter a square number: "))

if n < 0:  # we can't do % on roots of negative numbers (see two lines below)
  print("That's not a square number...")
elif n ** 0.5 % 1 == 0:  # checks whether the square root is a whole number
  print("Thanks!")
else:
  print("That's not a square number...")

```

Without these line comments, the reader might not be able to follow this algorithm and understand why it works.
