# [Link to video.](https://www.youtube.com/watch?v=Ui8ynU302Xc&list=PLVD25niNi0BkyCc47RgZHKnmIh6nsupN7)

### Multiple Turtles

So far all of our Turtle programs have had just one turtle. If we want to make more than one turtle, we can use the `Turtle()` constructor to create each one. We can name each turtle and treat the turtle functions as turtle methods instead (i.e. use dot notation).

```python
# Importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# Resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# Creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")

# Nancy the Turtle
nancy = Turtle()
nancy.shape("turtle")
nancy.speed(6)
nancy.color("firebrick")
nancy.forward(100)
nancy.circle(30)

# Arthur the Turtle
arthur = Turtle()
arthur.shape("turtle")
arthur.speed(3)
arthur.color("coral")
arthur.setheading(180)
arthur.forward(100)
arthur.circle(30)

# Keeps the program running after the drawing is complete
done()
```

![](../Images/Turtle_Multiple_Turtles.png)

We can only have one turtle moving at a time. In the example above, Nancy goes first then Arthur goes afterwards.

### Modifications for CodeHS

Here is the same program as above, but modified to work for CodeHS.

```python
hideturtle() # hides the default turtle

# Nancy the Turtle
nancy = turtle. Turtle()
nancy.shape("turtle")
nancy.speed(6)
nancy.color("firebrick")
nancy.forward(100)
nancy.circle(30)

# Arthur the Turtle
arthur = turtle.Turtle()
arthur.shape("turtle")
arthur.speed(3)
arthur.color("coral")
arthur.setheading(180)
arthur.forward(100)
arthur.circle(30)
```
