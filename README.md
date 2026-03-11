# Raki Yoga — Ayurveda Health Consultancy

[![Beautiful Jekyll CI](https://github.com/rakiyoga/rakiyoga.github.io/actions/workflows/ci.yml/badge.svg)](https://github.com/rakiyoga/rakiyoga.github.io/actions)

> Holistic wellness through Ayurveda, yoga, and meditation — Berlin & Online

🌐 **Live**: [rakiyoga.de](https://rakiyoga.de) | [rakiyoga.github.io](https://rakiyoga.github.io)

## About

Personal website for **Rakesh Singh ("Raki")**, an Ayurvedic health consultant based in Berlin, Germany. The site provides educational Ayurveda content, recipes, consultation services, and holistic health guidance.

## Tech Stack

- **Jekyll** ≥ 3.9.3 — Static site generator
- **Beautiful Jekyll** v6.0.1 — Theme
- **Bootstrap** 4.4.1 — Responsive CSS framework
- **GitHub Pages** — Hosting
- **GitHub Actions** — CI/CD

See [docs/techstack.md](docs/techstack.md) for full details.

## Local Development

### Prerequisites
- Ruby (≥ 3.3 recommended)
- Bundler (`gem install bundler`)

### Setup & Run
```bash
# Install dependencies
bundle install

# Start local dev server
bundle exec jekyll serve --livereload

# Open in browser
open http://localhost:4000
```

### Build
```bash
# Production build
bundle exec jekyll build

# Build with future-dated posts
bundle exec jekyll build --future
```

## Project Structure

```
├── _config.yml          # Site configuration
├── _layouts/            # HTML templates
├── _includes/           # Reusable partials
├── _posts/              # Blog posts
├── _data/               # YAML data
├── assets/              # CSS, JS, images
├── docs/                # Project documentation
│   ├── techstack.md     # Technology stack
│   ├── prd.md           # Product requirements
│   └── progress.md      # Development progress
├── .claude/             # Claude Code configuration
│   ├── skills/          # Development skills
│   ├── agents/          # Subagent definitions
│   ├── tools/           # Tool documentation
│   ├── rules/           # Standards & guidelines
│   ├── examples/        # Usage examples
│   └── context/         # Project context
├── index.html           # Home page
├── 1_aboutme.md         # About page
├── 2_wisdom.md          # Blog feed
├── 3_ayurveda_fundamentals.md
├── 4_recipes.md         # Ayurvedic recipes
├── 5_consultation.md    # Services
├── 6_contact.md         # Contact form
├── CLAUDE.md            # Claude Code project memory
└── CHANGELOG.md         # Version history
```

## Content Pages

| Page | URL Path | Description |
|------|----------|-------------|
| Home | `/` | Top-10 food lists |
| About | `/1_aboutme` | Bio & certifications |
| Wisdom | `/2_wisdom` | Blog feed |
| Ayurveda | `/3_ayurveda_fundamentals` | Educational content |
| Recipes | `/4_recipes` | Seasonal recipes |
| Consultation | `/5_consultation` | Services offered |
| Contact | `/6_contact` | Contact form & info |

## Documentation

- **[techstack.md](docs/techstack.md)** — Full technology stack details
- **[prd.md](docs/prd.md)** — Product requirements & roadmap
- **[progress.md](docs/progress.md)** — Development progress tracker

## Developer

rakiyoga, jrv07

## License

MIT License — Copyright (c) 2021
