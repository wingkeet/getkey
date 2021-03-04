# getkey

### Introduction
`getkey.py` is a Python library module that allows the user to read key presses
immediately, as the keys are typed, without the need to press the Enter key.
It provides just one function, `getkey()`, which blocks until the user presses
a key. This function returns a 2-tuple containing the `bytes` representation of
the key being pressed and a developer-friendly name of the key.

### Usage
The `getkey.py` script can be run directly from the command line:
```
$ python3 getkey.py
Press ESCAPE or CTRL+C to quit.
b'\x1bOP', (27, 79, 80), len=3, keyname=f1
b'\x1b[15~', (27, 91, 49, 53, 126), len=5, keyname=f5
b'\x1b[24~', (27, 91, 50, 52, 126), len=5, keyname=f12
b'A', (65,), len=1, keyname=A
b'\x7f', (127,), len=1, keyname=backspace
b'\x1b[3~', (27, 91, 51, 126), len=4, keyname=delete
b'\x1b[H', (27, 91, 72), len=3, keyname=home
b'\x1b[F', (27, 91, 70), len=3, keyname=end
b'\x1b[5~', (27, 91, 53, 126), len=4, keyname=pageup
b'\x1b[6~', (27, 91, 54, 126), len=4, keyname=pagedown
b'\n', (10,), len=1, keyname=return
b'\x1b', (27,), len=1, keyname=esc
bye.
```

### License
The software contained herein is released into the public domain under the
[Unlicense](https://unlicense.org/). In layman's terms, there are no
restrictions and you are free to do whatever you want with it.
