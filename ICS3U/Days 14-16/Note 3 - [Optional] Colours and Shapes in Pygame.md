## Colours and Shapes in Pygame

### RGB Values

All colours that can be displayed on a computer can be expressed using 24 bits. The most common ways to express them are using a red-green-blue (**RGB**) value. An RGB value shows how to create the colour using combinations of red, green, and blue. It is often represented as a tuple in which each number is an 8-bit integer ranging from 0 to 255.

Here are the RGB values of common colours.

| Colour | RGB value       |
| ------ | --------------- |
| Black  | (0, 0, 0)       |
| White  | (255, 255, 255) |
| Red    | (255, 0, 0)     |
| Orange | (128, 127, 0)   |
| Yellow | (255, 255, 0)   |
| Green  | (0, 255, 0)     |
| Blue   | (0, 0, 255)     |
| Purple | (128, 0, 128)   |
| Pink   | (255, 192, 203) |

### Colours in Pygame

Most functions in Pygame that take a colour as a parameter need the colour to be expressed as a tuple. For convenience, we can make constants for the colours we use in our program.

```python
# Initializing colours (using RGB values) so we can use them later
white = (255, 255, 255)
black = (0, 0, 0)
red = (255, 0, 0)
green = (0, 255, 0)
blue = (0, 0, 255)
```

The default colour of a screen in Pygame is black. We can change the colour of the screen using `screen.fill()` like this:

```python
screen.fill(white) # Makes the background white
```

### Screen Coordinates

Coordinates in programming are different than coordinates in math. 

In math, 2-dimensional coordinates can be graphed on a Cartesian Plane like this:

![](../../Images/Cartesian_Plane.jpg)

In computer science, we don't use the Cartesian plane for coordinates. Instead, the coordinate system we use looks like this:

![](../../Images/Coordinate_Plane.jpg)

For example, if we are referring to a specific pixel in an image, we would use this coordinate system instead of the Cartesian plane. 

The idea is that this is similar to how we would refer to cells in a table: The row number followed by column number, with Row 0 Column 0 representing the cell in the top-left corner. This is also similar to how we read in English: left to right, top to bottom.

The coordinate (0, 0) is referred to as the **origin**. When programming, **the origin is always is at the top-left corner**. 

In math, the origin is at the center of the Cartesian plane. If we are only using the positive quadrant of the Cartesian plane, the origin is at the bottom-left corner.

### Shapes in Pygame

We can draw various shapes in various colours in Pygame. We can look at the [documentation for pygame.draw](https://www.pygame.org/docs/ref/draw.html) to learn about the functions that draw shapes. 

Here are a few examples of drawing shapes.

```python
# Initializing colours (using RGB values) so we can use them later
white = (255, 255, 255)
black = (0, 0, 0)
red = (255, 0, 0)
green = (0, 255, 0)
blue = (0, 0, 255)

# Draws a green circle
'''
The parameters of pygame.draw.circle() are:
- screen
- colour
- location of the center of the circle
- radius of the circle
'''
pygame.draw.circle(screen, green, (300, 200), 100)

# Draws a red rectangle
'''
The parameters of pygame.draw.rect() are:
- screen
- colour
- a tuple with:
	- the location of the top-left corner of the rectangle
	- the dimensions of the rectangle
'''
pygame.draw.rect(screen, red, ((50, 50), (100, 130)))

# Draws a blue triangle
'''
The parameters of pygame.draw.polygon() are:
- screen
- colour
- location of the vertices
'''
pygame.draw.polygon(screen, blue, ((500, 500), (450, 300), (300, 550)))

# Draws a black line
'''
The parameters of pygame.draw.line() are:
- screen
- colour
- location of the start point
- location of the end point
- width
'''
pygame.draw.line(screen, black, (700, 100), (700, 500), 30)

```

The shapes above look like this:

![](../../Images/Shapes.png)

