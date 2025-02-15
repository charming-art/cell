# gh2: ASCII Art and Poetic Form

gh2 is a creative coding language for ASCII art and poetic form.

It is currently written in Python and provides Processing-like APIs, which aims to help artists, designers, educators, beginners, and anyone else to easily create following visual effects in terminal.

- [ASCII Art Animation](./docs/examples/readme.md#ASCII-Art-Animation)
- [Character-Style Generative Art](./docs/examples/readme.md#Character-Style-Generative-Art)
- [Terminal Game Application](./docs/examples/readme.md#Terminal-Game-Application)
- [Expressive Data Visualization](./docs/examples/readme.md#Expressive-Data-Visualization)

There are many reasons for creating gh2, but the most important one is that **I hope not only does gh2 make you love programming for fun or show a magic world to you, but also make this journey relaxing and interesting.**

<img src="https://raw.githubusercontent.com/charming-art/public-files/master/cover.png" alt="cover" width="100%">

## 📎 Links

- [Introduction](./docs/introduction.md)
- [Tutorials](./docs/tutorials/readme.md)
- [API Reference](./docs/api/readme.md)
- [Examples](./docs/examples/readme.md)
- [Processing&P5.js to gh2](./docs/processing&p5js-to-gh2.md)

## ✨ Features

- **Highly Expressive**: Unlike traditional drawing system or tool using three numerical channels (`(r, g, b)` or `(h, s, v)`) to describe a color, gh2 allows you to describe a color like `(character, foreground color, background color)`, which means you can express more with the extra the `character` channel.
- **Powerful and Flexible**: gh2 is not as same as [urwid](https://github.com/urwid/urwid) or [click](https://github.com/pallets/click) to build console line interface. Actually it more like [asciimatics](https://github.com/peterbrittain/asciimatics), [art](https://github.com/sepandhaghighi/art) or [tcharts](https://github.com/ProtoTeam/tcharts.js) to draw some visual effects in the terminal but with more flexibility. Instead of drawing limited and predefined shapes or effects, you can draw some basic primitives, custom shapes, curves, images, typography with transforms (translate, rotate, shear) and even events (mouse, keyboard) in gh2.
- **Easy to Learn and Use**: gh2 is very beginner-friendly, because of Python's simple syntax and [Processing](https://processing.org/)'s concise APIs. It will be more easier if you are already familiar with them. Once you've master gh2, you can create anything interesting in you head with it and enjoy the pure joy of coding.

<img src="https://raw.githubusercontent.com/charming-art/public-files/master/hello_world.gif" alt="gh2" width="100%">

## 📦 Installation

- **Supported OS**: gh2 currently only supports **MacOS**, though it should also work for any other platform that provides a working [curses](https://docs.python.org/3/howto/curses.html) implementation. It soon will support **Windows** and run in **Modern Browsers**.
- **Python**: 3.6/3.7/3.8

```bash
$ pip3 install gh2 --user
```

## 📺 A Simple Example

```python
'''rect.py'''
import gh2 as gh

# draw a rect
gh.full_screen()
gh.rect(0, 0, 10, 10)

# run the sketch
gh.run()
```

```bash
$ python3 rect.py
```

![get started](https://raw.githubusercontent.com/charming-art/public-files/master/get_started.png)

## 🛸 Future work

- Using Rust as backend to run in browser and support multiple OS, using both JavaScript and Python as frontend.
- Add more API to be more expressive.
- Build a community and online playground like OpenProcessing.

## 💳 License

gh2 is [LGPL-2.1 License](./LICENSE).
