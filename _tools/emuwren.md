---
name: Emuwren
order: 4
subtitle: Create, configure & debug Android emulators — no Android Studio required.
logo: /assets/img/emuwren.svg
type: Desktop App
language: C#
tags: [windows, android, emulator, sdk, developer-tools]
repo: ArcticGizmo/emuwren
releasesUrl: https://github.com/ArcticGizmo/emuwren/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/emuwren
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/emuwren/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Emuwren-win-Setup.exe
      - label: Portable (.zip)
        url: Emuwren-win-Portable.zip
---

Emuwren is a Windows desktop app for managing Android emulators — creating,
configuring and debugging them — while handling the Android SDK setup for you
automatically. It's a friendly graphical layer over Google's Android
command-line tools, so you get SDK management, emulator controls, environment
configuration and system diagnostics without ever installing Android Studio.

Common setup headaches are caught by automated checks with one-click fixes.
Browse and install SDK packages from a searchable, categorised catalogue, spin
up emulators from device profiles, and reach settings the CLI won't expose —
RAM, cores, resolution and GPU mode. Live logcat filtering and device-property
inspection help you debug, and a reversible teardown lets you reset everything
for testing.
