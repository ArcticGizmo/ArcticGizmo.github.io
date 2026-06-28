# ArcticGizmo.github.io

The source for my personal site at **https://arcticgizmo.github.io** — a launchpad
for the standalone tools, libraries, and apps I maintain.

Built with [Jekyll](https://jekyllrb.com/), which GitHub Pages builds and deploys
automatically on every push to `main`.

## Adding or editing a tool

All the content lives in one file: **`_data/projects.yml`**. To add a tool, copy an
existing block and edit the fields:

```yaml
- name: My Tool
  description: One or two punchy sentences about what it does.
  type: CLI                 # optional badge: CLI / Library / Desktop App / …
  language: Rust            # optional badge
  install: cargo install my-tool   # optional code snippet
  tags: [terminal, fast]    # optional keywords
  links:                    # optional buttons
    - label: Repo
      url: https://github.com/ArcticGizmo/my-tool
    - label: Docs
      url: https://github.com/ArcticGizmo/my-tool#readme
```

Only `name` and `description` are required — leave anything else out and it just
won't render. Commit, push, and the site updates in a minute or two.

## Project structure

```
_config.yml           Site title, tagline, URL
_data/projects.yml    ← edit this to add/change tools
index.html            Homepage that renders the cards
_layouts/default.html Page shell (head, footer)
assets/css/style.css  Styling (responsive, dark-mode aware)
docker-compose.yml    Local preview setup (see below)
```

## Previewing locally (optional)

You don't need this — pushing to `main` is enough — but to preview before
committing you can use Docker (no Ruby install required):

```sh
docker-compose up      # then open http://localhost:4000, Ctrl+C to stop
```

This builds the site and serves it, rebuilding automatically when you edit a
file. The first run downloads the Jekyll and Python images, so give it a minute.

> Note: this uses the Jekyll image's built-in gems rather than installing the
> `github-pages` gem, so it never has to reach RubyGems — which keeps it working
> behind a corporate TLS proxy. The site uses only core Jekyll features, so the
> preview matches what GitHub Pages publishes.
