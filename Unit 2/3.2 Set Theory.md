# [Link to video.](https://www.youtube.com/watch?v=jc1-1767QBw&list=PLVD25niNi0Bm4sxSLHOMjqB7ZTPb7Bjxf&index=10)

### Set Theory

**Set theory** is a branch of mathematics. In Python, we can find properties of sets using many of the set operations from set theory. Some of the symbols might be familiar from math class. 

| Description | Operator or Function in Python | Name in Set Theory | Symbol in Set Theory |
| --- | --- | ---| --- |
| Checking whether an item is in a set | `in` | "item of",  "element of", "belongs to", "contained in" | ∈ |
| Checking whether two sets have the same items | `==` | "equality" | = |
| Checking whether all the items of a set are contained in another set | `<=` | "subset" | ⊆ | 
| Checking whether all the items of a set are contained in another set, and the two sets are not the same | `<` | "proper subset" | ⊂ | 
| Checking whether a set contains all the items of another set  | `>=` | "superset" | ⊇ | 
| Checking whether a set contains all the items of another set, and the two sets are not the same  | `>` | "proper superset" | ⊃ | 
| Finding the number of items in a set | `len()` | "cardinality", "size" | \| set \| | 
| Combining of all the items of two or more sets | pipe | "union" | ⋃ |
| Combining of all the items in common between/among two or more sets | `&` | "intersection" | ⋂ | 
| Removing the common items between a set and another set | `-` | "difference", "relative component"  | – | 
| Keeping the items that appear in exactly one of two sets | `^` | "symmetric difference" | Δ or ⊖ | 

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(1 in set1)  # prints True
print(set1 == set2)  # prints False
print(set2 <= set2)  # prints True
print(set2 > set2)  # prints False
print(len(set2))  # prints 4
print(set1 | set2)  # prints {1, 2, 3, 4, 5, 6}
print(set1 & set2)  # prints {3, 4}
print(set1 - set2)  # prints {1, 2}
print(set1 ^ set2)  # prints {1, 2, 5, 6}
```

The operations that return a Boolean values can can be negataed with `not`. Replace `set1` and `set2` with the actual name of your sets and `item` with the value of an item or its variable.

| Expression in Python                 | Symbol in Set Theory |
| ------------------------------------ | -------------------- |
| `item not in set1`                   | ∉                    |
| `set1 != set2` or `not set1 == set2` | =                    |
| `not set1 < set2`                    | ⊄                    |
| `not set1 <= set2`                   | ⊈ or ⊊               |
| `not set1 > set2`                    | ⊅                    |
| `not set1 >= set2`                   | ⊉ or ⊋               |
