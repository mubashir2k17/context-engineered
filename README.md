# Context Engineered

Personal site and technical blog by [Mubashir Ali](https://github.com/mubashir2k17) on context engineering, AI, and software development.

🌐 **Live site**: [context-engineered.com](https://context-engineered.com)

## About

This site is built with [Hugo](https://gohugo.io/) and the [Blowfish](https://blowfish.page/) theme. It is a place to write about making AI systems useful in production — prompt and context design, architecture, and delivery.

## Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) v0.165.0 (or a nearby Extended release)
- Git, with submodule support

### Quick start

```bash
git clone --recurse-submodules https://github.com/mubashir2k17/context-engineered.git
cd context-engineered
hugo server -D
```

If the clone was done without submodules:

```bash
git submodule update --init --recursive
```

Then open [http://localhost:1313](http://localhost:1313).

### Creating content

```bash
hugo new content posts/my-new-post/index.md
```

New posts use the `mubashir-ali` author by default. Keep `draft: true` until the post is ready.

### Building for production

```bash
hugo --gc --minify
```

Output is written to `public/`.

## Deployment

Pushes to `main` build and deploy the site to GitHub Pages via `.github/workflows/hugo.yml`. Pull requests run the same Hugo build without deploying.

**Pages source must be GitHub Actions.** In the repository: Settings → Pages → Build and deployment → Source → **GitHub Actions**. If Source stays on "Deploy from a branch", GitHub also runs its Jekyll `pages-build-deployment` workflow, which fails for this Hugo project and can fight the Actions deploy.

The production `baseURL` is `https://context-engineered.com/`. `hugo server` overrides this locally. For a local production-style build use `--baseURL http://localhost:1313/`.

## Project structure

```
.
├── archetypes/          # Content templates
├── config/_default/     # Hugo configuration
├── content/             # Markdown content
│   ├── posts/          # Blog posts
│   ├── authors/        # Author / CV pages
│   └── about/          # About page
├── data/authors/        # Author metadata
├── static/              # Files copied as-is (CNAME, .nojekyll)
└── themes/blowfish/     # Blowfish theme (git submodule)
```

## Configuration

Site config lives in `config/_default/`:

- `hugo.toml` — Hugo core settings
- `languages.en.toml` — title, author, social links
- `params.toml` — Blowfish theme parameters
- `menus.en.toml` — header and footer navigation
- `markup.toml` — Markdown / highlighting

## Theme

Blowfish is vendored as a git submodule. Theme docs: [blowfish.page/docs](https://blowfish.page/docs/).

## License

Content is © Mubashir Ali. Hugo and Blowfish have their own licenses.
