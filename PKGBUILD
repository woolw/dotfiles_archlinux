# Maintainer: woolw woolw@pm.me
pkgname='woolw-dotfiles-git'
pkgver=r48.c6e1048
pkgrel=1
pkgdesc='mainly hyprland dotfiles with setup script for archlinux'
arch=('any')
url='https://github.com/woolw/dotfiles'
license=('None')
depends=(
   'amd-ucode'
   'blueman'
   'bluez'
   'bluez-utils'
   'brave-bin'
   'brightnessctl'
   'btop'
   'cliphist'
   'discord'
   'file-roller'
   'gamemode'
   'grim'
   'gtk3'
   'gvfs'
   'hyprpaper'
   'jq'
   'kitty'
   'lxappearance'
   'mako'
   'mpv'
   'neovim'
   'network-manager-applet'
   'noto-fonts'
   'noto-fonts-emoji'
   'obsidian'
   'pacman-contrib'
   'pamixer'
   'papirus-icon-theme'
   'pavucontrol'
   'pipewire'
   'polkit-gnome'
   'pyside2'
   'python-requests'
   'qt5-graphicaleffects'
   'qt5-quickcontrols2'
   'qt5-svg'
   'qt5-wayland'
   'qt5ct'
   'qt6-wayland'
   'qt6ct'
   'reflector'
   'rustup'
   'slurp'
   'starship'
   'steam'
   'swappy'
   'syncplay'
   'thunar'
   'thunar-archive-plugin'
   'ttf-baekmuk'
   'ttf-font-awesome'
   'ttf-hanazono'
   'ttf-hannom'
   'ttf-jetbrains-mono-nerd'
   'ttf-linux-libertine'
   'vulkan-radeon'
   'waybar'
   'wireplumber'
   'wl-clipboard'
   'wofi'
   'xdg-desktop-portal-hyprland'
   'xfce4-settings'
   'yt-dlp'
)
makedepends=('stow')
# add AUR packages here
optdepends=(
    'ani-cli'
    'nwg-look-bin'
    'swaylock-effects'
    'wlogout'
) 
source=('dotfiles::git+https://github.com/woolw/dotfiles')
md5sums=('SKIP')

pkgver() {
    cd "$srcdir/${_pkgname}"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd .. && stow -v --no-folding --ignore="PKGBUILD" --ignore="src" --ignore="dotfiles" --ignore="pkg" --ignore "README.md" --ignore ".gitignore" -t $HOME/.config .
    printf "\33[2K\r\033[1;32m%s\033[0m\n" "[4/5] symlinked config files"
}
