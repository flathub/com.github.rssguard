Starting from version 4.2.2, RSS Guard ships with an integrated web browser (Qt WebEngine) enabled by default.

If you wish to disable this feature, one option is to create a custom desktop file called `com.github.rssguard.desktop` that runs RSS Guard with the `--no-web-engine` option, like so:

```ini
[Desktop Entry]
Type=Application
Name=RSS Guard
GenericName=Feed reader
Comment=Tiny yet feature rich Qt feed reader
TryExec=flatpak
Exec=flatpak run com.github.rssguard --no-web-engine
Icon=com.github.rssguard
X-GNOME-Autostart-Delay=15
X-LXQt-Need-Tray=true
Categories=Qt;Network;News;
StartupWMClass=rssguard
X-Flatpak=com.github.rssguard
```

Then, you can save this file in one of these two directories:

- `~/.local/share/applications/` (current user)
- `/usr/share/applications/` (all users)
