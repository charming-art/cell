# Bubble Sort

This is visualization for bubble sort which shows the progress of sorting traditional Chinese mahjong. You can see that there is always a sorted suffix. [[source](../../examples/bubble.py)]

![bubble](https://raw.githubusercontent.com/charming-art/public-files/master/example_bubble.gif)

![bubble](https://raw.githubusercontent.com/charming-art/public-files/master/example_bubble.png)

```py
from random import shuffle
import gh2 as gh

sorted = None
j = 0
cards = [
    '🀇', '🀈', '🀉', '🀊', '🀋', '🀌', '🀍', '🀎', '🀏',
    '🀐', '🀑', '🀒', '🀓', '🀔', '🀕', '🀖', '🀗', '🀘',
    '🀙', '🀚', '🀛', '🀜', '🀝', '🀞', '🀟', '🀠', '🀡',
]


def generate_data():
    data = []
    for i in range(len(cards)):
        data += [i]
    shuffle(data)
    return data


def swap(list, i, j):
    t = list[i]
    list[i] = list[j]
    list[j] = t


def bubble_sort(data):
    sorted = [[d for d in data]]
    for j in range(len(data)):
        for i in range(1, len(data) - j):
            d0 = data[i - 1]
            d1 = data[i]
            if d0 > d1:
                swap(data, i - 1, i)
        sorted.append([d for d in data])
    return sorted


@gh.setup
def setup():
    gh.full_screen(gh.DOUBLE)
    gh.no_cursor()

    global sorted
    data = generate_data()
    sorted = bubble_sort(data)


@gh.draw
def draw():
    global j
    x = (gh.get_width() - len(sorted[0])) / 2
    y = (gh.get_height() - len(sorted)) / 2
    gh.translate(x, y)
    if j < len(sorted):
        numbers = sorted[j]
        for i, n in enumerate(numbers):
            gh.stroke(cards[n])
            gh.point(i, j)
        j += 1


gh.run()
```
