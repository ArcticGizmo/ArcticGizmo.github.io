# Adding a tool

Each tool on the site is a single Markdown file in [`_tools/`](../_tools). The
file name becomes the URL — `_tools/perch.md` → `/tools/perch/` — and the site
builds a home-page card plus a full project page from it automatically.

## Quick start

1. Copy [`_tool-template.md`](../_tool-template.md) into `_tools/` and rename it
   to your tool's slug, e.g. `_tools/my-app.md`.
2. Fill in the front-matter (everything between the `---` lines).
3. Write the long-form description as Markdown in the body (below the
   front-matter). If it's long, the project page shows a **See more** toggle.
4. Drop any logo into `assets/img/`.

## Front-matter fields

| Field         | Required | Purpose |
|---------------|----------|---------|
| `name`        | yes      | Card title and page heading. |
| `order`       | no       | Home-page sort position (low = first). |
| `subtitle`    | no       | Short line under the title (the "draw me in" hook). |
| `logo`        | no       | `/assets/img/…` path or full `https://` URL. Falls back to a lettered badge. |
| `type`        | no       | Free-text badge, e.g. `Desktop App`, `CLI`, `Library`. |
| `language`    | no       | Language chip, e.g. `C#`, `Rust`. |
| `tags`        | no       | List of short keyword chips. |
| `repo`        | no       | `owner/name`; used to expand bare download filenames. |
| `releasesUrl` | no       | Adds a "See all releases →" link under the install section. |
| `links`       | no       | List of `{ label, url }` buttons shown in the page hero. |
| `platforms`   | no       | Downloads grouped by OS — see below. |

## Platforms & downloads

Downloads are grouped per operating system. Each entry renders as its own card
(with an OS logo) in the **How to install** section:

```yaml
platforms:
  - os: windows            # windows | macos | linux (drives the logo + label)
    install_label: PowerShell         # optional caption for the one-liner
    install: irm https://…/get.ps1 | iex   # optional one-liner shown up top
    downloads:
      - label: Installer (.exe)
        url: MyApp-win-Setup.exe      # bare name → repo's LATEST release asset
      - label: Portable (.zip)
        url: https://example.com/MyApp.zip   # full URL → used verbatim
```

A bare `url` (no `://`) is expanded to
`https://github.com/<repo>/releases/latest/download/<url>` — a stable link that
always points at the newest release.

## Preview locally

```sh
docker-compose up
```

Then open <http://localhost:4000>.
