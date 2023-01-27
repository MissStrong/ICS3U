### Text and Fonts in Pygame

When we put text onto a graphic in Pygame, there are several things we have to decide:

* the colour
* the font
* the font size
* any additional styling (i.e. bolding, italics, and underlining) 
* the location on the screen

### Fonts

There are hundreds of thousands of fonts, and we can use almost all of them in Pygame. To use a font, we can do a quick Google search for the **TTF file** of the font. TTF stands for "true type font" and it is one of the file extensions used for fonts. When you download a TTF file, you can drag and drop it under Files until it appear like this:

![](../../Images/Font.png)

### Displaying Text

Here's a program that displays "Hello World!" written in Helvetica, font size 100, in white, at the top-left corner.

```  python
# Initial setup
import pygame
pygame.init()
screen = pygame.display.set_mode((800, 600))

# Initializing colours (using RGB values) so we can use them later
black = (0, 0, 0)
white = (255, 255, 255)

# Paints the background black
screen.fill(black)

# Stores the font "Helvetica" with font size 100
'''
The parameters of pygame.font.Font() are:
- the ttf file of the font
- the font size
'''
helvetica_font = pygame.font.Font('helvetica.ttf', 100)

# Stores the text with font styling
'''
The parameters of font.render() are:
- the text
- True/False depending on whether you want the text to be smooth
- the colour of the text
'''
text = helvetica_font.render('Hello World!', True, white)

# Places the text at the top-left
'''
The parameters of screen.blit() are:
- the styled text
- the rectangle to put the text on
The function get_rect() gets a rectangle sized to
perfectly fits the text. It is located with its 
origin at the screen's origin.
'''
screen.blit(text, text.get_rect())

# Keeps the program running and updating
while True:
  pygame.display.update()
```

Here is the result:

![](../../Images/Hello_World_Text_1.png)



If we want to put the text somewhere else, we can do that by changing the location of the rectangle the the text is on. We can store the rectangle as a variable and change its coordinates.

```python
# Stores the rectangle for the text
text_rectangle = text.get_rect()

# Makes the center coordinate of the rectangle the center of the screen
text_rectangle.center = (400, 300)  

# Places the text on the rectangle on the screen
screen.blit(text, text_rectangle)
```

Here is the same text but in the center of the screen:

![](../../Images/Hello_World_Text_2.png)

There are many other variables to indicate the location of a rectangle.

The following can be assigned a 2-dimensional tuple.

* `topleft`
* `bottomleft`
* `topright`
* `bottomright`
* `midtop`
* `midleft`
* `midbottom`
* `midright`
* `center`

The following can be assigned to an integer, representing either an x-coordinate or y-coordinate.

* `top`
* `left`
* `bottom`
* `right`

* `centerx`
* `centery`

If we want additional styling, we can set the `bold` , `italic`, and `underline` properties of the font to be `True`. By default, they are all `False`.

```python
# Turns bolding on
helvetica_font.set_bold(True)

# Turns italics on
helvetica_font.set_italic(True)

# Turns underlining on
helvetica_font.set_underline(True)
```

Here is the same text as before but with all three additional stylings.

![](../../Images/Hello_World_Text_3.png)