# Arch Rice (Nord Theme)

A beautiful and automated Arch Linux rice featuring the Nord color scheme with Hyprland compositor. This repository provides a one-command installation script to set up a complete, customized desktop environment.

![Nord Theme](https://img.shields.io/badge/Theme-Nord-5E81AC?style=flat-square)
![Compositor](https://img.shields.io/badge/Compositor-Hyprland-00A6FB?style=flat-square)
![Shell](https://img.shields.io/badge/Shell-Zsh-89E051?style=flat-square)

## 🎨 Features

- **Hyprland Wayland Compositor** - Modern GPU-accelerated window manager with all tools designed for the hyprland ecosistem.
- **SDDM Display Manager** - Elegant login screen
- **Kitty Terminal** - GPU-accelerated terminal emulator
- **Eww Widgets** - Customizable desktop widgets and panels
- **Complete Toolset** - Includes file manager (yazi), browser (zen-browser), editor (neovim), and more
- **Nord Color Scheme** - Beautiful, arctic-inspired color palette

## 📦 What's Included

### Core Components
- Hyprland compositor with utilities (hypridle, hyprlock, hyprshot, hyprpaper, hyprlauncher)
- SDDM display manager
- Mako notification daemon
- Eww widgets for status bar and desktop info

### Applications
- **Terminal**: Kitty with oh-my-posh prompt
- **File Manager**: Yazi (terminal-based)
- **Editor**: Neovim
- **Browser**: Zen Browser
- **Media Player**: MPV
- **System Info**: Fastfetch

### Utilities
- Audio: PipeWire, WirePlumber, pavucontrol
- Bluetooth: bluez, bluez-utils
- CLI Tools: fzf, lsd, bat, zoxide, ripgrep
- Clipboard: wl-clipboard

## 🚀 Installation

### Prerequisites
- Fresh Arch Linux installation
- Internet connection
- Git installed (`sudo pacman -S git`)

### Quick Install

1. Clone this repository:
```bash
git clone https://github.com/yourusername/ArchRice.git
cd ArchRice
```

2. Make the install script executable:
```bash
chmod +x install
```

3. Run the installation script:
```bash
./install
```

The script will:
1. Update your system
2. Install yay AUR helper (if not present)
3. Set up bluetooth and audio services
4. Prompt for network configuration (optional)
5. Prompt to change default shell to zsh (optional)
6. Install all packages from `packages.txt`
7. Create necessary directories in your home folder
8. Copy configuration files and wallpapers
9. Enable SDDM

### Post-Installation

After the script completes, reboot your system:
```bash
reboot
```

You'll be greeted by the SDDM login screen. Log in to enjoy your new rice!

## ⚙️ Customization

### Modifying Packages

Edit `packages.txt` to add or remove packages before installation. Lines starting with `#` are comments.

### Configuration Files

After installation, all config files are located in `~/.config/`. Feel free to customize all configurations to your liking.

### Wallpapers

Wallpapers are installed to `~/images/wallpapers/`. You can add your own or change the active wallpaper through Hyprpaper configuration.

## 🔧 Troubleshooting

### Script fails during package installation
- Check your internet connection
- Try running: `sudo pacman -Sy archlinux-keyring && sudo pacman -Syu`
- Re-run the install script

### SDDM doesn't start
- Check status: `systemctl status sddm`
- Enable manually: `sudo systemctl enable --now sddm.service`

### Audio not working
- Verify services: `systemctl --user status pipewire.service pipewire-pulse.service wireplumber.service`
- Restart services: `systemctl --user restart pipewire.service pipewire-pulse.service wireplumber.service`

## 🎯 Optional Configurations

During installation, you'll be prompted for:

1. **Network Manager**: Installs NetworkManager for easier network configuration
2. **Zsh Shell**: Changes your default shell from bash to zsh

Both are recommended for the full experience.

## 📝 Credits

Created by **Dtar380**

Inspired by the Nord color scheme and the [r/unixporn](https://www.reddit.com/r/unixporn/) community.

## 📄 License

This project is licensed under the MIT License. Users are free to:
- ✅ Use this rice for personal or commercial purposes
- ✅ Modify and customize the configuration to suit your needs
- ✅ Distribute copies with proper attribution
- ✅ Use as a base for your own projects

For full license details, see the [LICENSE](LICENSE) file.

---

**Enjoy your new Arch Rice!** 🎉
