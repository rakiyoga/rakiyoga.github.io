# CLAUDE.md — Raki Yoga Project

## Project Overview
Raki Yoga is an Ayurveda health consultancy website for Rakesh Singh ("Raki"), based in Berlin, Germany. Built with Jekyll and the Beautiful Jekyll theme, hosted on GitHub Pages.

**Live site**: https://rakiyoga.de / https://rakiyoga.github.io

## Tech Stack
- **SSG**: Jekyll ≥ 3.9.3 with Beautiful Jekyll v6.0.1 theme
- **Frontend**: Bootstrap 4.4.1, jQuery 3.5.1, Font Awesome 6.5.2
- **Fonts**: Lora (headings), Open Sans (body)
- **Markdown**: Kramdown with GFM
- **Hosting**: GitHub Pages with custom domain
- **CI**: GitHub Actions (`.github/workflows/ci.yml`)

See @docs/techstack.md for full details.

## Build & Serve Commands
```bash
# Install dependencies
bundle install

# Serve locally (http://localhost:4000)
bundle exec jekyll serve

# Build for production
bundle exec jekyll build

# CI build (with appraisal)
bundle exec appraisal jekyll build --future
```

## Project Structure
```
├── _config.yml          # Jekyll configuration (navbar, colors, social links)
├── _layouts/            # HTML templates (base, default, home, page, post, minimal)
├── _includes/           # Reusable HTML partials (nav, footer, head, comments, etc.)
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── _data/               # YAML data files (ui-text.yml)
├── assets/              # Static assets
│   ├── css/             # Stylesheets (beautifuljekyll.css, bootstrap-social.css)
│   ├── js/              # JavaScript (beautifuljekyll.js, staticman.js)
│   └── img/             # Images (logo, food lists, backgrounds)
├── docs/                # Project documentation (techstack, prd, progress)
├── .claude/             # Claude Code configuration
│   ├── skills/          # Skill definitions
│   ├── agents/          # Subagent definitions
│   ├── tools/           # Tool documentation
│   ├── rules/           # Coding & content rules
│   ├── examples/        # Usage examples
│   └── context/         # Project context
├── 1_aboutme.md         # About page
├── 2_wisdom.md          # Blog feed (home layout)
├── 3_ayurveda_fundamentals.md  # Ayurveda education
├── 4_recipes.md         # Recipes
├── 5_consultation.md    # Consultation services
├── 6_contact.md         # Contact page with form
├── index.html           # Home page (top-10 lists)
├── privacy.md           # Privacy policy
└── feed.xml             # RSS feed template
```

## Code Style & Conventions

### YAML Front Matter
Every page/post requires front matter:
```yaml
---
layout: page          # or 'post', 'home', 'default', 'minimal'
title: Page Title
subtitle: Optional subtitle
---
```

### File Naming
- **Pages**: `N_pagename.md` (numbered for navbar ordering)
- **Posts**: `YYYY-MM-DD-title-with-dashes.md` in `_posts/`
- **Images**: `descriptive_name.jpg` in `assets/img/`

### HTML in Markdown
- Use `<details>/<summary>` for expandable sections
- Use `<img>` tags with `class="pic"` for images
- Use `<p>` and `<b>` for formatted content within details blocks

### Color Theme
Forest green palette — defined in `_config.yml`:
- Primary: `#2E7D32` (navbar, footer)
- Page background: `#E8F5E9`
- Links: `#4CAF50`
- Hover: `#388E3C`

### Content Guidelines
- Ayurveda terminology: include Sanskrit terms with transliteration
- Bilingual audience: primarily English, some German context
- Scientific + traditional knowledge blend
- Always include disclaimer for health advice

## Additional Instructions
- Skills reference: @.claude/skills/
- Content rules: @.claude/rules/content-guidelines.md
- Coding standards: @.claude/rules/coding-standards.md
- Project context: @.claude/context/project-overview.md
- PRD: @docs/prd.md
- Progress: @docs/progress.md
