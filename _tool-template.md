---
# ---------------------------------------------------------------------------
# TEMPLATE — copy this file into _tools/ and rename it (e.g. _tools/my-app.md).
# The file name (minus .md) becomes the page URL: /tools/my-app/.
# This file itself is excluded from the build (see _config.yml).
#
# Everything except `name` is optional — leave a field out and that part of
# the page simply won't render.
# ---------------------------------------------------------------------------

name: My App                 # Display name (card title + page <h1>)
order: 99                    # Sort position on the home page (low = first)
subtitle: One punchy line.   # Short line under the title on the card & page
logo: /assets/img/my-app.svg # Local path (drop file in assets/img/) or https:// URL
type: Desktop App            # Free-text badge: Desktop App / CLI / Library …
language: C#                 # Optional language chip
tags: [windows, utility]     # Short keyword chips

repo: ArcticGizmo/my-app     # GitHub "owner/name". Used to expand bare download
                             # filenames to that repo's LATEST release asset.
releasesUrl: https://github.com/ArcticGizmo/my-app/releases/latest
links:                       # Buttons shown in the page hero (Repo, Docs, …)
  - label: Repo
    url: https://github.com/ArcticGizmo/my-app

# Downloads grouped by OS. Each `os` (windows / macos / linux) gets its own
# card with an OS logo in the "How to install" section.
platforms:
  - os: windows
    # Optional one-liner install shown at the top of the OS card. Great for a
    # PowerShell one-liner. Add `install_label:` to caption it.
    # install_label: PowerShell
    # install: irm https://arcticgizmo.github.io/get/my-app.ps1 | iex
    downloads:
      # `url` is EITHER a full https:// URL (used verbatim) OR a bare release
      # asset filename, expanded to: <repo>/releases/latest/download/<url>
      - label: Installer (.exe)
        url: MyApp-win-Setup.exe
  - os: macos
    downloads:
      - label: Apple Silicon (.dmg)
        url: MyApp-osx-arm64.dmg
---

Write the **detailed description** here as normal Markdown. The first chunk
shows on the project page; if it's long, a "See more" button reveals the rest.

You can use multiple paragraphs, **bold**, lists, and links — it's the full
long-form pitch for the tool.
