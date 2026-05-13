# Aetherelic Hyprland Rice

A personal Arch Linux + Hyprland desktop rice based on/forked from the excellent **Vroomies** rice by **maxchennn**.

This setup started from the Vroomies aesthetic and Quickshell structure, then evolved into a fully customized daily-driver environment with adaptive theming, gaming utilities, system menus, screenshots, recording tools, audio helpers, profile modes, backups, and a full action center.

## Credits

This rice is based on/forked from:

- **Vroomies GitHub repo:**  
  https://github.com/maxchennn/vroomies

- **Original Reddit post/inspiration:**  
  https://www.reddit.com/r/hyprland/comments/1t8myvg/blame_it_on_your_love_feat_vroomies/

Huge credit to **maxchennn** for the original Vroomies rice, Quickshell components, visual direction, and the music panel concept.  
My version, **Aetherelic Hyprland Rice**, is a customized fork/personal rebuild made for my own Arch + Hyprland setup.

---

# Overview

Aetherelic Hyprland Rice is a polished desktop environment built around:

- Arch Linux
- Hyprland
- Quickshell
- Rofi
- Kitty
- Matugen
- Awww wallpaper daemon
- SwayNC
- PipeWire/WirePlumber
- Vesktop
- MangoHud/GameMode
- Swappy/grim/slurp
- Custom Bash/Python helper scripts

The goal is to make Hyprland feel like a complete custom desktop environment rather than just a window manager.

---

# Main Features

## Adaptive Wallpaper + Theme System

Wallpapers live in:

```bash
~/Pictures/visions
```

Supported formats:

```text
.jpg
.jpeg
.png
.webp
```

The wallpaper system is tied into `matugen`, so selecting a wallpaper also regenerates adaptive colors used by:

- Quickshell
- Rofi
- Kitty
- Hyprland borders/glow
- Hyprlock config, if re-enabled later
- Wallpaper/theme picker
- Random theme switcher

Keybinds:

```text
SUPER + Shift + A  Wallpaper/adaptive theme picker
SUPER + Ctrl + A   Random adaptive theme
```

The setup also includes a boot theme shuffle script that can randomly choose a wallpaper/theme when Hyprland starts.

---

## Quickshell Bar and Panels

The rice uses Quickshell as the main visual shell layer.

Current Quickshell features include:

- Left-side vertical bar
- Workspace indicators
- Music indicator
- Adaptive colors
- Wallpaper picker integration
- Small music panel
- Launcher support
- Wifi panel components
- Theme-aware styling

The Quickshell configuration lives in:

```bash
~/.config/quickshell
```

Main loader:

```bash
~/.config/quickshell/shell.qml
```

Important components:

```bash
~/.config/quickshell/components/Bar/bar.qml
~/.config/quickshell/components/MusicPanel.qml
~/.config/quickshell/components/wall/wall.sh
~/.config/quickshell/components/Launcher/Sway.qml
~/.config/quickshell/components/Launcher/Luna.qml
```

---

## Music Panel

Credit for the original music-panel idea goes to Vroomies/maxchennn.

The music panel is not a Spotify-specific widget. It uses MPRIS, so it can work with media players that expose MPRIS metadata.

Features:

- Album art
- Track title
- Artist
- Playback state
- Play/pause/next/previous controls
- Adaptive theme colors
- Small floating music panel

Keybind/menu access:

```text
SUPER + M          Music panel toggle
SUPER + F1         Audio / Media → Small music panel
```

---

## Rofi Glass Menus

The original messy action menu has been rebuilt into a clean category-based menu.

Main keybind:

```text
SUPER + F1
```

The menu is split into categories:

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

The Rofi theme is adaptive and glassy:

```bash
~/.config/rofi/aetherelic-glass.rasi
```

The theme generator is:

```bash
~/.config/hypr/scripts/generate-rofi-glass-theme.py
```

---

## Clean Category Action Menu

The main action menu script is:

```bash
~/.config/hypr/scripts/aetherelic-menu.sh
```

It launches the category menu for:

### Apps

- Terminal
- Drop-down terminal
- System monitor
- File manager
- Firefox
- Vesktop/Discord
- Bluetooth manager
- Clipboard history
- Clear clipboard

### Rice / Theme

- Wallpaper picker
- Random adaptive theme
- Repair/refresh rice
- Welcome popup
- Colour picker
- Emoji picker
- Export keybind cheat sheet
- Export GitHub dotfiles

### System

- Info Center
- Rice health check
- Toggle caffeine
- Turn screens off
- Toggle floating
- Center floating window
- Close active window
- Reload Hyprland

### Audio / Media

- Set output to Astro A50 Game
- Set input to Fifine Microphone
- Volume controls
- Media controls
- Small music panel
- Media profile

### Screenshots / Recording

- Area screenshot
- Full screenshot
- Open screenshots folder
- Record area
- Record full screen
- Stop recording
- Open recordings folder
- Recording profile

### Gaming

- Gaming profile
- Leave gaming profile
- Toggle gaming mode
- Fullscreen active window
- Window move/nudge reminders

### Notes / Info

- Notes/todo menu
- Focus timer
- Info Center
- Calendar
- Weather
- Now playing
- Network
- Storage
- System summary

### Maintenance / Backup

- Maintenance menu
- Rice snapshot/restore
- Repair/refresh rice
- Check updates
- Export keybind cheat sheet
- Export GitHub dotfiles
- Open snapshots folder

### Power

- Power menu
- Reboot
- Shutdown
- Logout Hyprland

---

# Keybinds

## Core Window Controls

| Keybind | Action |
|---|---|
| `SUPER + Enter` | Open Kitty terminal |
| `SUPER + Shift + Enter` | Open file manager |
| `SUPER + Q` | Close active window |
| `SUPER + F` | Fullscreen active window |
| `SUPER + Shift + F` | Open Firefox |
| `SUPER + V` | Toggle floating |
| `SUPER + Shift + V` | Center floating window |
| `SUPER + Arrow` | Move focus |
| `SUPER + Shift + Arrow` | Move window |
| `SUPER + Alt + Arrow` | Nudge floating window |

## Main Menus

| Keybind | Action |
|---|---|
| `SUPER + F1` | Main category action menu |
| `SUPER + I` | Info Center |
| `SUPER + W` | Welcome/session popup |
| `SUPER + Shift + M` | Maintenance menu |
| `SUPER + Shift + B` | Rice snapshot/restore menu |
| `SUPER + Shift + R` | Repair/refresh rice |
| `SUPER + Shift + L` | Power menu |

## Theme / Rice

| Keybind | Action |
|---|---|
| `SUPER + Shift + A` | Wallpaper/adaptive theme picker |
| `SUPER + Ctrl + A` | Random adaptive theme |
| `SUPER + Ctrl + P` | Colour picker |
| `SUPER + .` | Emoji picker |

## Terminal / System

| Keybind | Action |
|---|---|
| `SUPER + key above Tab` | Drop-down glass terminal |
| `SUPER + Shift + key above Tab` | Floating btop system monitor |
| `SUPER + K` | Notes/todo menu |
| `SUPER + Shift + K` | Focus timer |
| `SUPER + Shift + C` | Toggle caffeine mode |
| `SUPER + Ctrl + Z` | Turn screens off |

## Screenshots / Recording

| Keybind | Action |
|---|---|
| `Print` | Area screenshot with Swappy editor |
| `SUPER + Print` | Full screenshot with Swappy editor |
| `SUPER + F1 → Screenshots / Recording` | Recording/screenshot tools |

## Gaming

| Keybind | Action |
|---|---|
| `SUPER + F12` | Toggle gaming mode |
| `SUPER + G` | Gaming profile |
| `SUPER + Shift + G` | Leave gaming profile |
| `SUPER + O` | Recording profile |
| `SUPER + Y` | Media profile |

## Export Tools

| Keybind | Action |
|---|---|
| `SUPER + Ctrl + B` | Export keybind cheat sheet |
| `SUPER + Ctrl + D` | Export GitHub-ready dotfiles |

---

# Gaming Mode

Gaming mode disables expensive visuals and switches the system into a more performance-focused state.

Script:

```bash
~/.config/hypr/scripts/gaming-toggle.sh
```

Keybind:

```text
SUPER + F12
```

Gaming mode does:

- Disables Hyprland blur
- Sets opacity to solid
- Disables animations
- Attempts to set CPU governor to performance
- Restores the rice when disabled

Recommended Steam launch option for most games:

```text
gamemoderun %command%
```

For testing FPS/frametimes:

```text
mangohud gamemoderun %command%
```

For CS2 specifically, MangoHud and Steam Overlay may cause instability on some NVIDIA setups, so CS2 is best tested without overlays if crashes occur.

---

# Gaming Profile

The gaming profile is a convenience wrapper around workspace and performance settings.

Keybinds:

```text
SUPER + G          Gaming profile
SUPER + Shift + G  Leave gaming profile
```

Gaming profile:

- Switches to workspace 8
- Enables gaming mode
- Starts Steam if it is not already running

Leaving gaming profile:

- Disables gaming mode
- Returns to workspace 1

Scripts:

```bash
~/.config/hypr/scripts/profile-gaming.sh
~/.config/hypr/scripts/profile-gaming-off.sh
```

---

# Audio Defaults

The setup includes scripts to quickly restore preferred audio devices.

Output:

```text
Astro A50 Game
```

Input:

```text
Fifine Microphone
```

Scripts:

```bash
~/.config/hypr/scripts/audio-game-output.sh
~/.config/hypr/scripts/audio-fifine-input.sh
```

These are also available from:

```text
SUPER + F1 → Audio / Media
```

---

# Vesktop / Discord Screenshare

Official Discord was kept as a backup, but Vesktop is used as the main Discord client because it worked better for screensharing on this Hyprland/Wayland setup.

Vesktop launch option in menu:

```text
SUPER + F1 → Apps → Vesktop / Discord
```

Installed Flatpak:

```text
dev.vencord.Vesktop
```

Reason:

- Better Wayland/Linux screenshare behavior
- Better Discord customization
- More reliable than the official Discord client in this setup

---

# Screenshots

Screenshots use:

- `grim`
- `slurp`
- `swappy`
- `wl-copy`
- `notify-send`

Scripts:

```bash
~/.config/hypr/scripts/screenshot-area.sh
~/.config/hypr/scripts/screenshot-full.sh
```

Keybinds:

```text
Print          Area screenshot with preview/editor
SUPER + Print  Full screenshot with preview/editor
```

Screenshots save to:

```bash
~/Pictures/Screenshots
```

The screenshot is also copied to clipboard after editing.

---

# Screen Recording

Recording uses `wf-recorder`.

Scripts:

```bash
~/.config/hypr/scripts/record-area.sh
~/.config/hypr/scripts/record-full.sh
~/.config/hypr/scripts/record-stop.sh
```

Recordings save to:

```bash
~/Videos/Recordings
```

Available from:

```text
SUPER + F1 → Screenshots / Recording
```

---

# Info Center

The Info Center is a Rofi menu that launches small glass terminal popups.

Keybind:

```text
SUPER + I
```

Script:

```bash
~/.config/hypr/scripts/aetherelic-info-center.sh
```

Includes:

- Calendar
- Weather
- Now playing
- Network
- Storage
- System summary

Individual scripts:

```bash
~/.config/hypr/scripts/popup-calendar.sh
~/.config/hypr/scripts/popup-weather.sh
~/.config/hypr/scripts/popup-nowplaying.sh
~/.config/hypr/scripts/popup-network.sh
~/.config/hypr/scripts/popup-storage.sh
~/.config/hypr/scripts/popup-system.sh
```

---

# Welcome Popup

A compact session popup appears once per day on startup and can be opened manually.

Keybind:

```text
SUPER + W
```

Scripts:

```bash
~/.config/hypr/scripts/aetherelic-welcome.sh
~/.config/hypr/scripts/aetherelic-welcome-launch.sh
~/.config/hypr/scripts/aetherelic-welcome-once.sh
```

It shows:

- Username
- Kernel
- Uptime
- Monitor mode
- GPU
- NVIDIA driver
- Temperature
- Current wallpaper
- Quickshell status
- SwayNC status
- Wallpaper daemon status
- Keybind reminders

---

# Rice Repair System

If the rice visually breaks, the repair script refreshes the main components.

Keybind:

```text
SUPER + Shift + R
```

Script:

```bash
~/.config/hypr/scripts/repair-rice.sh
```

It restarts/regenerates:

- Rofi glass theme
- Rofi adaptive theme
- Hyprland adaptive borders
- Wallpaper daemon
- Current wallpaper
- Quickshell
- SwayNC
- Safe idle
- Audio defaults
- Hyprland reload

---

# Maintenance Menu

Keybind:

```text
SUPER + Shift + M
```

Script:

```bash
~/.config/hypr/scripts/aetherelic-maintenance-menu.sh
```

Includes:

- Check updates
- Update system
- Clean pacman cache
- List orphan packages
- Remove orphan packages
- Clean journal logs
- Open cache folder
- Rice health check

---

# Rice Snapshot / Restore

A full snapshot/restore system is included.

Keybind:

```text
SUPER + Shift + B
```

Main menu:

```bash
~/.config/hypr/scripts/rice-snapshot-menu.sh
```

Snapshot script:

```bash
~/.config/hypr/scripts/rice-create-snapshot.sh
```

Restore script:

```bash
~/.config/hypr/scripts/rice-restore-snapshot.sh
```

Export script:

```bash
~/.config/hypr/scripts/rice-export-latest.sh
```

Snapshots are saved to:

```bash
~/Aetherelic-Rice-Snapshots
```

Exports are saved to:

```bash
~/Aetherelic-Rice-Exports
```

This makes experimenting safer because a working rice can be restored if a config change breaks something.

---

# Notes / Todo / Focus Timer

Keybinds:

```text
SUPER + K          Notes/todo menu
SUPER + Shift + K  Focus timer
```

Files:

```bash
~/Documents/Aetherelic/quick-notes.md
~/Documents/Aetherelic/todo.txt
```

Scripts:

```bash
~/.config/hypr/scripts/aetherelic-notes-menu.sh
~/.config/hypr/scripts/quick-note.sh
~/.config/hypr/scripts/todo-add.sh
~/.config/hypr/scripts/todo-menu.sh
~/.config/hypr/scripts/notes-view.sh
~/.config/hypr/scripts/todo-view.sh
~/.config/hypr/scripts/focus-timer.sh
```

---

# Safe Idle / Caffeine

Hyprlock has been disabled for now because of a lock/unlock issue.  
Instead, this rice uses a safe idle setup that only turns displays off and does not lock the session.

Scripts:

```bash
~/.config/hypr/scripts/safe-idle.sh
~/.config/hypr/scripts/caffeine-toggle.sh
~/.config/hypr/scripts/screen-off.sh
```

Keybinds:

```text
SUPER + Shift + C  Toggle caffeine
SUPER + Ctrl + Z   Turn screens off
```

Caffeine mode disables idle display sleep.

---

# Kitty Terminal

Kitty is themed with a glassy adaptive config.

Config:

```bash
~/.config/kitty/kitty.conf
```

Adaptive theme:

```bash
~/.config/kitty/aetherelic-adaptive.conf
```

Theme generator:

```bash
~/.config/hypr/scripts/generate-kitty-theme.py
```

Features:

- Glassy transparency
- Adaptive colors
- JetBrainsMono Nerd Font
- Padded terminal windows
- Powerline-style tab bar
- Useful tab/window shortcuts

---

# Drop-down Terminal

A floating glass drop-down terminal is included.

Keybind:

```text
SUPER + key above Tab
```

Script:

```bash
~/.config/hypr/scripts/dropdown-terminal.sh
```

There is also a floating btop monitor:

```text
SUPER + Shift + key above Tab
```

Script:

```bash
~/.config/hypr/scripts/dropdown-btop.sh
```

---

# Clipboard Manager

Clipboard history uses `cliphist`.

Available from:

```text
SUPER + F1 → Apps → Clipboard history
```

Scripts:

```bash
~/.config/hypr/scripts/clipboard-picker.sh
~/.config/hypr/scripts/clipboard-clear.sh
```

---

# Bluetooth

Bluetooth is managed with BlueZ/Blueman.

Menu:

```text
SUPER + F1 → Apps → Bluetooth manager
```

Expected packages:

```bash
bluez
bluez-utils
blueman
```

---

# Boot Behavior

The setup uses systemd-boot and starts Hyprland through TTY autologin + `.bash_profile`.

The intent:

```text
PC boots
TTY1 autologin starts
Hyprland launches automatically
```

Hyprland autostart is handled in:

```bash
~/.bash_profile
```

The auto-login override is handled through:

```bash
/etc/systemd/system/getty@tty1.service.d/autologin.conf
```

To disable auto-login, remove:

```bash
sudo rm -f /etc/systemd/system/getty@tty1.service.d/autologin.conf
sudo systemctl daemon-reload
```

---

# Dotfiles Export

The GitHub-ready dotfiles export lives at:

```bash
~/Dotfiles-Aetherelic
```

The export script is:

```bash
~/.config/hypr/scripts/export-dotfiles-github.sh
```

Keybind:

```text
SUPER + Ctrl + D
```

It exports:

```bash
~/.config/hypr
~/.config/quickshell
~/.config/rofi
~/.config/kitty
~/.config/matugen
~/.config/swaync
~/.config/fastfetch
~/.config/MangoHud
~/.config/cava
```

It also creates:

```bash
README.md
.gitignore
SYSTEM-INFO.txt
```

---

# Keybind Cheat Sheet Export

The keybind cheat sheet is exported to:

```bash
~/Documents/Aetherelic/AETHERELIC-KEYBINDS.md
```

Script:

```bash
~/.config/hypr/scripts/export-keybind-cheatsheet.sh
```

Keybind:

```text
SUPER + Ctrl + B
```

---

# Important Folders

```bash
~/.config/hypr
~/.config/quickshell
~/.config/rofi
~/.config/kitty
~/.config/matugen
~/.config/swaync
~/.config/MangoHud
~/.config/cava
~/Pictures/visions
~/Pictures/Screenshots
~/Videos/Recordings
~/Documents/Aetherelic
~/Aetherelic-Rice-Snapshots
~/Dotfiles-Aetherelic
```

---

# Recommended Packages

This rice uses many tools. Important packages include:

```bash
hyprland
quickshell
kitty
rofi-wayland
swaync
swayidle
grim
slurp
swappy
wl-clipboard
cliphist
hyprpicker
wf-recorder
playerctl
pamixer
pavucontrol
pipewire
wireplumber
bluez
bluez-utils
blueman
flatpak
btop
fastfetch
matugen
gamemode
mangohud
vulkan-tools
steam
git
github-cli
rsync
```

Some tools may come from the AUR depending on the system.

---

# Current Known Notes

## Hyprlock Disabled

Hyprlock was temporarily disabled because of a bug where the lock screen repeatedly re-locked or failed to unlock correctly.

Current state:

```text
No automatic lock
Safe idle only turns screens off
Power menu lock option removed
```

Hyprlock can be rebuilt later using a minimal config first.

## CS2 / NVIDIA Stability

CS2 previously crashed with:

```text
VK_ERROR_DEVICE_LOST
NVIDIA Xid 31
```

This appeared to be a CS2/NVIDIA/Vulkan stability issue rather than a rice issue.  
The system now keeps gaming tools available, but CS2 should be tested without MangoHud/Steam Overlay if crashes return.

---

# Restore Notes

This repo is a personal backup, not a universal installer.

Basic restore idea:

```bash
cp -a .config/hypr ~/.config/
cp -a .config/quickshell ~/.config/
cp -a .config/rofi ~/.config/
cp -a .config/kitty ~/.config/
cp -a .config/matugen ~/.config/
cp -a .config/swaync ~/.config/
```

Then reload:

```bash
hyprctl reload
pkill quickshell
QML_XHR_ALLOW_FILE_READ=1 quickshell --path ~/.config/quickshell/shell.qml &
```

Before restoring, always back up the current config:

```bash
mkdir -p ~/arch-working-backup
cp -a ~/.config/hypr ~/arch-working-backup/hypr-before-restore
cp -a ~/.config/quickshell ~/arch-working-backup/quickshell-before-restore
```

---

# Disclaimer

This is a personal Hyprland rice built for my own hardware, monitor layout, audio devices, and workflow.

It may not work out of the box on another system without edits.

Things likely needing adjustment on another machine:

- Monitor names/resolutions
- Audio device names
- Wallpaper paths
- GPU/NVIDIA settings
- Autologin username
- Quickshell screen targeting
- Bluetooth/network device names
- Package availability

---

# Final Credit

Again, this rice is heavily inspired by and forked from **Vroomies** by **maxchennn**.

Original repo:

```text
https://github.com/maxchennn/vroomies
```

Original Reddit inspiration:

```text
https://www.reddit.com/r/hyprland/comments/1t8myvg/blame_it_on_your_love_feat_vroomies/
```

This Aetherelic version is my own customized Arch/Hyprland daily-driver fork with additional scripts, menus, gaming tools, maintenance utilities, adaptive theming, and workflow polish.
