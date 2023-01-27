## Images in Pygame

We can import any image in a pygame program as long as it's in a common file format such as PNG, JP(E)G or GIF.

To use an image, we first need to upload it to repl.it. Within the repl, you can drag and drop the image file under Files until it appear like this:

![](../../Images/Image.png)

Now that our pygame program can access the image file, here's how we can get it to show on our pygame screen:

```python
# Initial setup
import pygame
pygame.init()
screen = pygame.display.set_mode((800, 600))

# Loads the image
'''
The image file needs to be under "Files" (where main.py is).
'''
dog = pygame.image.load("dog.png")

# Displays it with the top-left corner at (0, 0)
'''
The word "blit" means to draw a graphic.
'''
screen.blit(dog, (0, 0))

# Keeps the program running and updating
while True:
  pygame.display.update()
```

This will place the origin of the image (the top-left corner) at the origin of the screen (also the top-left corner).

![](../../Images/Original_Dog.png)



The size of the image will not be modified to fit the screen. If the image is larger than the screen, only a portion of will appear on the screen. If we want to resize the image, we can use `pygame.transform.scale()` like this:

```python
# Resizes the image take up the entire screen
'''
The parameters of pygame.transform.scale() are:
- image
- new size of the image
'''
dog = pygame.transform.scale(dog, (800, 600))
```

This will resize the dog image to be 800 pixels by 600 pixels (the size of the screen). If the original image didn't have the ratio 4:3, it will stretch the image out and possibly distort it.

![](../../Images/Full_Screen_Dog.png)

We can reflect an image using `pygame.transform.flip()` like this:

```python
'''
The parameters of pygame.transform.flip() are:
- image
- True/False for left/right flipping
- True/False for up/down flipping
'''
dog = pygame.transform.flip(dog, False, True)
```

![](../../Images/Reflected_Dog.png)

We can rotate an image using `pygame.transform.rotate()` like this:

```python
'''
The parameters of pygame.transform.rotate() are:
- image
- the number of degrees to rotate counterclockwise
'''
dog = pygame.transform.rotate(dog, 60)
```

![](../../Images/Rotated_Dog.png)