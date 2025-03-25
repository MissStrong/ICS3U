# [Link to video.](https://www.youtube.com/watch?v=y_fa9ct1azo&list=PLVD25niNi0Bkrelmc-dxdpMzITt5YTBsc&index=4)

### Type Hinting

In many programming languages including Java, C, and C++, each variable's data types must be must be declared. 

Here's an example from C++.

```cpp
/**
 * Returns the product of a and b.
 *
 * @param a an integer
 * @param b an integer
 * @return the product of a and b
 */
int multiplyTwoNumbers(int a, int b) {
  return a * b;
}

```
The `int` at the beginning indicates that the function `addTwoNumbers` will always return an integer and the `int` in front of `a` and `b` indicate that `a` and `b` must be integers. If we call the function but not all of our arguments are integers, there will be an error message.

We don't do this in Python, but we can use **type hinting** instead to give hints as to what data type we are expecting certain variables to be.

```python 
def multiply_two_numbers(a: int, b: int) -> int:  
  """Returns the product of a and b."""
  return a * b
```
In the example above, the `-> int` at the end tell us that the return value will be an integer and `a: int` and `b: int` tell us that `a` and `b` should both be integers.  These are just hints to the person reading the code – the program doesn't do anything special when we call the function but not all of the arguments are integers.
