---
name: Perch
order: 1
subtitle: Keep an eye on every Claude Code session from one floating panel.
logo: /assets/img/perch.svg
type: Desktop App
language: C#
tags: [windows, macos, claude-code, tray]
repo: ArcticGizmo/perch
releasesUrl: https://github.com/ArcticGizmo/perch/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/perch
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/perch/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Perch-win-Setup.exe
  - os: macos
    downloads:
      - label: Apple Silicon (.dmg)
        url: Perch-osx-arm64.dmg
---

Keep an eye on every Claude Code session from one floating panel — get
notified the moment a session needs you, track your usage at a glance, and add
custom notes to each of your sessions so you always know what needs to be done.

Perch sits quietly in your tray and surfaces only when something changes, so you
can run several sessions in parallel without constantly tabbing between them.
