---
name: Sprig
order: 2
subtitle: Worktree & infrastructure isolation for any git repo.
logo: /assets/img/sprig.svg
type: Desktop App
language: C#
tags: [windows, git, worktree, docker, cli]
repo: ArcticGizmo/sprig
releasesUrl: https://github.com/ArcticGizmo/sprig/releases/latest
links:
  - label: Repo
    url: https://github.com/ArcticGizmo/sprig
platforms:
  - os: windows
    install_label: PowerShell (recommended)
    install: irm https://raw.githubusercontent.com/ArcticGizmo/sprig/main/install.ps1 | iex
    downloads:
      - label: Installer (.exe)
        url: Sprig-win-Setup.exe
---

Worktree and infrastructure isolation for any git repo. Spin up isolated
workspaces, each on its own branch, with non-colliding ports and docker infra,
so you can work on several things at once without them stepping on each other.

Available as both a CLI and a desktop app, so it fits whether you live in the
terminal or prefer to point and click.
