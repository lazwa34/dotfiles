# dotfiles

### Install

```bash
git clone git@github.com:lazywa/dotfiles.git
cp -r dotfiles/* ~/.config/
cp dotfiles/.zshrc ~/
```

### The following packages need to be installed and config

### 
```bash
yay -S alactirry kitty
yay -S waybar swaybg swaylock wlogout
yay -S mako kanshi xfce-polkit network-manager-applet
yay -S ranger exa light rofi-lbonn-wayland-git
yay -S pavucontrol blueberry
```

#### Setting greet
```bash
yay -S greetd greetd-tuigreet
systemctl enable greetd

/etc/greetd/config.toml
-----------------------
[terminal]
# The VT to run the greeter on. Can be "next", "current" or a number
# designating the VT.
vt = 1

# The default session, also known as the greeter.
[default_session]

# `agreety` is the bundled agetty/login-lookalike. You can replace `$SHELL`
# with whatever you want started, such as `sway`.
command = "tuigreet --user-menu --asterisks --cmd wayfire"

# The user to run the command as. The privileges this user must have depends
# on the greeter. A graphical greeter may for example require the user to be
# in the `video` group.
user = "lazywa"
```

#### Setting Nemo
```bash
# Fix open in terminal
gsettings set org.cinnamon.desktop.default-applications.terminal exec kitty
```

### Setting backlight
```bash
yay -S brightnessctl

# use
brightnessctl set 5%-
brightnessctl set 5%+
```
