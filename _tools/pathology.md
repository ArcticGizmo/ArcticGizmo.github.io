---
name: PATHology
order: 5
subtitle: Find and safely fix security and correctness problems in your Windows PATH.
logo: /assets/img/pathology.svg
type: Desktop App
language: C#
tags: [windows, security, path, utility]
repo: ArcticGizmo/pathology
releasesUrl: https://github.com/ArcticGizmo/pathology/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/pathology
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/pathology/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Pathology-win-Setup.exe
      - label: Portable (.zip)
        url: Pathology-win-Portable.zip
---

PATHology is a Windows desktop app that checks your machine and user `PATH` for
security and correctness problems, explains each one in plain language, and
fixes them safely, with every change backed up and undoable.

It looks for system folders that any user can write (a way to get code running
as SYSTEM), folders that don't exist yet but anyone could create, entries that
shadow Windows' own commands, `%VAR%`s that never expand, duplicates, dead
entries and values nearing the length limit. Each of its 25 checks says what's
wrong, why it matters and how to fix it, and each category (Security,
Correctness, Hygiene) is rated by its worst problem, so ten tidy-ups can't hide
one open door.

Nothing changes until you say. Review the before-and-after ratings, each diff
and every folder permission change before applying, with one UAC prompt per
apply (none at all for your user PATH). Writes keep `REG_EXPAND_SZ`, never use
`setx`, and are backed up to History so they can be undone.

A scan is read-only: no test files, no shell-outs, network paths left alone, and
it runs unelevated.
