# steam-status-tray

On Windows, you can right-click Steam's tray icon to set yourself
**Online**, **Away**, **Invisible** or **Offline**. The Linux Steam
client doesn't have those options.

This adds a tray icon that does, along with the usual shortcuts:

```
● Online
○ Away
○ Invisible
○ Offline
─────────────
Store
Library
Community
Profile
Friends
─────────────
Downloads
Screenshots
Settings
Big Picture
─────────────
Exit Steam
```

The dot shows your current status. It updates every time you open the
menu, even if you changed your status inside Steam.

Left-click the icon to open your Friends list.

The icon only appears while Steam is running. It shows up when you
start Steam and goes away when you exit Steam.

---

## Install

For **CachyOS**, **Arch**, **EndeavourOS**, **Manjaro** and other
Arch-based systems. You need the normal (non-Flatpak) Steam.

### 1. Open a terminal

Press the **Windows key** on your keyboard, type **Konsole** (or
**Terminal**), and press **Enter**.

### 2. Copy and paste these lines

Paste them into the terminal and press **Enter**:

```
sudo pacman -S --needed git base-devel
cd ~
rm -rf steam-status-tray
git clone https://github.com/CausticCatastrophe/steam-status-tray
cd steam-status-tray
makepkg -si
setsid -f steam-status-tray >/dev/null 2>&1
cd ~
rm -rf steam-status-tray
```

The `setsid` line starts the tray right away. The last two lines delete
the downloaded files once it's installed.

- It will ask for **your password**. Typing it won't show anything on
  screen. That's normal. Type it and press Enter.
- If it asks **"Proceed with installation? [Y/n]"**, press **Enter**.

### 3. Start Steam

That's it. The tray is already running, so the icon shows up as soon
as Steam is open. From now on it also starts by itself every time you
log in.

On KDE Plasma, Steam's own tray icon is hidden automatically while this
one runs, so you only see one Steam icon.

---

## Update

Run the same lines from step 2 again. The new version replaces the old
one right away.

## Uninstall

```
sudo pacman -R steam-status-tray
```

This also closes the tray icon, and Steam's own tray icon comes back.

---

## Notes

- **Native Steam only.** The Flatpak version of Steam isn't supported.
- **GNOME** doesn't show tray icons by default. Install the
  *AppIndicator and KStatusNotifierItem Support* extension first.
- The status dot reads an undocumented Steam setting. If a Steam update
  breaks it, changing status from the menu will still work.
- Steam doesn't save **Offline** anywhere the tray can read, so the dot
  only shows Offline when you pick it from this menu. Going offline from
  Steam's own friends window won't move the dot.

## License

MIT
