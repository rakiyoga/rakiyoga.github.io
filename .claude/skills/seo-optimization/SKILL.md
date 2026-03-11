---
name: seo-optimization
description: SEO best practices for Jekyll sites on GitHub Pages — meta tags, structured data, sitemap, and social sharing
---

# SEO Optimization Skill

## Overview
Search engine optimization guidelines specific to Jekyll/Beautiful Jekyll sites hosted on GitHub Pages.

## Jekyll SEO Infrastructure

### Sitemap
The `jekyll-sitemap` plugin auto-generates `sitemap.xml` at build time. No configuration needed — all pages and posts are included.

### Feed
RSS feed is generated via `feed.xml` template. Configure in `_config.yml`:
```yaml
rss-description: "Your RSS feed description"
social-network-links:
  rss: true
```

## Meta Tags (Built into Beautiful Jekyll)

### Page-Level YAML Parameters
```yaml
---
title: "Page Title"              # → <title> tag & og:title
subtitle: "Brief description"    # → meta description
share-title: "Custom Share Title"  # Override for social sharing
share-description: "Custom description"  # Override meta description
share-img: "/assets/img/share.jpg"  # Social share image
cover-img: "/assets/img/cover.jpg"  # Hero/cover image
thumbnail-img: "/assets/img/thumb.jpg"  # Feed thumbnail
tags: [keyword1, keyword2]        # Post tags
---
```

### Site-Level SEO Settings (`_config.yml`)
```yaml
title: "Raki Yoga"                    # Site name
url-pretty: "rakiyoga.de"             # Display URL
keywords: "ayurveda,yoga,health,berlin,consultation"  # Site keywords
title-on-all-pages: true              # Append site name to page titles
```

## Social Media Sharing

### Open Graph Tags
Beautiful Jekyll automatically generates OG tags from front matter:
- `og:title` — from `title` or `share-title`
- `og:description` — from `subtitle` or `share-description`
- `og:image` — from `share-img`, `cover-img`, or `thumbnail-img`
- `og:type` — `article` for posts, `website` for pages

### Twitter Cards
- Large summary card when cover/share image is present
- Standard summary card otherwise
- Configure Twitter handle in `_config.yml`

### Share Links
Enabled in `_config.yml`:
```yaml
share-links-active:
  twitter: true
  facebook: true
  linkedin: false
```

## On-Page SEO Checklist

### For Every Page
- [ ] Descriptive `title` (50-60 characters)
- [ ] Compelling `subtitle` for meta description (150-160 characters)
- [ ] Proper heading hierarchy (single h1 from title)
- [ ] Alt text on all images
- [ ] Internal links to related pages
- [ ] Mobile-responsive content

### For Blog Posts
- [ ] Date in filename (YYYY-MM-DD)
- [ ] Relevant tags (3-5 per post)
- [ ] Feature image (`cover-img` or `thumbnail-img`)
- [ ] Excerpt length appropriate (configured at 50 words)
- [ ] Social sharing enabled

### For the Site
- [ ] `keywords` set in `_config.yml`
- [ ] Custom 404 page exists (`404.html`)
- [ ] CNAME configured for custom domain
- [ ] HTTPS enabled (GitHub Pages default)
- [ ] Sitemap accessible at `/sitemap.xml`

## Keyword Strategy for Raki Yoga
| Primary | Secondary | Long-tail |
|---------|-----------|-----------|
| Ayurveda Berlin | Ayurvedic health consultant | Ayurveda consultation Berlin online |
| Yoga Berlin | Dosha balancing | Personalized Ayurveda treatment plan |
| Ayurvedic recipes | Vata Pitta Kapha | Ayurvedic cooking classes Berlin |
| Holistic health | Natural remedies | Autoimmune disorders Ayurveda |

## Technical SEO
- **URL structure**: Clean URLs via Jekyll permalink (`/:year-:month-:day-:title/`)
- **Canonical URLs**: Handled by GitHub Pages
- **Page speed**: Static HTML = fast; optimize images further
- **Structured data**: Consider adding JSON-LD for LocalBusiness schema
- **Multi-language**: Future opportunity for `hreflang` tags (DE/EN)
