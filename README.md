# Context Engineered

A personal branding and technical blog focused on context engineering, AI, and software development.

🌐 **Live Site**: [context-engineered.com](https://context-engineered.com)

## About

This website is built with [Hugo](https://gohugo.io/) using the beautiful [Blowfish](https://blowfish.page/) theme. It's designed for sharing insights about context engineering, AI interactions, and the future of human-AI collaboration.

## Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (v0.140.0 or later)

### Quick Start

1. Clone the repository with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/yourusername/context-engineered.git
   cd context-engineered
   ```

2. If you already cloned without submodules, initialize them:
   ```bash
   git submodule update --init --recursive
   ```

3. Start the development server:
   ```bash
   hugo server -D
   ```

4. Open [http://localhost:1313](http://localhost:1313) in your browser.

### Creating New Content

Create a new blog post:
```bash
hugo new content posts/my-new-post/index.md
```

### Building for Production

```bash
hugo --gc --minify
```

The generated site will be in the `public/` directory.

## Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/hugo.yml`).

## Project Structure

```
.
├── archetypes/          # Content templates
├── assets/              # Asset files (images, etc.)
├── config/_default/     # Hugo configuration files
├── content/             # Website content (Markdown files)
│   ├── posts/          # Blog posts
│   └── about/          # About page
├── layouts/             # Custom layout templates (optional)
├── static/              # Static files (CNAME, favicon, etc.)
└── themes/blowfish/     # Blowfish theme (git submodule)
```

## Configuration

The site configuration is split into multiple files in `config/_default/`:

- `hugo.toml` - Main Hugo configuration
- `languages.en.toml` - Language and author settings
- `params.toml` - Theme parameters
- `menus.en.toml` - Navigation menus
- `markup.toml` - Markdown rendering settings

## Theme

This site uses the [Blowfish](https://blowfish.page/) theme. For theme documentation and customization options, visit [blowfish.page/docs](https://blowfish.page/docs/).

## License

Content is © Context Engineered. The Hugo framework and Blowfish theme have their own licenses.

---

*Built with curiosity, powered by experimentation, and shared with love* ❤️
