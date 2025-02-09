# Intro

This guide is my attempt to share a distributable and recyclable setup without compromising the integrity of new users who might want to figure it out on their own, without copying my dotfiles.

A lot of my application choices are designed to work optimally with the i3 environment, enabling FULL user authority over just about everything.

If it seems too complicated for you, it probably is.

<br>
<div align="right">
 <a href="">
    <img src="https://github.com/TekkadanPlays/eOS-Dotfiles/blob/main/1706459290178581.png">
  </a>
</div>
  
# Getting Started with [endeavourOS](https://endeavouros.com/) and [i3-wm](https://i3wm.org/)

eOS is a lightweight distro that ships with a minimum amount of pre-installed apps.

Be sure to choose i3-wm from the installer when prompted to choose a desktop environment.

Be prepared to do some configuring!

# Coping with i3 (if it's your first time)

The default ```$mod``` key is the /⌘ key. You can launch [rofi](https://github.com/davatorium/rofi) with ```$mod + d``` to launch applications.

> NOTE: ```$mod + enter``` will quickly open a terminal.

Start by launching Thunar with dmenu: ```$mod + d``` + search ```thunar``` + press ```enter``` to launch.

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

- install [ranger](https://github.com/ranger/ranger) and [qutebrowser](https://qutebrowser.org/): 

```
paru -S ranger qutebrowser
```
*Goodbye, thunar!*

A few other small apps I use: 

```
paru -S zim flameshot picom drawing galculator
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
