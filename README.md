# Dynamic Window Manager

`dwm` is a dynamic window manager for X. It manages windows in tiled, monocle and floating layouts. All of the layouts can be applied dynamically, optimising the environment for the application in use and the task performed.

## Upstream

The upstream development for `dwm` can be found [here](https://git.suckless.org/dwm).

# Patches

- [fullscreen](https://dwm.suckless.org/patches/actualfullscreen/)
- [gaps](https://dwm.suckless.org/patches/vanitygaps/)
- [shiftview](https://dwm.suckless.org/patches/nextprev/)
- [stacker](https://dwm.suckless.org/patches/stacker/)
- [statuscmd](https://dwm.suckless.org/patches/statuscmd/)
- [swallow](https://dwm.suckless.org/patches/swallow/)
- [vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/)
- [xresources](https://dwm.suckless.org/patches/xresources/)

# Arch Linux Install

Download the`PKGBUILD` from this repository and run the following command:

```
makepkg -cf
```

This will create a file that ends in `.pkg.tar.zst`. Then run:

```
sudo pacman -U *.pkg.tar.zst
```

# Regular Install

Download the source code from this repository:

```
git clone https://github.com/hooregi/dwm.git
cd dwm
sudo make clean install
```
