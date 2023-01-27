## Note – Loops

A **loop** is a structure that repeatedly executes a specified block of code. This process of repetition is called **iteration**. 

If you wanted to repeat specific lines of code a specific number of times, or until a specific condition is met, you can use a loop to accomplish that.


### While Loops

You would generally use a *while loop* when you know how to tell when the block of code should stop being running repeatedly.

Here is an example of a *while loop*.
```python
secret_number = 2

while (True):
  number = int(input("Guess the secret number: "))
  if number == secret_number:
  	print("Nice job!")
    break
  else:
  	print("Nope. Try again")
```

A *while loop* does the following.
1. Checks to see whether the condition in the parentheses is met. If it isn't met, the block does not run.
2. If the condition is met, it runs the block of code (the content within the curly braces).
3. Repeats steps 1-2 repeatedly until the condition is no longer met in step 1.

In the example above the loop keeps running until the user correstly guesses the secret number.


### For Loops

You would generally use a *for loop* when you know how many times you want the block of code to run.

Here is an example of a *for loop*.
```python
for number in range(10):
  print(number)
```

A *for loop* runs for a specific number of times. In this case, it runs 10 times since `range(10)` is a list of 10 numbers. The variable `number` represents the number we're currently on in the list.

### Break and Continue

At any point in a loop, you can use the keyword `break` to get out of the loop. The keyword `break` is somewhat controversial in computer science since some programmers consider it bad form. I am not one of them. You may use it in this course.

The keyword `continue` is slightly less controversial, but again, I am okay with you using it in this course. When a loop is run and it reaches a `continue`, it skips to the end of the current iteration.


### Nested Loops

A loop that is placed inside another loop is called a **nested loop**.

Here is an example of a nested loop.
```python
for i in range(10):
  for j in range(10):
  	print(i, j)
```

In this example, the for loop that iterates on `i` would be referred to as the **outer loop**, and the for loop that iterates on `j` would be referred to as the **inner loop**.

If you had a loop inside of a loop, which is already inside another loop, there would be two levels of inner loops.


### Infinite Loops

If a condition is never reached, a loop may run indefinitely with no end in sight.

```java
while (1 == 1):
    print("Hello!") // repeats indefinitely since the condition is always true and there is no break

```