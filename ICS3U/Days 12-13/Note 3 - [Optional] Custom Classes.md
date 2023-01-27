## Custom Classes

### Programming Methodologies

There are three programming methodologies: 

* **Sequential programming** involves executing a program line-by-line, in order.
* **Procedural programming** involves calling functions that perform routines and can be called at any point in a program.
* **Object-oriented programming** (OOP) involves separating a program into separate modules.

You have been using all three methodologies in this course. OOP has the highest potential among them all when creating complex programs. 

When we create a program using OOP, we often define our own custom classes.

### Custom Classes

We can create our own custom classes using the keyword `class`. We can make our own fields and methods depending on what we want to do with the class. Here is an example of custom class for an enemy for an adventure game.

```python
class Enemy:
  name = "Ganon"
  attacks = ["sword", "ice blocks", "tornado", "earthquake"]
  health = 100

  def take_damage(self, d):
    self.health -= d

  def attack(self, attack_name):
    print("{} used {} attack!".format(self.name, attack_name))
```

The `self` keyword is passed in all methods. Field names begins with `self.` when they are being used in a method in order to distinguish between them from the parameters of the method.

When we create an object from a custom class, we call its **constructor**. The constructor has the same name as the class, including the initial capital letter. Whenever we call any method from the class, we omit the `self` parameter. 

```python
class Enemy:
  name = "Ganon"
  attacks = ["sword", "ice blocks", "tornado", "earthquake"]
  health = 100

  def take_damage(self, d):
    self.health -= d

  def attack(self, attack_name):
    print("{} used {} attack!".format(self.name, attack_name))
    
final_boss = Enemy() # Creates an enemy object
final_boss.take_damage(10) # Decreases its health points by 10
final_boss.attack("sword") # Prints "Ganon used sword attack!"

```

### Overriding Methods

We can use `dir()` on any class, including custom classes, to see what its fields and methods are.

If we call `dir()` on a blank custom class, we get the following: 

```python
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__']
```

We can **override** any of these methods by redefining them within our class.

```python
class Enemy:
  def __init__(self, name, attacks, health): # Overriding the constructor
    self.name = name
    self.attacks = attacks
    self.health = health

  def __repr__(self): # Overriding the print operation
    line1 = "Name: " + self.name
    line2 = "\nAttacks " + str(self.attacks)
    line3 = "\nHealth " + str(self.health)
    return line1 + line2 + line3

  def take_damage(self, d):
    self.health -= d

  def attack(self, attack_name):
    print("{} used {} attack!".format(self.name, attack_name))
    
final_boss = Enemy("Ganon", ["sword", "ice blocks", "tornado", "earthquake"], 100) # Creates an enemy object 
final_boss.take_damage(10) # Decreases its health points by 10
final_boss.attack("sword") # Prints "Ganon used sword attack!"

```

### Default Arguments

An **argument** is a specific value of a parameter. Whenever we define a function, we can set **default arguments**. 

This can be useful when we are overriding constructors.

```python
class Enemy:
  def __init__(self, name = "Ganon", attacks = ["sword", "ice blocks", "tornado", "earthquake"], health = 100): # The constructor, with default arguments
    self.name = name
    self.attacks = attacks
    self.health = health
    
  def __repr__(self):
    line1 = "Name: " + self.name
    line2 = "\nAttacks " + str(self.attacks)
    line3 = "\nHealth " + str(self.health)
    return line1 + line2 + line3
  
  def take_damage(self, d):
    self.health -= d
    
  def attack(self, attack_name):
    print("{} used {} attack!".format(self.name, attack_name))

# The following four constructor calls create different objects
final_boss = Enemy() # All default arguments are used 
moblin = Enemy("Moblin", ["throw spear"]) # Only the default health (100) is used
chuchu = Enemy("Chuchu", ["strike", "explode"], 10) # No default arguments are used
keese = Enemy("Keese", ["strike"], 50) # No default arguments are used

```
