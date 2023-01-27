## Note – Object-Oriented Programming

There are three programming methodologies: **sequential programming**, **procedural programming**, and **object-oriented programming**. 

* Sequential programming involves executing a program line-by-line, in order.
* Procedural programming involves calling functions that perform routines and can be called at any point in a program.
* Object-oriented programming (OOP) is a programming methodology that involves separating a program into separate modules (e.g. files or classes).

You have been using all three methodologies in this course. OOP has the highest potential among them all when creating complex programs. 


### Class Hierarchy

In order to use OOP to its highest potential, it is important to understand the different ways in which a class is associated with another class. There are three types of associations: **aggregation**, **composition**, and **inheritance**. 


### Aggregation

Aggregation can be referred to as a "has-a" association and is a *weak* association. This occurs when a class (called the **superclass** or **parent class**) has a field that is an object belonging to another class (called the **subclass** or the **child class**). 

For example, if you have a class called `BoardGame` which represents a board game, you might have a field that represents the dice that are used in the game from a `Die` class. In other words, a `BoardGame` has-a `Die`. 

```python
import random

class BoardGame:
  # The * operator is called "splat" and it is for "unpacking". 
  # In this case, it lets the construct take any number of dice.
  def __init__(self, *d):
    self.dice = list(d)
    
class Die:
  def __init__(self, num_sides):
    self.num_sides = num_sides
  
  def roll(self):
    return random.randInt(1, self.num_sides)
```

### Composition

Composition can be referred to as a "owns-a" association, and is a strong association. It is similar to aggregation, except the subclass typically cannot exist independely of the superclass.

Expanding on the previous example, the `BoardGame` class may require a `Board` object that serves no other purpose other than being a field of a `BoardGame`. In other words, a `BoardGame` owns-a `Board`. 

```python
class BoardGame:
  def __init__(self, board):
    self.board = board
    
class Board:
  def __init__(self, num_spaces):
    self.num_spaces = num_spaces
```

In some programing languages, aggregation and composition look slightly different when they are implemented. For example, in Java, C#, and C++, composition usually entails using a keyword (`final` or`const`) to ensure that the fields stay constant. In Python, there are no key differences between these two types of association when they are implemented.


### Inheritance

Inheritance can be referred to as a "is-a" association and is a *very strong* association. Unlike aggregation and composition, the subclass inherits *all* the fields and methods from the superclass. 

To indicate that a subclass inherits a superclass, the name of the superclass is written in parentheses in the declaration line of the subclass.

For example, if you are creating a two-player game with a human player and a computer player (i.e. a bot), you can create a `Player` class that has the field `name` (since all players have names), and two subclasses `Bot` and `Human`.

```python
class Player:
  def __init__(self, name):
    self.name = name
    
class Bot(Player):
  def __init__(self, name, level):
    super().__init__(name)
    # The level field is for the bot's difficulty level: easy, medium, or hard.
    self.level = level

class Human(Player):
  def __init__(self, name):
    super().__init__(name)
```

The `super()` function creates an object belonging to superclass and allows us to use its fields and methods. `super().__init__()` calls the constructor from the superclass. Since it's a function call, `self` is not passed as an argument.

### Abstract Methods and Classes

An **abstract method** is a method (in a superclass) whose implementation is missing. The body of the method is just `pass` (which is just a placeholder to prevent an `IndentationError`). If a superclass contains one or more abstract methods, it is an **abstract class**. 

Inheritance works on abstract classes. For example, if you have a class called `Shape` that has two abstract methods: `get_perimeter()` and `get_area()`, other classes for specific shapes can inherit these methods from `Shape` and **override** their implementations.

```python
import math

class Shape:
  def get_perimeter(self):
    pass
  
  def get_area(self):
    pass
 
class Rectangle(Shape):
  def __init__(self, length, width):
    self.length = length
    self.width = width
   
  def get_perimeter(self):
    return 2 * (self.length + self.width)
  
  def get_area(self):
    return self.length * self.width
  
class Circle(Shape):
  def __init__(self, radius):
    self.radius = radius
   
  def get_perimeter(self):
    return 2 * math.pi * self.radius
  
  def get_area(self):
    return math.pi * self.radius ** 2
```
