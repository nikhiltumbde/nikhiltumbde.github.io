# nikhiltumbde — personal website

Built with [Quarto](https://quarto.org), hosted on GitHub Pages.

## Setup

### 1. Install Quarto
Download from https://quarto.org/docs/get-started/

### 2. Clone and preview locally
```bash
git clone https://github.com/NikhilT-DS/nikhiltumbde.git
cd nikhiltumbde
quarto preview
```
This opens a live-reloading preview at `localhost:4848`.

### 3. Add your profile photo
Drop a square image (at least 300×300px) at `assets/profile.jpg`.
It's referenced in `index.qmd` as `![](assets/profile.jpg)`.

### 4. Build for production
```bash
quarto render
```
Output goes to the `docs/` folder (configured in `_quarto.yml`).

### 5. Deploy to GitHub Pages
In your repo settings → Pages:
- Source: **Deploy from a branch**
- Branch: `main` / `docs` folder

Then push — GitHub Pages will serve from `docs/`.

---

## Structure

```
.
├── _quarto.yml        # Site config, navbar, theme
├── index.qmd          # Homepage
├── research.qmd       # Publications & patents
├── projects.qmd       # Personal projects
├── blog/
│   └── index.qmd      # Blog listing (add posts/ subfolder when ready)
└── assets/
    ├── styles.css     # Custom CSS
    └── profile.jpg    # Your photo (add this)
```

## Adding a blog post

Create `blog/posts/your-post-title/index.qmd`:

```yaml
---
title: "Your post title"
date: 2026-06-15
categories: [machine learning, fraud]
description: "One sentence summary."
---

Your post content here...
```

The blog listing at `blog/index.qmd` auto-discovers posts in `blog/posts/`.

## Updating content

All content is plain Markdown inside `.qmd` files — edit directly and `quarto preview` to see changes instantly.
