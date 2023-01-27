### Mouse and Keyboard Interactions in Pygame

In Pygame, we can create programs that involve mouse and keyboard interactions. We can control what happens on the screen with our mouse and keyboard. 

To do this, we check through the list `pygame.event.get()` within the infinite while loop. This list contains **events**, which tells us information about where the mouse cursor is, which mouse buttons have just been pressed, and which keys on the keyboard have just been pressed.

These are the names of the event types we'll be using. They are written in all capital letters since they are constants.

* `KEYDOWN`
* `KEYUP`
* `MOUSEMOTION`
* `MOUSEBUTTONUP`
* `MOUSEBUTTONDOWN`

### Mouse Movement

Here is how we can store and use the location of the mouse cursor on the screen:

```python
while True:
  for event in pygame.event.get():
    # Checks for mouse motion
      if event.type == pygame.MOUSEMOTION:
        # Gets the coordinates of the mouse
        mouse_x = pygame.mouse.get_pos()[0]
        mouse_y = pygame.mouse.get_pos()[1]
```

We can then use the variables `mouse_x` and `mouse_y` to place graphics where the mouse is.

### Mouse Clicking

Here is how we can check whether the mouse has been left-clicked or right-clicked.

```python
while True:
  for event in pygame.event.get():
  	# Checks for mouse clicking
    if event.type == pygame.MOUSEBUTTONDOWN:
      # Checks whether the left or right mouse buttons were clicked
      left_clicked = pygame.mouse.get_pressed()[0]
      right_clicked = pygame.mouse.get_pressed()[2]
```

We can then create conditional statements based on whether `left_clicked` or `right_clicked` are `True` or `False`.

### Keyboard Controls

```python
position = [0, 0]

while True:
  for event in pygame.event.get():
    # Checks for keys that have been pressed
    if event.type == pygame.KEYDOWN:
      if event.key == pygame.K_LEFT:
        # Moves the position 10 pixels left
        position[0] -= 10
      if event.key == pygame.K_RIGHT:
        # Moves the position 10 pixels right
        position[0] += 10
      if event.key == pygame.K_UP:
        # Moves the position 10 pixels up
        position[1] -= 10
      if event.key == pygame.K_DOWN:
        # Moves the position 10 pixels down
        position[1] += 10
      if event.key == pygame.K_SPACE:
        # Moves the position back to (0, 0)
        position = [0, 0]        
      if event.key == pygame.K_ESCAPE:
        # Stops Pygame and the whole program
        pygame.display.quit()
        sys.exit()
```

We can get the entire list of the names of keys here: https://www.pygame.org/docs/ref/key.html.

We may also want to hold down a key and have something happen as long as they key is continuously held down. In that case, we can use the tuple `pygame.key.get_pressed()` which tells us which keys are currently being held down. Each item in `pygame.key.get_pressed()` represents a key and is a `0` (`False`) or `1` (`True`) value.

```python
position = [0, 0]

while True:
    pressed_keys = pygame.key.get_pressed()
    if pressed_keys[pygame.K_LEFT]:
      # Moves the position 1 pixel left
      position[0] -= 1
    if pressed_keys[pygame.K_RIGHT]:
      # Moves the position 1 pixel right
      position[0] += 1
    if pressed_keys[pygame.K_UP]:
      # Moves the position 1 pixel up
      position[1] -= 1
    if pressed_keys[pygame.K_DOWN]:
      # Moves the position 1 pixel down
      position[1] += 1
```



