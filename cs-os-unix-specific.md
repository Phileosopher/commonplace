
# Specific Unix-based commands and shortcuts

## Keyboard tweaks

To add a compose key:

Open /etc/default/keyboard

- "XKBOPTIONS=compose:ralt" (or whatever compose keyboard mapping you want)
- Your compose key can be the following:
  - ralt (a good general option)
  - lwin/rwin (probably not a good idea since it opens the bottom left programs bar)
  - menu (probably not on most keyboards)
  - lctrl/rctrl (might be a good option)
  - caps (a bad idea unless you never use caps lock ever)
  - paus (a good option)
  - prsc (not recommended if you ever use screenshots)
  - sclk (not recommended if you ever use it)

## Keyboard shortcuts

Navigate to display manager (login screen): CTRL+ALT+F1

Navigate to GUI (desktop environment): CTRL+ALT+F2

Drop to terminal: CTRL+ALT+F3/F4/F5/F6

Open terminal (Debian-based): CTRL+ALT+T

## Cleaning the system

Routinely, it's wise to clear out unused memory and optimize the system.

1. Uninstall unneeded software
2. Clean unnecessary packages and dependencies (e.g., autoremove)
3. Clear the thumbnail cache:
   - du -sh ~/.cache/thumbnails (view its size)
   - sudo rm -rf ~/.cache/thumbnails/* (delete the cache)
4. Clear the package manager cache:
   - sudo du -sh /var/cache/apt
   - sudo apt/dnf clean
5. Remove orphaned packages
6. Remove unnecessary kernels
7. Remove unused locale files
