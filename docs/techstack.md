# Technology Stack — Raki Yoga

## Static Site Generator
| Component | Details |
|-----------|---------|
| **Framework** | [Jekyll](https://jekyllrb.com/) ≥ 3.9.3 |
| **Theme** | [Beautiful Jekyll](https://beautifuljekyll.com/) v6.0.1 |
| **Markup** | Kramdown (GFM — GitHub Flavored Markdown) |
| **Syntax Highlighting** | Rouge |
| **Language** | Ruby (Gemspec-based) |

## Frontend Libraries
| Library | Version | Purpose |
|---------|---------|---------|
| **Bootstrap** | 4.4.1 | Responsive CSS framework |
| **jQuery** | 3.5.1 (slim) | DOM manipulation, Bootstrap dependency |
| **Popper.js** | 1.16.0 | Tooltip/popover positioning |
| **Font Awesome** | 6.5.2 | Icon library |

## Typography (Google Fonts)
- **Lora** (400, 700, italic) — Headings & accents
- **Open Sans** (300–800, italic) — Body text

## Color System
| Variable | Value | Role |
|----------|-------|------|
| `page-col` | `#E8F5E9` | Light green page background |
| `text-col` | `#333333` | Main text |
| `link-col` | `#4CAF50` | Links |
| `hover-col` | `#388E3C` | Hover state |
| `navbar-col` | `#2E7D32` | Forest green navbar |
| `footer-col` | `#2E7D32` | Forest green footer |
| `navbar-text-col` | `#FFFFFF` | White navbar text |
| `footer-text-col` | `#FFFFFF` | White footer text |

## Hosting & Deployment
| Service | Details |
|---------|---------|
| **Hosting** | GitHub Pages |
| **Domain** | `rakiyoga.de` (CNAME), `rakiyoga.github.io` |
| **CI/CD** | GitHub Actions (`ci.yml`) |
| **Build** | `bundle exec appraisal jekyll build --future` |

## Jekyll Plugins
- `jekyll-paginate` ~> 1.1 — Blog pagination
- `jekyll-sitemap` ~> 1.4 — Auto-generated sitemap.xml

## Development Dependencies
- `bundler` ≥ 1.16
- `rake` ~> 12.0
- `appraisal` ~> 2.5
- `kramdown-parser-gfm` ~> 1.1
- `kramdown` ~> 2.3
- `webrick` ~> 1.8 (local server)

## Content Types
- **Pages** — Markdown with YAML front matter (`.md`)
- **Blog Posts** — Markdown in `_posts/` with date-prefixed filenames
- **Layouts** — Liquid HTML templates (`_layouts/`)
- **Includes** — Reusable HTML partials (`_includes/`)
- **Data** — YAML files (`_data/`)
- **Assets** — CSS, JS, images (`assets/`)
