---
name: Binoc
order: 4
subtitle: A close look at Android & Apple app binaries — without the toolchain.
logo: /assets/img/binoc.svg
type: Desktop App
language: C#
tags: [windows, android, ios, apk, aab, ipa]
repo: ArcticGizmo/binoc
releasesUrl: https://github.com/ArcticGizmo/binoc/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/binoc
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/binoc/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Binoc-win-Setup.exe
---

Binoc is a small Windows desktop app that inspects Android (`.apk`, `.aab`) and
iOS (`.ipa`) binaries and produces one normalised report across the categories
that matter — identity, signing, provisioning, code, obfuscation/optimisation,
size and security posture. Drag a file in, or pick one, and read the result. No
Android Studio, no Xcode, no `aapt2` / `apksigner` / `bundletool` / `codesign` —
binoc parses everything itself in managed .NET.

See identity and signing at a glance, read real R8 optimisation metrics straight
from Google Play's own bundle metadata rather than guesses, spot commercial
packers and protectors, and inspect iOS posture — provisioning, entitlements,
Mach-O architectures, FairPlay encryption and hardening flags.
