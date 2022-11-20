# dwm - dynamic window manager

This is my own fork of dwm, an extremely fast, small, and dynamic window manager for X.

# Patches

I've applied the following patches:

- [scratchpad](https://dwm.suckless.org/patches/scratchpad/) : allows you to spawn or restore a floating terminal window
- [stacker](https://dwm.suckless.org/patches/stacker/) : change focus and move windows using Mod+j/k
- [swallow](https://dwm.suckless.org/patches/swallow/) : prevents screen cluttering by hiding terminals from which GUIs are started (and restore terminal when closed)
- [warp](https://dwm.suckless.org/patches/warp/) : center the mouse to the focused window
- [deck](https://dwm.suckless.org/patches/deck/) : layout which applies the monocle-layout only to the clients in the stack
- [bottomstack](https://dwm.suckless.org/patches/bottomstack/) : layout which puts master at the top and the stack at the bottom
- [xresources](https://dwm.suckless.org/patches/xresources) : load font and colors from ~/.Xresources

# Installation

```sh
$ make
$ sudo make install
```

Add the following line to your .xinitrc to start dwm using startx:

```sh
# Using an infinite loop to restart dwm when the "quit" keybinding is used
while true
do
    dwm > "$HOME/.dwm.logs" 2>&1
done
```
