---
name: Port Hawk
order: 8
subtitle: Find what's holding your file or port — and kill it.
logo: /assets/img/port-hawk.png
type: Desktop App
language: C#
tags: [windows, process, utility]
repo: ArcticGizmo/port-hawk
releasesUrl: https://github.com/ArcticGizmo/port-hawk/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/port-hawk
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/port-hawk/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: PortHawk-win-Setup.exe
      - label: Portable (.zip)
        url: PortHawk-win-Portable.zip
---

Find what's holding your file or port — and kill it. No more running random CMD
commands to hunt down and stop the process that's locking a file or hogging a
port.

Search by port or by path, see exactly what's responsible, and end it in a
single click.
