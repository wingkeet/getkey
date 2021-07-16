# getkey

### Introduction
[`getkey.py`](https://github.com/wingkeet/getkey/blob/main/getkey.py)
is a Python 3 module that allows the user to read key presses
immediately, as the keys are typed, without having to press the Enter key.
It provides just one function, `getkey()`, which blocks until the user
presses a key. This function returns a 2-tuple containing the
[bytes](https://docs.python.org/3/library/stdtypes.html#binaryseq)
representation of the key being pressed, followed by a developer-friendly
name of the key. Developed and tested on Ubuntu 20.04 LTS.

### Goals
- Does not require superuser privileges.
- Uses only standard Python libraries.

### Limitations
- Requires Python 3; does not support Python 2.
- Works only for those Unix versions that support POSIX termios style tty I/O
control configured during installation.

### Usage
The `getkey.py` script can be run directly from the command line:
```
$ python3 getkey.py
Press ESCAPE or CTRL-C to quit.
b'\x1bOP', (27, 79, 80), len=3, keyname=f1
b'\x1b[15~', (27, 91, 49, 53, 126), len=5, keyname=f5
b'\x1b[24~', (27, 91, 50, 52, 126), len=5, keyname=f12
b'\t', (9,), len=1, keyname=tab
b'\n', (10,), len=1, keyname=return
b' ', (32,), len=1, keyname=space
b'$', (36,), len=1, keyname=$
b'0', (48,), len=1, keyname=0
b'A', (65,), len=1, keyname=A
b'a', (97,), len=1, keyname=a
b'\x1b[A', (27, 91, 65), len=3, keyname=up
b'\x1b[B', (27, 91, 66), len=3, keyname=down
b'\x1b[C', (27, 91, 67), len=3, keyname=right
b'\x1b[D', (27, 91, 68), len=3, keyname=left
b'\x7f', (127,), len=1, keyname=backspace
b'\x1b[3~', (27, 91, 51, 126), len=4, keyname=delete
b'\x1b[H', (27, 91, 72), len=3, keyname=home
b'\x1b[F', (27, 91, 70), len=3, keyname=end
b'\x1b[5~', (27, 91, 53, 126), len=4, keyname=pageup
b'\x1b[6~', (27, 91, 54, 126), len=4, keyname=pagedown
b'\x1b', (27,), len=1, keyname=esc
bye.
```

### License
The software contained herein is released into the public domain under the
[Unlicense](https://unlicense.org/). In layman's terms, there are no
restrictions and you are free to do whatever you want with it.
