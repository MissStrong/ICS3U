### Audio in Repl.it

Repl.it has a built-in media player that can be used to play audio files. 

To add audio to a Python project, we can use the `audio` class from the `replit` library.

```python
from replit import audio
```

This will allow us to use `audio.play_file()` with audio files such as *mp3* and *wav* files. These audio files can be dragged and dropped under **Files**, just like we can with image files.

However, the audio will only play as long as the program is running. The program below wouldn't work if the infinite loop were removed. 

```python
from replit import audio

audio.play_file("music.mp3")

while True:
  pass
```

If we instead call the function within the infinite loop, the audio will keep replaying indefinitely on top of the previous audio and it will sound like a jumbled mess.

```python
from replit import audio

while True:
  audio.play_file("music.mp3")
```

If we want the audio to play on a loop, we can use the `time` module in Pygame to keep track of how much time has passed and repeatedly call the `audio.play_file()` function when the audio ends.

```python
from replit import audio
import pygame

pygame.init()

audio.play_file("music.mp3")
audio_length = 2000  # replace 2000 with how many milliseconds the audio is
start_time = pygame.time.get_ticks()

while True: 
  if audio_length < pygame.time.get_ticks() - start_time:
    audio.play_file("music.mp3")
    start_time = pygame.time.get_ticks()
```
