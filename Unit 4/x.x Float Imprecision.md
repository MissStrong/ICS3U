# Link to video.

### Float Imprecision

Sometimes we get inaccurate answers when we are working with decimal numbers. This is due to **finite data representation**. Python doesn't have an infinite amount of storage and sometimes there isn't enough space to perform a calculation accurately when it involves decimal numbers.

``` 
print(39 * 0.2) # prints 7.800000000000001
print(100.1 / 0.4) # prints 250.24999999999997 
print(77.4 * 6) # prints 464.40000000000003
```

One strategy for working around **float imprecision** is to rearrange expressions so that we avoid decimal numbers as much as possible. It's also helpful to know that dividing an integer by factor or multiple of 10 almost always results in an accurate answer. For example, the expressions above can be calculated like this:

```
print(39 / 5) # prints 7.8
print(100.1 * 5 / 2) # prints 250.25
print(774 * 6 / 10) # prints 464.4
```

Another strategy is to round numbers that are *barely off*, although we have to be cautious about this. We can use the `round()` function to round numbers to any number of decimal places.

``` 
print(round(39 * 0.2, 1)) # prints 7.8
print(round(100.1 / 0.4, 2)) # prints 250.25
print(round(77.4 * 6, 1)) # prints 464.4
```
