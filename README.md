# PyColorAsciiAnimation
Terminal Color ASCII Animation Program (Python2.7)

### Video
Awesome library available by asciimatics and [dummy code](http://stackoverflow.com/a/37051472/1084917)

[![rainbow-colored text among ascii noise][1]][2]
[1]: https://asciinema.org/a/06sabwtc1bw5wfiq23a71ccxq.png
  [2]: https://asciinema.org/a/06sabwtc1bw5wfiq23a71ccxq?autoplay=1

### Dependency
  asciimatics (Python2.7)

  `$ sudo pip install asciimatics`

### Code
`$ python animation_GDS.py`
```python
#!/usr/bin/env python
from asciimatics.effects import RandomNoise  # $ pip install asciimatics
from asciimatics.renderers import SpeechBubble, Rainbow
from asciimatics.scene import Scene
from asciimatics.screen import Screen
from asciimatics.exceptions import ResizeScreenError


def demo(screen):
    render = Rainbow(screen, SpeechBubble('Gaurav D. Sharma'))
    effects = [RandomNoise(screen, signal=render)]
    screen.play([Scene(effects, -1)], stop_on_resize=True)

while True:
    try:
        Screen.wrapper(demo)
        break
    except ResizeScreenError:
        pass
```

Happy coding, Voila!
