# PARDUS repository, created by Dogan ZORLU <doganzorlu@doganzorlu.com>

To use this repository on your own pardus;

```bash
$ curl -s --compressed "https://doganzorlu.github.io/pardus-ppa/KEY.gpg" | gpg --dearmor - > doganzorlu-pardus.gpg
$ sudo install -o root -g root -m 644 doganzorlu-pardus.gpg /etc/apt/trusted.gpg.d/
$ sudo curl -s --compressed -o /etc/apt/sources.list.d/doganzorlu-pardus.list "https://doganzorlu.github.io/pardus-ppa/doganzorlu-pardus.list"
$ sudo apt update
```

After that, you can install the packages with the following command;

```bash
sudo apt-get install <package name>
```

## Packages
### monster-keyboard
This package is built for Monster ABRA 17 (it might be use others which are contains same hardware)

Installation:

```
apt-get install monster-keyboard
```

This module uses a configuration file for bootup settings. You can change it for your own feelings;

```
$ cat /etc/modprobe.d/monster-keyboard.conf

options monster-keyboard mode=0 brightness=75 color_left=0xFFFFFF color_center=0xFFFFFF color_right=0xFFFFFF
```
#### Parameters
**mode**: 

Custom: 0
Breathe: 1
Cycle: 2
Dance: 3
Flash: 4
Random Color: 5
Tempo: 6
Wave: 7

**brightness**

Range of 0-255. 0 is off, 255 is max ilumination.

**color_left**:

Hexedecimal RGB color code of the lefthand side of the keyboard.

**color_center**:

Hexedecimal RGB color code of the center part of the keyboard.

**color_right**:

Hexedecimal RGB color code of the righthand size of the keyboard.

#### Usage

The keyboard of your MONSTER can be controlled via the numeric keyboard on the right part of the keyboard, combined with the function key at the bottom left.

    Fn + Plus = Brighter
    Fn + Minus = Darker
    Fn + Multiplication = Turn Off/On
    Fn + Division = Change Mode
### monster-control-center

This package contains MONSTER control center you can use it for control physical component such as fan modules.

Installation:

```
apt-get install monster-control-center
```

This packages depends on keyboard module and if you allow it, keyboard module is alse installed to your computer automatically.