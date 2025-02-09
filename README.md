# Getting started with [endeavourOS](https://endeavouros.com/) and [i3-wm](https://i3wm.org/)

This guide is my attempt to share a distributable and recyclable setup without compromising the integrity of new users who might want to figure it out on their own, or do things their own way.

eOS is a lightweight distro that ships with a minimum amount of pre-installed apps.

A lot of my application choices are designed to work optimally with the i3 environment, enabling FULL user authority over just about everything, with a minimal and completely tunable UI/UX.

Choose i3-wm from the installer when prompted to choose a desktop environment, and be prepared to do some configuring.

If it seems too complicated for you, *it probably is!*

<div align="right">
 <a href="">
    <img src="https://github.com/TekkadanPlays/Getting-Started-with-eOS/blob/672861f9a3914f75330e2f9821926056d4f9c213/1706459290178581.png">
  </a>
</div>

# Embracing i3 (if it's your first time)

The default ```$mod``` key in eOS is the  /  / ⌘ key. You can launch [rofi](https://github.com/davatorium/rofi) with ```$mod + d``` to launch applications.

Some brief mentions:

- ```$mod + enter``` will quickly open a terminal.

- ```$mod + shift + spacebar``` will snap between tiled and windowed mode. This is especially useful.

- ```$mod + shift + [0-9]``` will quickly move applications between virtual desktops.

You can USE YOUR MOUSE in conjunction with ```$mod``` + ```RMB```! 

> NOTE: your mouse hover determines the *active window!*

<br>

**Keys to use with ```$mod```:**

<br>
<div align="center">
 <a href="">
    <img src="https://i3wm.org/docs/4.0/keyboard-layer1.png">
  </a>
</div>
<br>

**Keys to use with ```$mod + shift```:**

<br>
<div align="center">
 <a href="">
    <img src="https://i3wm.org/docs/4.0/keyboard-layer2.png">
  </a>
</div>
<br>

Start by launching Thunar with rofi: ```$mod + d``` + search ```thunar``` + press ```enter``` to launch.

Navigate to ```~/.config/i3/``` with thunar. Here you can replace ```config.txt``` with my provided [config.txt](https://github.com/TekkadanPlays/Getting-Started-with-eOS/blob/cd9552227b6f4c5f66b166faa395dabeb05afb11/config.txt) file.

If you prefer to configure i3 yourself, I recommend changing the default ```$mod``` key to ```alt```. This is far more comfortable for me.

- Search the ```config``` file for ```set $mod Mod4``` and replace ```Mod4``` with ```Mod1```

Whether you replaced or changed your own config file, press ```$mod + shift + r``` to hot reload the X environment. 

For me, this is ```alt + shift + r```.

# Initialization

- install [paru](https://github.com/Morganamilo/paru) instead of yay:

```
yay -S paru
```

- install [redshift](https://github.com/jonls/redshift), [terminus-font](https://files.ax86.net/terminus-ttf/), and [neofetch](https://github.com/dylanaraps/neofetch) with paru:

```
paru -S redshift terminus-font neofetch
```

> NOTE: add ```neofetch``` to end of ```~/.bashrc``` to start it each time a terminal is launched!

You can also overwrite ```~/.config/neofetch/``` with a [custom theme](https://github.com/chick2d/neofetch-themes). I use [papirus](https://github.com/chick2d/neofetch-themes/blob/main/normal/papirus.conf)!

- install [ranger](https://github.com/ranger/ranger) and [qutebrowser](https://qutebrowser.org/): 

```
paru -S ranger qutebrowser
```
*Goodbye, thunar!*

- A few other small apps I use: [zim-wiki](https://zim-wiki.org/), [flameshot](https://flameshot.org/), [galculator](http://galculator.mnim.org/)

```
paru -S zim flameshot galculator
```

I also particularly enjoy [cmatrix](https://github.com/abishekvashok/cmatrix): 

```
paru -S cmatrix
```

<div align="center">
 <a href="">
    <img src="https://github.com/abishekvashok/cmatrix/blob/master/data/img/capture_orig.gif">
  </a>
</div>

For gaming:
```
paru -S lutris wine
```

For max refresh rate (on Nvidia cards) use the ```Nvidia X Server Settings``` application. (it comes preinstalled)

As of ~2025, you will also need to run ```nvidia -o --32``` and reboot.
