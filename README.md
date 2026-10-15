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
Quit Tray Icon
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

Press the app launcher, type **Konsole** (or **Terminal**), and open it.

### 2. Copy and paste these lines

Paste them into the terminal and press **Enter**:

```
sudo pacman -S --needed git base-devel
cd /tmp
rm -rf steam-status-tray
git clone https://github.com/CausticCatastrophe/steam-status-tray
cd steam-status-tray
makepkg -si
```

- It will ask for **your password**. Typing it won't show anything on
  screen. That's normal. Type it and press Enter.
- If it asks **"Proceed with installation? [Y/n]"**, press **Enter**.

### 3. Start it

Open the app launcher, search for **Steam Status Tray**, and click it.
(Or just log out and back in.)

**Nothing shows up?** That's normal if Steam is closed. Start Steam and
the icon will appear.

From now on, it starts by itself every time you log in.

### 4. (Optional) Hide Steam's own tray icon

Otherwise you'll have two Steam icons. On KDE Plasma:

1. Right-click the small **▲** arrow in the system tray
2. Click **Configure System Tray…**
3. Open **Entries**
4. Find **steam** and set it to **Always hidden**

---

## Update

Run the same lines from step 2 again.

## Uninstall

```
sudo pacman -R steam-status-tray
```

If you hid Steam's own tray icon, set it back to **Shown when relevant**
in the same settings page.

---

## Notes

- **Quit Tray Icon** closes it until you log in again, or until you start
  it from the app launcher.
- **Native Steam only.** The Flatpak version of Steam isn't supported.
- **GNOME** doesn't show tray icons by default. Install the
  *AppIndicator and KStatusNotifierItem Support* extension first.
- The status dot reads an undocumented Steam setting. If a Steam update
  breaks it, changing status from the menu will still work.

## License

MIT
