# Agents

## Cursor Cloud specific instructions

This is a Hugo static site (the Context Engineered blog) using the [Blowfish](https://blowfish.page/) theme as a git submodule at `themes/blowfish`. There is no backend, database, or Docker Compose stack.

### Prerequisites

- **Hugo Extended v0.165.0** (or the version pinned in `.github/workflows/hugo.yml`). Blowfish v2.106.0 needs the Extended edition in the 0.158.0–0.165.0 range.
- **Git submodules** initialized: `git submodule update --init --recursive`

### Dev server

```bash
hugo server -D --bind 0.0.0.0 --baseURL http://localhost:1313
```

The site is at `http://localhost:1313`. `-D` includes drafts.

### Production build (the validation step)

There is no separate test or lint suite. A clean Hugo build is the check:

```bash
hugo --gc --minify --printPathWarnings
```

Output goes to `public/`. The build fails on broken templates, invalid front matter, or missing required assets.

### New content

```bash
hugo new content posts/my-post-slug/index.md
```

### Non-obvious notes

- Configuration is split across TOML files in `config/_default/`. Author identity and social links are in `languages.en.toml`; CV content is in `content/authors/mubashir-ali/_index.md`.
- `baseURL` in `hugo.toml` is `https://context-engineered.com/`. `hugo server` overrides it. For inspecting a production-style build locally, pass `--baseURL http://localhost:1313/`.
- GitHub Pages must use Source = **GitHub Actions**. Branch/Jekyll deploys fail because this is not a Jekyll site.
- Do not edit files under `themes/blowfish/` for site customizations; change site config, `content/`, `data/`, `static/`, or add overlays under `layouts/` / `assets/` at the repo root.
