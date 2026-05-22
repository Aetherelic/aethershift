# Adaptive Hyprland Rice

A personal Arch Linux + Hyprland rice based on/forked from **Vroomies** by **maxchennn**.

This started as a Vroomies-inspired setup and was expanded into a full daily-driver Hyprland environment with adaptive theming, Quickshell panels, glass menus, gaming tools, screenshots/recording, system utilities, backup tools, and workflow polish.

---

## Credits

This rice is based on/forked from:

- **Vroomies GitHub repo:**  
  https://github.com/maxchennn/vroomies

- **Original Reddit inspiration:**  
  https://www.reddit.com/r/hyprland/comments/1t8myvg/blame_it_on_your_love_feat_vroomies/

Huge credit to **maxchennn** for the original visual direction, Quickshell setup, Vroomies components, and the music-player concept.

This version, **Aetherelic Hyprland Rice**, is my customized Arch Linux + Hyprland fork with extra scripts, menus, system tools, and personal workflow additions.

---

# Screenshots

<img width="2560" height="1440" alt="screenshot-area-2026-05-13_22-44-52" src="https://github.com/user-attachments/assets/412dd6e1-b740-4820-805f-3772f5243c95" />

<img width="1213" height="898" alt="screenshot-area-2026-05-13_22-45-38" src="https://github.com/user-attachments/assets/57e7061a-b955-413d-9c15-d139ac472c9d" />

<img width="913" height="391" alt="screenshot-area-2026-05-13_22-45-28" src="https://github.com/user-attachments/assets/4ee75899-b307-4e3b-9927-ed54bdf67570" />

---

# What This Rice Adds

This fork keeps the Vroomies/Quickshell aesthetic but adds a lot of extra daily-driver functionality.

## Adaptive Theme System

Wallpapers are stored in:

```bash
~/Pictures/visions
```

When a wallpaper is selected, the rice regenerates colours for:

- Quickshell
- Rofi
- Kitty
- Hyprland borders/glow
- Wallpaper picker
- Random theme switcher

Main theme controls:

```text
SUPER + Shift + A  Wallpaper/theme picker
SUPER + Ctrl + A   Random adaptive theme
```

There is also an optional boot shuffle script that can randomly apply a wallpaper/theme when Hyprland starts.

---

## Quickshell Desktop Shell

The rice uses Quickshell for the main desktop shell.

Includes:

- Vertical side bar
- Workspace indicators
- Adaptive colours
- Music integration through MPRIS
- Wallpaper picker integration
- Small music panel
- Vroomies-style visual language

Main Quickshell folder:

```bash
~/.config/quickshell
```

---

## Glass Rofi Menus

The old flat action menu was rebuilt into a cleaner category-based launcher.

Main menu:

```text
SUPER + F1
```

Categories include:

- Apps
- Rice / Theme
- System
- Audio / Media
- Screenshots / Recording
- Gaming
- Notes / Info
- Maintenance / Backup
- Power

The menu uses an adaptive glass Rofi theme generated from the current wallpaper colours.

---

## Gaming Tools

Added gaming-focused tools:

- Gaming mode
- Gaming workspace/profile
- MangoHud support
- GameMode support
- CS2 troubleshooting profile
- One-key visual/performance toggle

Gaming mode:

```text
SUPER + F12
```

Gaming profile:

```text
SUPER + G          Enter gaming profile
SUPER + Shift + G  Leave gaming profile
```

Gaming mode turns off heavy visuals like blur/transparency/animations and tries to set the CPU governor to performance.

---

## Screenshot and Recording Workflow

Screenshots use:

- `grim`
- `slurp`
- `swappy`
- `wl-copy`

Keybinds:

```text
Print          Area screenshot with editor
SUPER + Print  Full screenshot with editor
```

Screenshots save to:

```bash
~/Pictures/Screenshots
```

Recording uses `wf-recorder` and is available through:

```text
SUPER + F1 → Screenshots / Recording
```

Recordings save to:

```bash
~/Videos/Recordings
```

---

## Vesktop Screenshare Setup

Official Discord was unreliable for screensharing on this Wayland/Hyprland setup.

This rice uses **Vesktop** as the recommended Discord client.

Menu path:

```text
SUPER + F1 → Apps → Vesktop / Discord
```

Vesktop is installed through Flatpak:

```bash
flatpak install flathub dev.vencord.Vesktop
```

---

## Audio Helpers

Added quick scripts for preferred audio defaults:

- Output: Astro A50 Game
- Input: Fifine Microphone

Available from:

```text
SUPER + F1 → Audio / Media
```

Scripts:

```bash
~/.config/hypr/scripts/audio-game-output.sh
~/.config/hypr/scripts/audio-fifine-input.sh
```

You will probably need to edit these if your audio device names are different.

---

## Rice Repair System

A one-key repair script refreshes the main rice components if something breaks.

Keybind:

```text
SUPER + Shift + R
```

It refreshes:

- Quickshell
- Wallpaper daemon
- SwayNC
- Adaptive themes
- Audio defaults
- Hyprland reload

Script:

```bash
~/.config/hypr/scripts/repair-rice.sh
```

---

## Snapshot and Restore System

This rice includes a full snapshot/restore menu.

Keybind:

```text
SUPER + Shift + B
```

Snapshots are saved to:

```bash
~/Aetherelic-Rice-Snapshots
```

This makes it safer to experiment because you can restore a previous working rice.

---

## Maintenance Menu

A maintenance menu was added for system upkeep.

Keybind:

```text
SUPER + Shift + M
```

Includes:

- Check updates
- Update system
- Clean pacman cache
- List orphan packages
- Remove orphan packages
- Clean journal logs
- Rice health check

---

## Info Center

The rice includes a small info center.

Keybind:

```text
SUPER + I
```

Includes:

- Calendar
- Weather
- Now playing
- Network
- Storage
- System summary

---

## Welcome Popup

A compact session popup shows useful system/rice info.

Keybind:

```text
SUPER + W
```

It shows:

- User
- Kernel
- Uptime
- Monitor mode
- GPU
- NVIDIA driver
- Current wallpaper
- Quickshell/SwayNC/wallpaper daemon status

---

## Drop-down Terminal and System Monitor

Added glass terminal popups:

```text
SUPER + key above Tab          Drop-down terminal
SUPER + Shift + key above Tab  Floating btop system monitor
```

Scripts:

```bash
~/.config/hypr/scripts/dropdown-terminal.sh
~/.config/hypr/scripts/dropdown-btop.sh
```

---

## Notes, Todo, and Focus Timer

Simple productivity tools were added.

```text
SUPER + K          Notes/todo menu
SUPER + Shift + K  Focus timer
```

Files are stored in:

```bash
~/Documents/Aetherelic
```

---

## Safe Idle and Caffeine

Hyprlock is currently disabled because it caused unlock issues on this system.

Instead, the rice uses safe idle display blanking.

```text
SUPER + Shift + C  Toggle caffeine
SUPER + Ctrl + Z   Turn screens off
```

This avoids locking the session while still allowing the display to sleep.

---

## Dotfiles Export

The repo itself was generated using the dotfiles export script.

Keybind:

```text
SUPER + Ctrl + D
```

Script:

```bash
~/.config/hypr/scripts/export-dotfiles-github.sh
```

It exports the rice into:

```bash
~/Dotfiles-Aetherelic
```

---

# Keybind Summary

| Keybind | Action |
|---|---|
| `SUPER + F1` | Main action menu |
| `SUPER + Enter` | Terminal |
| `SUPER + Shift + Enter` | File manager |
| `SUPER + Q` | Close active window |
| `SUPER + F` | Fullscreen active window |
| `SUPER + Shift + F` | Firefox |
| `SUPER + Shift + A` | Wallpaper/theme picker |
| `SUPER + Ctrl + A` | Random adaptive theme |
| `SUPER + F12` | Toggle gaming mode |
| `SUPER + G` | Gaming profile |
| `SUPER + Shift + G` | Leave gaming profile |
| `Print` | Area screenshot |
| `SUPER + Print` | Full screenshot |
| `SUPER + I` | Info Center |
| `SUPER + W` | Welcome popup |
| `SUPER + Shift + M` | Maintenance menu |
| `SUPER + Shift + B` | Rice snapshot/restore |
| `SUPER + Shift + R` | Repair/refresh rice |
| `SUPER + K` | Notes/todo |
| `SUPER + Shift + K` | Focus timer |
| `SUPER + Shift + C` | Caffeine toggle |
| `SUPER + Ctrl + Z` | Turn screens off |
| `SUPER + Shift + L` | Power menu |
| `SUPER + Ctrl + B` | Export keybind cheat sheet |
| `SUPER + Ctrl + D` | Export GitHub dotfiles |

A full keybind cheat sheet can be exported to:

```bash
~/Documents/Aetherelic/AETHERELIC-KEYBINDS.md
```

---

# Installation Guide

This repo is a personal rice backup, not a universal installer.

These instructions assume:

- Arch Linux
- Hyprland
- systemd-boot or another working bootloader
- PipeWire audio
- NetworkManager
- A normal user account

You should read through the steps before running them.

---

## 1. Install Base Packages

Install the main packages:

```bash
sudo pacman -S --needed \
  hyprland \
  xdg-desktop-portal \
  xdg-desktop-portal-hyprland \
  xdg-desktop-portal-gtk \
  pipewire \
  pipewire-pulse \
  wireplumber \
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
  github-cli \
  rsync \
  imagemagick \
  curl \
  libnotify \
  pacman-contrib
```

Some packages may not exist on every system depending on enabled repositories.

---

## 2. Install AUR Helper

If you do not already have `yay`:

```bash
cd /tmp
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

---

## 3. Install AUR Packages

Some tools may be from the AUR depending on your setup.

Examples:

```bash
yay -S --needed matugen-bin quickshell
```

Package names can change. If one fails, search:

```bash
yay -Ss matugen
yay -Ss quickshell
```

---

## 4. Install Fonts

This rice expects Nerd Fonts, especially JetBrains Mono Nerd Font.

```bash
sudo pacman -S --needed ttf-jetbrains-mono-nerd noto-fonts noto-fonts-emoji
```

If icons look broken, the font is probably missing.

---

## 5. Clone This Repo

Clone into a temporary location:

```bash
cd ~
git clone https://github.com/Aetherelic/adaptive-hyprland-rice.git
cd aetherelic-hyprland-rice
```

Replace `YOUR_USERNAME` with your GitHub username.

---

## 6. Back Up Existing Configs

Before copying anything, back up your current configs:

```bash
mkdir -p ~/arch-working-backup/pre-aetherelic-install-$(date +%Y-%m-%d_%H-%M)

BACKUP_DIR=~/arch-working-backup/pre-aetherelic-install-$(date +%Y-%m-%d_%H-%M)

cp -a ~/.config/hypr "$BACKUP_DIR/hypr" 2>/dev/null || true
cp -a ~/.config/quickshell "$BACKUP_DIR/quickshell" 2>/dev/null || true
cp -a ~/.config/rofi "$BACKUP_DIR/rofi" 2>/dev/null || true
cp -a ~/.config/kitty "$BACKUP_DIR/kitty" 2>/dev/null || true
cp -a ~/.config/matugen "$BACKUP_DIR/matugen" 2>/dev/null || true
cp -a ~/.config/swaync "$BACKUP_DIR/swaync" 2>/dev/null || true
```

---

## 7. Copy Configs

Copy the rice configs:

```bash
mkdir -p ~/.config

cp -a .config/hypr ~/.config/
cp -a .config/quickshell ~/.config/
cp -a .config/rofi ~/.config/
cp -a .config/kitty ~/.config/
cp -a .config/matugen ~/.config/ 2>/dev/null || true
cp -a .config/swaync ~/.config/ 2>/dev/null || true
cp -a .config/fastfetch ~/.config/ 2>/dev/null || true
cp -a .config/MangoHud ~/.config/ 2>/dev/null || true
cp -a .config/cava ~/.config/ 2>/dev/null || true
```

Make scripts executable:

```bash
chmod +x ~/.config/hypr/scripts/*.sh 2>/dev/null || true
chmod +x ~/.config/hypr/scripts/*.py 2>/dev/null || true
chmod +x ~/.config/quickshell/components/wall/wall.sh 2>/dev/null || true
```

---

## 8. Create Wallpaper Folder

Create the wallpaper folder:

```bash
mkdir -p ~/Pictures/visions
mkdir -p ~/Pictures/Screenshots
mkdir -p ~/Videos/Recordings
mkdir -p ~/Documents/Aetherelic
```

Add wallpapers to:

```bash
~/Pictures/visions
```

Recommended resolution:

```text
2560x1440 minimum
3840x2160 ideal
```

Low-resolution wallpapers will look blurry on a 1440p monitor.

---

## 9. Set Current Wallpaper Symlink

Pick one wallpaper and link it:

```bash
ln -sf ~/Pictures/visions/YOUR_WALLPAPER.png ~/.config/hypr/current_wallpaper
```

Replace `YOUR_WALLPAPER.png` with your actual wallpaper.

If using `.jpg` or `.webp`, adjust the file name.

---

## 10. Generate Themes

Run the theme generators if they exist:

```bash
~/.config/hypr/scripts/generate-rofi-glass-theme.py 2>/dev/null || true
~/.config/hypr/scripts/generate-rofi-theme.py 2>/dev/null || true
~/.config/hypr/scripts/generate-hypr-theme.py 2>/dev/null || true
~/.config/hypr/scripts/generate-kitty-theme.py 2>/dev/null || true
```

If `matugen` is installed, also run the wallpaper script once:

```bash
bash ~/.config/quickshell/components/wall/wall.sh ~/.config/hypr/current_wallpaper
```

---

## 11. Enable Services

Enable Bluetooth if needed:

```bash
sudo systemctl enable --now bluetooth.service
```

Make sure PipeWire is running:

```bash
systemctl --user enable --now pipewire pipewire-pulse wireplumber
```

Restart portals:

```bash
systemctl --user restart xdg-desktop-portal xdg-desktop-portal-hyprland xdg-desktop-portal-gtk
```

---

## 12. Install Vesktop

For Discord/screenshare:

```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install -y flathub dev.vencord.Vesktop
flatpak override --user --filesystem=home dev.vencord.Vesktop
```

Launch with:

```bash
flatpak run dev.vencord.Vesktop
```

---

## 13. Edit Monitor Settings

You must check your monitor names.

Run:

```bash
hyprctl monitors
```

Then edit:

```bash
nano ~/.config/hypr/hyprland.conf
```

Or any monitor-specific included config.

This rice was built around a setup using a main monitor named something like:

```text
DP-2
```

Your monitor name may be different.

If Quickshell appears on the wrong monitor, check files like:

```bash
~/.config/quickshell/components/Bar/bar.qml
~/.config/quickshell/components/MusicPanel.qml
```

and replace hardcoded monitor names if needed.

---

## 14. Edit Audio Device Scripts

This rice includes personal audio scripts for:

```text
Astro A50 Game
Fifine Microphone
```

If you use different devices, edit:

```bash
nano ~/.config/hypr/scripts/audio-game-output.sh
nano ~/.config/hypr/scripts/audio-fifine-input.sh
```

Find your device names with:

```bash
wpctl status
```

---

## 15. Start Hyprland

From TTY:

```bash
Hyprland
```

Once inside Hyprland, reload config:

```bash
hyprctl reload
```

Check errors:

```bash
hyprctl configerrors
```

If nothing prints, the config is clean.

---

# Optional: Auto-start Hyprland After Login

To auto-start Hyprland from TTY1 after login, add this to:

```bash
~/.bash_profile
```

```bash
# Auto-start Hyprland on TTY1
if [ -z "$WAYLAND_DISPLAY" ] && [ "$XDG_VTNR" = "1" ] && [ -z "$SSH_CONNECTION" ]; then
  exec Hyprland
fi
```

---

# Optional: Auto-login to Hyprland

This is less secure because it logs in without typing your password.

Create:

```bash
sudo mkdir -p /etc/systemd/system/getty@tty1.service.d
```

Then:

```bash
sudo tee /etc/systemd/system/getty@tty1.service.d/autologin.conf >/dev/null <<'EOF'
[Service]
ExecStart=
ExecStart=-/usr/bin/agetty --autologin YOUR_USERNAME --noclear %I $TERM
EOF
```

Replace `YOUR_USERNAME` with your username.

Reload systemd:

```bash
sudo systemctl daemon-reload
```

To undo:

```bash
sudo rm -f /etc/systemd/system/getty@tty1.service.d/autologin.conf
sudo systemctl daemon-reload
```

---

# Optional: NVIDIA Notes

This setup was used with an NVIDIA GPU on Wayland.

Useful packages:

```bash
sudo pacman -S --needed nvidia-open nvidia-utils lib32-nvidia-utils
```

For multiple kernels, DKMS may be easier:

```bash
sudo pacman -S --needed nvidia-open-dkms
```

Check NVIDIA:

```bash
nvidia-smi
```

---

# Optional: Steam/GameMode/MangoHud

Install:

```bash
sudo pacman -S --needed steam gamemode mangohud
```

Basic Steam launch option:

```text
gamemoderun %command%
```

For FPS testing:

```text
mangohud gamemoderun %command%
```

For games that crash with Vulkan overlays, test without MangoHud first.

---

# Troubleshooting

## Hyprland Config Errors

Run:

```bash
hyprctl configerrors
```

If errors appear, inspect the mentioned file and line.

---

## Quickshell Not Starting

Run:

```bash
pkill quickshell
QML_XHR_ALLOW_FILE_READ=1 quickshell --path ~/.config/quickshell/shell.qml
```

Check logs:

```bash
tail -80 /tmp/quickshell.log
```

---

## Wallpaper Not Applying

Restart the wallpaper daemon:

```bash
pkill awww-daemon
awww-daemon &
```

Reapply wallpaper:

```bash
awww img ~/.config/hypr/current_wallpaper --transition-type fade --transition-duration 1.2 --resize crop
```

---

## Audio Wrong Device

Check devices:

```bash
wpctl status
```

Then either edit the audio scripts or set manually:

```bash
wpctl set-default DEVICE_ID
```

---

## Rofi Menus Look Broken

Regenerate Rofi theme:

```bash
~/.config/hypr/scripts/generate-rofi-glass-theme.py
```

---

## Kitty Theme Not Updating

Regenerate Kitty theme:

```bash
~/.config/hypr/scripts/generate-kitty-theme.py
```

Open a new Kitty window after regenerating.

---

## Screenshare Not Working

Use Vesktop instead of official Discord:

```bash
flatpak run dev.vencord.Vesktop
```

Also restart portals:

```bash
systemctl --user restart xdg-desktop-portal xdg-desktop-portal-hyprland xdg-desktop-portal-gtk
```

---

## Repair the Rice

Use:

```text
SUPER + Shift + R
```

Or run:

```bash
bash ~/.config/hypr/scripts/repair-rice.sh
```

---

# Known Notes

## Hyprlock Disabled

Hyprlock was disabled because it caused an unlock/re-lock issue on this system.

Current behavior:

- No automatic lock
- Idle only turns screens off
- Caffeine mode can disable idle screen blanking

Hyprlock can be rebuilt later from a minimal safe config.

## Personal Device Names

Some scripts are personalized for:

- Astro A50 headset
- Fifine microphone
- DP-2 monitor
- NVIDIA GPU
- Aetherelic username/workflow

Edit scripts/configs as needed on another machine.

---

# Disclaimer

This is a personal rice, not a universal Hyprland installer.

It may require edits for:

- Monitor names
- Audio devices
- Wallpaper paths
- GPU drivers
- Quickshell monitor targeting
- Usernames
- Installed packages
- Keyboard layout
- Boot/login preferences

Use it as a reference, fork, or backup.

---

# Final Credit

Again, this rice is based on/forked from **Vroomies** by **maxchennn**.

- Vroomies repo:  
  https://github.com/maxchennn/vroomies

- Reddit inspiration:  
  https://www.reddit.com/r/hyprland/comments/1t8myvg/blame_it_on_your_love_feat_vroomies/

This Aetherelic version adds my own adaptive theming, glass menus, gaming tools, repair scripts, snapshots, recording tools, info popups, maintenance workflows, and daily-driver polish.
