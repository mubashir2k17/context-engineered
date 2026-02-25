## Cursor Cloud specific instructions

### Overview

This is a Hugo static site ("Context Engineered" blog) using the [Blowfish](https://blowfish.page/) theme via git submodule. There are no backend services, databases, or Docker containers.

### Prerequisites (installed by update script)

- **Hugo Extended v0.141.0** — installed from the official `.deb` release. Must be the Extended edition (required by the Blowfish theme for Sass processing).
- **Git submodules** — the Blowfish theme lives at `themes/blowfish` and must be initialized.

### Running the dev server

```bash
hugo server -D --bind 0.0.0.0 --baseURL http://localhost:1313
```

The `-D` flag includes draft content. The site is served at `http://localhost:1313`.

### Building

```bash
hugo --gc --minify
```

Output goes to `public/`.

### Creating content

```bash
hugo new content posts/my-post-slug/index.md
```

### Non-obvious notes

- There is no `package.json`, `Makefile`, linter config, or test framework in this project. Hugo itself is the only tool.
- Hugo has no traditional "lint" or "test" commands. The build (`hugo --gc --minify`) serves as the validation step — it will fail on broken templates, invalid front matter, or missing assets.
- Configuration is split across 5 TOML files in `config/_default/` (see `README.md` for details).
- The `baseURL` in `hugo.toml` is set to `https://context-engineered.com/`. For local dev, the `hugo server` command overrides this automatically, but when building for local inspection use `--baseURL http://localhost:1313/`.
