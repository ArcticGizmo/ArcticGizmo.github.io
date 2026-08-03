---
name: Otter
order: 6
subtitle: Hands-off Slack status for your calls.
logo: /assets/img/otter.png
type: Desktop App
language: C#
tags: [windows, slack, teams, tray]
repo: ArcticGizmo/otter
releasesUrl: https://github.com/ArcticGizmo/otter/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/otter
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/otter/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Otter-win-Setup.exe
---

Hands-off Slack status for your calls. Otter detects when you're on a Microsoft
Teams call, sets your Slack status to match, then clears it again the moment you
hang up.

Set it once and forget it — no more manually toggling your status every time a
meeting starts.
