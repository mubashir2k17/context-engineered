# Context-Engineered

Welcome to **Context-Engineered** - a personal branding and technical blog exploring context engineering, AI, and intelligent systems.

## 🚀 Built With

- **[Hugo](https://gohugo.io/)** - Fast and flexible static site generator
- **[Blowfish Theme](https://blowfish.page/)** - Beautiful and feature-rich Hugo theme
- **GitHub Pages** - Free hosting with custom domain support

## 📁 Project Structure

```
.
├── config/              # Hugo configuration files
│   └── _default/
│       ├── hugo.toml    # Main site configuration
│       ├── params.toml  # Theme parameters
│       ├── languages.en.toml  # Language settings
│       └── menus.en.toml      # Navigation menus
├── content/             # Site content (markdown files)
│   ├── _index.md        # Homepage content
│   └── posts/           # Blog posts
├── themes/              # Hugo themes
│   └── blowfish/        # Blowfish theme (git submodule)
├── static/              # Static files (copied to site root)
│   └── CNAME            # Custom domain configuration
├── .github/
│   └── workflows/
│       └── hugo.yml     # GitHub Actions deployment workflow
└── public/              # Generated site (created by Hugo build)
```

## 🛠️ Local Development

### Prerequisites

- Hugo Extended v0.141.0 or later
- Git

### Setup

1. Clone the repository:
```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
```

2. Initialize and update the theme submodule:
```bash
git submodule update --init --recursive
```

3. Start the Hugo development server:
```bash
hugo server -D
```

4. Open your browser to `http://localhost:1313`

## 📝 Creating Content

### New Blog Post

Create a new blog post using Hugo's CLI:

```bash
hugo new content/posts/my-new-post.md
```

Or manually create a file in `content/posts/` with this frontmatter:

```markdown
---
title: "My New Post Title"
date: 2025-12-24
draft: false
description: "A brief description of your post"
tags: ["tag1", "tag2"]
categories: ["Technical"]
---

Your content here...
```

## 🚀 Deployment

This site is automatically deployed to GitHub Pages using GitHub Actions whenever you push to the `main` branch.

### GitHub Pages Setup

1. Go to your repository Settings → Pages
2. Under "Build and deployment", select:
   - **Source**: GitHub Actions
3. The site will be available at `https://context-engineered.com` (or your custom domain)

### Custom Domain

The custom domain is configured in the `static/CNAME` file. It's automatically included in the built site.

## 🎨 Customization

### Site Configuration

Edit `config/_default/hugo.toml` to change:
- Site title
- Base URL
- Language settings
- Taxonomies

### Theme Parameters

Edit `config/_default/params.toml` to customize:
- Color scheme
- Layout options
- Features (search, code copy, etc.)
- Social sharing

### Author Information

Edit `config/_default/languages.en.toml` to update:
- Author name and bio
- Social media links
- Site description

## 📚 Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Blowfish Theme Documentation](https://blowfish.page/docs/)
- [Blowfish Theme Examples](https://blowfish.page/examples/)

## 📄 License

Content is copyrighted. Theme is licensed under the MIT License.

---

**Happy blogging!** 🎉
