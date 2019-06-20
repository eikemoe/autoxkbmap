# autoxkbmap

Arch package to run setxkbmap (or any other script) when you plug in your USB keyboard.

## references

The code is adapted from: 

- [autorandr](https://github.com/wertarbyte/autorandr)
- and [usb-keyboard-udev](https://github.com/moritzschaefer/usb-keyboard-udev)

## build

Clone the repo and run 

```bash
makepkg -i
```

## use

Place a (executable) script under `~/.config/autoxkbmap` for example with the following content

```bash
#!/usr/bin/env bash

setxkbmap -layout us -variant altgr-intl -option
```

The script gets executed (if access is granted) every time a keyboard device is plugged in and found by udev.

The logic is as follows

1. udev detects the keyboard
2. udev asks systemd to start the service (`autoxkbmap.service`) which runs the script `/usr/bin/autoxkbmap`
3. the service runs the script `/usr/bin/autoxkbmap`
4. the script iterates over the active X11 sessions
5. for each X11 session the script `~/.config/autoxkbmap` is run as the user owning the session

## Contribute

Fell free to fork and create pull requests.
