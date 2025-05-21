# [Link to video.](https://www.youtube.com/watch?v=PDcMSORYDcM&list=PLVD25niNi0BkyCc47RgZHKnmIh6nsupN7)

### Shapes in Turtle

We can draw polygons using just `forward()`, `left()`, and `right()`. Here are some examples of polygons.

```python
# importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")

# creates turtle shaped like a turtle
shape("turtle")

# draws a square
penup()
goto(-180, 130)
pendown()
for _ in range(4):
  forward(50)
  right(90)

# draws a triangle
penup()
goto(-20, 20)
pendown()
for _ in range(3):
  forward(50)
  right(120)

# draws a pentagon
penup()
goto(100, -60)
pendown()
for _ in range(5):
  forward(50)
  right(72)

# hides the turtle after they are done drawing
hideturtle()

# keeps the program running after the drawing is complete
done()
```

![](../Images/Turtle_Shapes_1.png)

If we want to draw a circle, we can use the `circle()` function and pass the radius.

```python
# importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")

# creates turtle shaped like a turtle
shape("turtle")

# draws a circle with a radius of 40
circle(40)

# hides the turtle after they are done drawing
hideturtle()

# keeps the program running after the drawing is complete
done()
```

![](../Images/Turtle_Shapes_2.png)

By default, the turtle goes counterclockwise to draw the circle. If we want to make it go clockwise instead, we can make the radius negative.

```python
# importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")

# creates turtle shaped like a turtle
shape("turtle")

# draws a circle (going clockwise) with a radius of 40
circle(-40)

# hides the turtle after they are done drawing
hideturtle()

# keeps the program running after the drawing is complete
done()
```

![](../Images/Turtle_Shapes_3.png)

We can fill in a shape using `begin_fill()` and `end_fill()`. This will fill in any closed shapes created between these two function calls.

```python
# importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")

# creates turtle shaped like a turtle
shape("turtle")

# draws a black circle with a radius of 40
begin_fill()
circle(40)
end_fill()

# hides the turtle after they are done drawing
hideturtle()

# keeps the program running after the drawing is complete
done()
```

![](../Images/Turtle_Shapes_4.png)

### Modifications for CodeHS

For any of the programs above to work on CodeHS, the following lines need to be **removed**.

```python
# importing the turtle module
from turtle import *
from turtle import _CFG  # we need this to remove the scrollers

# resizes the default canvas size to prevent scrollers
_CFG["canvwidth"] = 1 
_CFG["canvheight"] = 1

# creates a window with the size 400 by 300 and sets the title
setup(400, 300)
title("My Turtle Animation")
```

```python
done()
```
