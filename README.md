# dotfiles

### Install

```bash
git clone git@github.com:lazywa/dotfiles.git
cp -r dotfiles/* ~/.config/
cp dotfiles/.zshrc ~/
```

### Install some packages

```bash
yay -S alactirry kitty
yay -S waybar swaybg swaylock swayidle wlogout
yay -S mako kanshi xfce-polkit network-manager-applet
yay -S ranger exa brightnessctl rofi-lbonn-wayland-git
yay -S pavucontrol blueberry blueman
```

### Install Nerd Fonts & icon theme

```bash
yay -S nerd-fonts-cascadia-code nerd-fonts-jetbrains-mono nerd-fonts-robotomono
yay -S oranchelo-icon-theme
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
gsettings set org.cinnamon.desktop.default-applications.terminal exec alacritty
```

### Setting backlight

```bash
yay -S brightnessctl

# use
brightnessctl set 5%-
brightnessctl set 5%+
```

### Setting themes

See [catppuccin](https://github.com/catppuccin/catppuccin)

- [alacritty](https://github.com/catppuccin/alacritty)
- [kitty](https://github.com/catppuccin/kitty)
- [rofi](https://github.com/catppuccin/rofi)
- [mako](https://github.com/catppuccin/mako)
