<div align="center">

# ◈ AetherShift

### A wallpaper-driven Hyprland environment that changes with you.

<br>

[![Arch Linux](https://img.shields.io/badge/ARCH-LINUX-1793D1?style=for-the-badge&logo=archlinux&logoColor=white)](https://archlinux.org/)
[![Hyprland](https://img.shields.io/badge/HYPRLAND-WAYLAND-58E1FF?style=for-the-badge&logo=wayland&logoColor=111827)](https://hypr.land/)
[![Quickshell](https://img.shields.io/badge/QUICKSHELL-QML-7C3AED?style=for-the-badge&logo=qt&logoColor=white)](https://quickshell.org/)
[![Matugen](https://img.shields.io/badge/MATUGEN-ADAPTIVE_THEMES-A78BFA?style=for-the-badge&logo=materialdesign&logoColor=white)](https://github.com/InioX/matugen)
[![Status](https://img.shields.io/badge/STATUS-PERSONAL_BUILD-111827?style=for-the-badge)](#-before-installing)

<br>

**AetherShift** is my personal Arch Linux and Hyprland environment.

It combines adaptive wallpaper-based colours, a custom Quickshell desktop shell, glass Rofi menus, media controls, gaming tools, system utilities and workflow automation into one cohesive daily-driver setup.

<br>

> Change the wallpaper.  
> Shift the atmosphere.  
> Keep the workflow.

<br>

[Preview](#-preview) •
[Features](#-features) •
[Components](#-components) •
[Installation](#-installation) •
[Keybinds](#-keybinds) •
[Credits](#-credits)

</div>

<br>

---

## ✦ Preview

<div align="center">

<img width="100%" alt="AetherShift Hyprland desktop" src="https://github.com/user-attachments/assets/412dd6e1-b740-4820-805f-3772f5243c95" />

<br><br>

<img width="49%" alt="AetherShift glass action menu" src="https://github.com/user-attachments/assets/57e7061a-b955-413d-9c15-d139ac472c9d" />
<img width="49%" alt="AetherShift music panel" src="https://github.com/user-attachments/assets/4ee75899-b307-4e3b-9927-ed54bdf67570" />

</div>

<br>

---

## ✦ What Is AetherShift?

AetherShift began as a personal fork inspired by
[Vroomies](https://github.com/maxchennn/vroomies) by
[maxchennn](https://github.com/maxchennn).

It has since grown into a larger daily-driver environment with its own:

- Wallpaper-driven theme system
- Custom scripts and utilities
- Glass application menus
- Gaming and performance controls
- Screenshot and recording workflow
- Snapshot and restoration tools
- Maintenance and repair systems
- Productivity helpers
- Audio-device shortcuts
- Personal workflow integrations

This repository contains the configuration files behind that environment.

It is designed primarily for my own system, but it can also be used as a reference, starting point or source of individual components for another Hyprland setup.

<br>

---

## ✦ Design Philosophy

AetherShift is built around three ideas.

### Adaptive

The visual identity should come from the wallpaper rather than from one permanently hardcoded palette.

### Functional

Every menu, panel and animation should serve a real purpose instead of existing only for screenshots.

### Recoverable

Experimenting with a rice should not mean losing a working configuration. Repair scripts, backups and snapshots are treated as part of the desktop itself.

<br>

---

## ✦ Theme Pipeline

```text
┌─────────────────┐
│    Wallpaper    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│     Matugen     │
│ Colour analysis │
└────────┬────────┘
         │
         ├──────────────┬──────────────┬──────────────┐
         ▼              ▼              ▼              ▼
   Quickshell          Rofi           Kitty        Hyprland
   panels and UI    glass menus    terminal theme   borders
```

Wallpapers are stored in:

```bash
~/Pictures/visions
```

Selecting a wallpaper can regenerate colours for:

- Quickshell
- Rofi
- Kitty
- Hyprland borders and effects
- Wallpaper menus
- Supporting scripts and widgets

Main theme controls:

```text
SUPER + Shift + A    Open wallpaper and theme picker
SUPER + Ctrl + A     Apply a random adaptive theme
```

An optional boot-shuffle script can also apply a random wallpaper and colour scheme when Hyprland starts.

<br>

---

## ✦ Features

### Adaptive desktop

- Wallpaper-derived colour palettes
- Coordinated colours across desktop components
- Animated wallpaper transitions
- Random theme switching
- Generated glass-menu styling

### Quickshell environment

- Vertical workspace bar
- Workspace indicators
- Adaptive foreground and accent colours
- MPRIS media integration
- Wallpaper-picker integration
- Compact music panel
- Desktop information widgets

### Glass menus

- Central category-based action menu
- Adaptive borders and highlights
- Application launcher
- Theme and wallpaper controls
- System-management actions
- Audio and media shortcuts
- Screenshot and recording tools
- Gaming controls
- Maintenance and backup actions
- Power controls

### Gaming workflow

- One-key gaming mode
- Dedicated gaming profile
- Reduced visual effects while gaming
- MangoHud support
- GameMode support
- Performance-oriented workspace controls
- CS2 troubleshooting profile

### Desktop utilities

- Screenshot editor workflow
- Screen recording
- Drop-down terminal
- Floating system monitor
- Information centre
- Welcome and system-status popup
- Notes and todo menu
- Focus timer
- Caffeine mode
- Display blanking
- Power menu

### Recovery and maintenance

- Rice repair script
- Snapshot and restore menu
- Configuration backups
- Package update shortcuts
- Pacman cache maintenance
- Orphan-package checks
- Journal cleanup
- Rice health checks
- GitHub dotfiles export

<br>

---

## ✦ Components

| Component | Role |
|:--|:--|
| **Hyprland** | Wayland compositor and window management |
| **Quickshell** | Main desktop shell, panels and widgets |
| **Matugen** | Wallpaper-based colour generation |
| **Rofi** | Glass application and action menus |
| **Kitty** | Terminal emulator |
| **SwayNC** | Notifications and notification centre |
| **awww** | Wallpaper daemon and transitions |
| **PipeWire** | Audio routing |
| **Playerctl** | MPRIS media control |
| **Cava** | Audio visualisation |
| **MangoHud** | Gaming performance overlay |
| **GameMode** | Gaming performance integration |
| **Grim** | Wayland screenshots |
| **Slurp** | Region selection |
| **Swappy** | Screenshot editing |
| **wf-recorder** | Screen recording |
| **btop** | System monitoring |
| **Fastfetch** | System information |

<br>

---

## ✦ Repository Layout

```text
aethershift-hyprland/
├── .config/
│   ├── MangoHud/       # Gaming overlay configuration
│   ├── cava/           # Audio visualiser
│   ├── fastfetch/      # System-information layout
│   ├── hypr/           # Hyprland configuration and scripts
│   ├── kitty/          # Terminal configuration
│   ├── matugen/        # Adaptive colour templates
│   ├── quickshell/     # Desktop shell and QML components
│   ├── rofi/           # Launchers and glass menus
│   └── swaync/         # Notification styling
├── .gitignore
├── README.md
└── SYSTEM-INFO.txt
```

<br>

---

## ✦ Before Installing

> [!IMPORTANT]
> AetherShift is a personal configuration repository, not a universal Hyprland installer.

The configuration contains assumptions based on my own setup, including:

- Arch Linux
- Hyprland
- PipeWire
- NetworkManager
- NVIDIA graphics
- Specific monitor names
- Specific audio-device names
- Personal directory paths
- My preferred applications and keybinds

You should read the configuration and installation steps before copying anything.

At minimum, expect to adjust:

- Monitor names
- Monitor resolutions and refresh rates
- Audio-device names
- Wallpaper paths
- GPU-related settings
- Keyboard layout
- Default applications
- User-specific paths
- Quickshell monitor targeting

<br>

---

## ✦ Requirements

### Base system

- Arch Linux or an Arch-based distribution
- A working Hyprland installation
- NetworkManager
- PipeWire and WirePlumber
- A regular non-root user
- An AUR helper such as `yay`

### Fonts

AetherShift expects a Nerd Font, particularly JetBrains Mono Nerd Font.

```bash
sudo pacman -S --needed \
  ttf-jetbrains-mono-nerd \
  noto-fonts \
  noto-fonts-emoji
```

Broken or missing icons usually indicate that the expected font is not installed.

<br>

---

## ✦ Installation

### 1. Install the main packages

```bash
sudo pacman -S --needed \
  hyprland \
  xdg-desktop-portal \
  xdg-desktop-portal-hyprland \
  xdg-desktop-portal-gtk \
  pipewire \
  pipewire-pulse \
  wireplumber \
  networkmanager \
  kitty \
  dolphin \
  firefox \
  rofi-wayland \
  swaync \
  swayidle \
  grim \
  slurp \
  swappy \
  wl-clipboard \
  cliphist \
  hyprpicker \
  wf-recorder \
  playerctl \
  pamixer \
  pavucontrol \
  bluez \
  bluez-utils \
  blueman \
  flatpak \
  btop \
  fastfetch \
  gamemode \
  mangohud \
  vulkan-tools \
  steam \
  git \
  rsync \
  imagemagick \
  curl \
  libnotify \
  pacman-contrib
```

Some packages may vary depending on your enabled repositories.

### 2. Install the adaptive-shell packages

Using `yay`:

```bash
yay -S --needed \
  quickshell-git \
  matugen-bin \
  awww-git
```

AUR package names can change over time. Search the AUR when one of the listed packages is unavailable.

### 3. Clone AetherShift

```bash
cd ~
git clone https://github.com/Aetherelic/aethershift-hyprland.git
cd aethershift-hyprland
```

### 4. Back up existing configurations

```bash
BACKUP_DIR="$HOME/.config-backups/aethershift-$(date +%Y%m%d-%H%M%S)"

mkdir -p "$BACKUP_DIR"

for directory in \
  hypr \
  quickshell \
  rofi \
  kitty \
  matugen \
  swaync \
  fastfetch \
  MangoHud \
  cava
do
  if [ -e "$HOME/.config/$directory" ]; then
    cp -a "$HOME/.config/$directory" "$BACKUP_DIR/"
  fi
done
```

The backup will be stored under:

```bash
~/.config-backups/
```

### 5. Copy the configuration

```bash
mkdir -p ~/.config
rsync -a .config/ ~/.config/
```

Make the included scripts executable:

```bash
find ~/.config/hypr/scripts \
  -type f \
  \( -name '*.sh' -o -name '*.py' \) \
  -exec chmod +x {} +

chmod +x \
  ~/.config/quickshell/components/wall/wall.sh \
  2>/dev/null || true
```

### 6. Create the required folders

```bash
mkdir -p \
  ~/Pictures/visions \
  ~/Pictures/Screenshots \
  ~/Videos/Recordings \
  ~/Documents/Aetherelic
```

Place your wallpapers inside:

```bash
~/Pictures/visions
```

High-resolution wallpapers are strongly recommended because they become the visual foundation of the whole desktop.

### 7. Select an initial wallpaper

Replace `YOUR_WALLPAPER.png` with an existing file:

```bash
ln -sf \
  "$HOME/Pictures/visions/YOUR_WALLPAPER.png" \
  "$HOME/.config/hypr/current_wallpaper"
```

### 8. Generate the initial themes

```bash
~/.config/hypr/scripts/generate-rofi-glass-theme.py \
  2>/dev/null || true

~/.config/hypr/scripts/generate-rofi-theme.py \
  2>/dev/null || true

~/.config/hypr/scripts/generate-hypr-theme.py \
  2>/dev/null || true

~/.config/hypr/scripts/generate-kitty-theme.py \
  2>/dev/null || true
```

Apply the selected wallpaper through the Quickshell wallpaper script:

```bash
bash \
  ~/.config/quickshell/components/wall/wall.sh \
  ~/.config/hypr/current_wallpaper
```

### 9. Enable supporting services

Enable Bluetooth when required:

```bash
sudo systemctl enable --now bluetooth.service
```

Start the user audio services:

```bash
systemctl --user enable --now \
  pipewire \
  pipewire-pulse \
  wireplumber
```

Restart the desktop portals:

```bash
systemctl --user restart \
  xdg-desktop-portal \
  xdg-desktop-portal-hyprland \
  xdg-desktop-portal-gtk
```

### 10. Check the configuration

```bash
hyprctl reload
hyprctl configerrors
```

No output from `hyprctl configerrors` means Hyprland did not detect a configuration error.

<br>

---

## ✦ Personalisation

### Monitor configuration

Find your monitor names:

```bash
hyprctl monitors
```

Then inspect the Hyprland configuration:

```bash
nano ~/.config/hypr/hyprland.conf
```

The original setup may contain references to a monitor such as:

```text
DP-2
```

Your outputs may instead be named something like:

```text
DP-1
HDMI-A-1
eDP-1
```

Also inspect Quickshell files that may contain monitor targeting:

```text
~/.config/quickshell/components/Bar/bar.qml
~/.config/quickshell/components/MusicPanel.qml
```

### Audio devices

The included helper scripts were designed around:

```text
Output: Astro A50 Game
Input:  Fifine Microphone
```

Find your own device names with:

```bash
wpctl status
```

Then edit:

```text
~/.config/hypr/scripts/audio-game-output.sh
~/.config/hypr/scripts/audio-fifine-input.sh
```

### Default applications

Review the Hyprland configuration and action-menu scripts for references to applications such as:

- Kitty
- Dolphin
- Firefox
- Vesktop
- Steam
- btop

Replace them with your preferred applications where necessary.

<br>

---

## ✦ Keybinds

| Keybind | Action |
|:--|:--|
| `SUPER + F1` | Open the main action menu |
| `SUPER + Enter` | Open terminal |
| `SUPER + Shift + Enter` | Open file manager |
| `SUPER + Q` | Close active window |
| `SUPER + F` | Toggle fullscreen |
| `SUPER + Shift + F` | Open Firefox |
| `SUPER + Shift + A` | Open wallpaper and theme picker |
| `SUPER + Ctrl + A` | Apply a random adaptive theme |
| `SUPER + F12` | Toggle gaming mode |
| `SUPER + G` | Enter gaming profile |
| `SUPER + Shift + G` | Leave gaming profile |
| `Print` | Capture an area and open the editor |
| `SUPER + Print` | Capture the full screen |
| `SUPER + I` | Open information centre |
| `SUPER + W` | Open welcome and system-status popup |
| `SUPER + Shift + M` | Open maintenance menu |
| `SUPER + Shift + B` | Open snapshot and restore menu |
| `SUPER + Shift + R` | Repair and refresh the rice |
| `SUPER + K` | Open notes and todo menu |
| `SUPER + Shift + K` | Open focus timer |
| `SUPER + Shift + C` | Toggle caffeine mode |
| `SUPER + Ctrl + Z` | Turn displays off |
| `SUPER + Shift + L` | Open power menu |
| `SUPER + Ctrl + B` | Export keybind cheat sheet |
| `SUPER + Ctrl + D` | Export GitHub dotfiles |

A full keybind reference can be exported to:

```bash
~/Documents/Aetherelic/AETHERELIC-KEYBINDS.md
```

<br>

---

## ✦ Main Action Menu

Open the action menu with:

```text
SUPER + F1
```

The menu is divided into functional categories:

```text
Apps
Rice / Theme
System
Audio / Media
Screenshots / Recording
Gaming
Notes / Info
Maintenance / Backup
Power
```

Its colours, borders and highlights are generated from the current wallpaper.

<br>

---

## ✦ Gaming Mode

Toggle gaming mode with:

```text
SUPER + F12
```

Gaming mode attempts to reduce desktop overhead by disabling or reducing effects such as:

- Blur
- Transparency
- Animations
- Non-essential visual processes

The dedicated gaming profile can be controlled with:

```text
SUPER + G            Enter gaming profile
SUPER + Shift + G    Leave gaming profile
```

Basic Steam launch option:

```text
gamemoderun %command%
```

With MangoHud:

```text
mangohud gamemoderun %command%
```

Test without MangoHud when a game has problems with Vulkan overlays.

<br>

---

## ✦ Screenshots and Recording

### Area screenshot

```text
Print
```

### Full screenshot

```text
SUPER + Print
```

The workflow uses:

```text
grim → slurp → swappy → wl-copy
```

Screenshots are stored in:

```bash
~/Pictures/Screenshots
```

Screen recording uses `wf-recorder` and can be accessed through:

```text
SUPER + F1
└── Screenshots / Recording
```

Recordings are stored in:

```bash
~/Videos/Recordings
```

<br>

---

## ✦ Repair System

AetherShift includes a repair script for refreshing the main desktop components.

Run it with:

```text
SUPER + Shift + R
```

Or manually:

```bash
bash ~/.config/hypr/scripts/repair-rice.sh
```

The repair process can refresh:

- Quickshell
- Wallpaper daemon
- SwayNC
- Adaptive themes
- Audio defaults
- Hyprland configuration

<br>

---

## ✦ Snapshots

Open the snapshot and restore menu with:

```text
SUPER + Shift + B
```

Snapshots are stored in:

```bash
~/Aetherelic-Rice-Snapshots
```

This allows experimental changes to be reverted without rebuilding the entire environment manually.

<br>

---

## ✦ Maintenance

Open the maintenance menu with:

```text
SUPER + Shift + M
```

Available actions include:

- Check for package updates
- Update the system
- Clean the Pacman cache
- List orphan packages
- Remove orphan packages
- Clean journal logs
- Run a rice health check

Review every maintenance action before confirming it.

<br>

---

## ✦ Productivity Tools

### Notes and todo

```text
SUPER + K
```

### Focus timer

```text
SUPER + Shift + K
```

Personal productivity files are stored in:

```bash
~/Documents/Aetherelic
```

### Drop-down terminal

```text
SUPER + key above Tab
```

### Floating system monitor

```text
SUPER + Shift + key above Tab
```

<br>

---

## ✦ Safe Idle and Caffeine

The current configuration uses display blanking rather than an automatic lock workflow.

```text
SUPER + Shift + C    Toggle caffeine mode
SUPER + Ctrl + Z     Turn displays off
```

> [!WARNING]
> This configuration may not automatically lock your session.

Anyone using AetherShift on a shared or portable computer should review the idle configuration and add a secure lock screen appropriate for their system.

<br>

---

## ✦ Troubleshooting

### Hyprland reports configuration errors

```bash
hyprctl configerrors
```

Inspect the file and line reported by Hyprland.

### Quickshell does not start

```bash
pkill quickshell 2>/dev/null || true

QML_XHR_ALLOW_FILE_READ=1 \
  quickshell --path ~/.config/quickshell/shell.qml
```

### Wallpaper does not apply

```bash
pkill awww-daemon 2>/dev/null || true
awww-daemon &
```

Then apply the current wallpaper:

```bash
awww img \
  ~/.config/hypr/current_wallpaper \
  --transition-type fade \
  --transition-duration 1.2 \
  --resize crop
```

### Rofi colours look incorrect

```bash
~/.config/hypr/scripts/generate-rofi-glass-theme.py
```

### Kitty colours do not update

```bash
~/.config/hypr/scripts/generate-kitty-theme.py
```

Open a new Kitty window after regenerating the theme.

### Audio uses the wrong device

```bash
wpctl status
```

Set the correct device manually:

```bash
wpctl set-default DEVICE_ID
```

Then update the included audio helper scripts.

### Screen sharing does not work

Restart the desktop portals:

```bash
systemctl --user restart \
  xdg-desktop-portal \
  xdg-desktop-portal-hyprland \
  xdg-desktop-portal-gtk
```

AetherShift uses Vesktop as the recommended Discord client for this workflow:

```bash
flatpak install flathub dev.vencord.Vesktop
```

<br>

---

## ✦ Known Personal Settings

Some parts of the repository were written specifically for my hardware and workflow.

These include references to:

- Astro A50 audio output
- Fifine microphone input
- NVIDIA graphics
- `DP-2` monitor targeting
- The `aetherelic` username
- Personal document folders
- Personal wallpaper locations

These values are not intended to work unchanged on every computer.

<br>

---

## ✦ Credits

AetherShift is based on and heavily inspired by
[Vroomies](https://github.com/maxchennn/vroomies) by
[maxchennn](https://github.com/maxchennn).

The original project established much of the visual direction, Quickshell foundation and music-player concept that inspired this environment.

Original showcase:

[Blame It on Your Love feat. Vroomies](https://www.reddit.com/r/hyprland/comments/1t8myvg/blame_it_on_your_love_feat_vroomies/)

AetherShift adds my own:

- Adaptive theme scripts
- Glass action menus
- Gaming profiles
- Repair utilities
- Snapshot system
- Maintenance tools
- Recording workflow
- Information popups
- Productivity tools
- Daily-driver customisation

Credit remains with the original authors for their work and inspiration.

<br>

---

## ✦ Disclaimer

AetherShift is provided as a personal dotfiles repository.

It may require substantial editing before it is suitable for another system.

Installing it may overwrite existing configuration files. Always create and verify a backup before copying the repository into `~/.config`.

Use the project as:

- A reference
- A personal fork
- A source of individual components
- A foundation for your own Hyprland environment

Do not treat it as a guaranteed universal installation script.

<br>

---

<div align="center">

<br>

[![AetherShift](https://img.shields.io/badge/AETHERSHIFT-BY_AETHERELIC-7C3AED?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Aetherelic/aethershift-hyprland)
[![Aetherelic](https://img.shields.io/badge/CREATED_BY-AETHERELIC-111827?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Aetherelic)

</div>
