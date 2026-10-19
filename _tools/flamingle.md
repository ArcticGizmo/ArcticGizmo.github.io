---
name: Flamingle
order: 6
subtitle: Windows that flock together.
logo: /assets/img/flamingle.svg
type: Desktop App
language: C#
tags: [windows, window-management, productivity, tray]
repo: ArcticGizmo/flamingle
releasesUrl: https://github.com/ArcticGizmo/flamingle/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/flamingle
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/flamingle/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Flamingle-win-Setup.exe
      - label: Portable (.zip)
        url: Flamingle-win-Portable.zip
---

Most work spans more than one window: an editor and a terminal, a browser and
its dev tools, mail beside a calendar. Windows treats each one as a stranger, so
you minimise, restore and arrange them one at a time. Flamingle is a small
Windows tray app that groups windows into **flocks** that minimise, restore,
move and relaunch together, and snaps them into **layouts** on each monitor.

Pick a few windows and one hotkey or taskbar click puts them all away or brings
them all back. Hold Shift while dragging a window to snap it into a zone of the
monitor's layout, and everything in that layout becomes a flock too. Save a
flock and Flamingle can later start its apps and put every window back where it
was.

Each flock gets its own taskbar button, with a preview of the whole flock laid
out as it is on screen. Layouts follow docked side panels, survive monitors
being renumbered after a wake, and keep to one flock per virtual desktop.

Flamingle is young and still experimental. Most behaviours can be switched off
in Settings if you'd rather not have them.
