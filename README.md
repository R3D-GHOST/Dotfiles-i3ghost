# Dotfiles-i3ghost
# update

sudo apt update

# Picom 

sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev  libpcre2-dev  libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

git clone https://github.com/ibhagwan/picom.git

cd picom

git submodule update --init --recursive

meson --buildtype=release . build

ninja -C build

sudo ninja -C build install

cd ..

# Polybar 

sudo apt install bison flex libstartup-notification0-dev check autotools-dev libpango1.0-dev librsvg2-bin librsvg2-dev libcairo2-dev libglib2.0-dev libxkbcommon-dev libxkbcommon-x11-dev libjpeg-dev

# Kitty

sudo apt install kitty

# Kitty Config

# color.ini

cursor_shape          Underline
cursor_underline_thickness 1
window_padding_width  20

# Special
foreground #a9b1d6
background #1a1b26

# Black
color0 #414868
color8 #414868

# Red
color1 #f7768e
color9 #f7768e

# Green
color2  #73daca
color10 #73daca

# Yellow
color3  #e0af68
color11 #e0af68

# Blue
color4  #7aa2f7
color12 #7aa2f7

# Magenta
color5  #bb9af7
color13 #bb9af7

# Cyan
color6  #7dcfff
color14 #7dcfff

# White
color7  #c0caf5
color15 #c0caf5

# Cursor
cursor #c0caf5
cursor_text_color #1a1b26

# Selection highlight
selection_foreground #7aa2f7
selection_background #28344a


----------------------------------------------------------------------------------
----------------------------------------------------------------------------------

# Kitty.conf

enable_audio_bell no

include color.ini

font_family      Cartograph CF Italic
font_size 11

disable_ligatures never

url_color #fff

url_style curly

shell zsh



-------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------



# Wallpaper OPT 1

sudo apt install feh

feh --bg-fill $HOME/

# Wallpaper OPT 2

sudo apt install nitrogen

# Install oh-my-bash

sudo apt install zsh
 
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)

# Install Powerlevel10k

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

