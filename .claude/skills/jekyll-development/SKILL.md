---
name: jekyll-development
description: Jekyll static site development with Beautiful Jekyll theme — build, serve, customize, and deploy
---

# Jekyll Development Skill

## Overview
This skill covers local development, customization, and deployment of a Jekyll site using the Beautiful Jekyll v6.0.1 theme.

## Prerequisites
- Ruby ≥ 3.3 (for CI) or compatible local version
- Bundler gem installed (`gem install bundler`)
- Git

## Quick Start
```bash
# Install all gem dependencies
bundle install

# Start local dev server with live reload
bundle exec jekyll serve --livereload

# Build production site to _site/
bundle exec jekyll build

# Build with future-dated posts
bundle exec jekyll build --future
```

## Layout System
Beautiful Jekyll provides these layouts:

| Layout | Purpose |
|--------|---------|
| `base` | Root HTML document (includes head, nav, footer) |
| `default` | Wraps content in standard container |
| `page` | Standard content page with title/subtitle |
| `post` | Blog post with date, author, social share |
| `home` | Blog feed with pagination |
| `minimal` | Stripped-down layout |

### Layout Hierarchy
```
base.html
├── default.html
│   ├── page.html
│   ├── post.html
│   └── home.html
└── minimal.html
```

## Creating a New Page
1. Create `N_pagename.md` in root (N = order number)
2. Add YAML front matter:
   ```yaml
   ---
   layout: page
   title: My Page
   subtitle: Optional description
   ---
   ```
3. Add to navbar in `_config.yml`:
   ```yaml
   navbar-links:
     "Page Name": "N_pagename"
   ```

## Creating a Blog Post
1. Create file in `_posts/YYYY-MM-DD-title.md`
2. Add front matter:
   ```yaml
   ---
   layout: post
   title: "Post Title"
   subtitle: "Optional subtitle"
   tags: [ayurveda, health]
   comments: true
   ---
   ```

## Liquid Templating
Common Liquid patterns used in this project:
```liquid
{% include nav.html %}
{% include footer.html %}
{{ content }}
{{ page.title }}
{{ site.title }}
{% for post in paginator.posts %}
  {{ post.title }}
{% endfor %}
```

## Configuration (_config.yml)
Key settings:
- `title` — Site name
- `navbar-links` — Navigation menu items
- `avatar` — Logo image path
- `social-network-links` — Footer social icons
- Color variables (`navbar-col`, `page-col`, etc.)
- `plugins` — jekyll-paginate, jekyll-sitemap

## Deployment
- **GitHub Pages**: Automatic on push to main branch
- **CI**: GitHub Actions runs `bundle exec appraisal jekyll build --future`
- **Custom domain**: Configured via `CNAME` file (`rakiyoga.de`)

## Troubleshooting
| Issue | Fix |
|-------|-----|
| `bundle install` fails | Check Ruby version, run `gem update --system` |
| CSS not updating | Clear `_site/` and `.sass-cache/` |
| Page not in navbar | Add entry to `navbar-links` in `_config.yml` |
| Images not showing | Verify path starts with `/assets/img/` |
| Build warnings | Check timezone setting (`Germany/Berlin` may need `Europe/Berlin`) |
