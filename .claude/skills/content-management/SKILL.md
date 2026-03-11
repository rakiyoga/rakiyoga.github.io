---
name: content-management
description: Creating and managing Ayurveda-focused content pages and blog posts with proper structure and SEO
---

# Content Management Skill

## Overview
Guidelines for creating, editing, and organizing content for the Raki Yoga Ayurveda website. Covers page creation, blog post authoring, content formatting, and Ayurveda-specific terminology.

## Page Creation

### New Content Page
1. Create `N_pagename.md` in the project root
2. Set the number prefix to control navbar ordering:
   - `1_` = About, `2_` = Wisdom, `3_` = Ayurveda, etc.
3. Add front matter:
   ```yaml
   ---
   layout: page
   title: "Page Title"
   subtitle: "Brief description"
   ---
   ```
4. Register in `_config.yml` navbar:
   ```yaml
   navbar-links:
     "Display Name": "N_pagename"
   ```

### New Blog Post
1. Create `YYYY-MM-DD-title-with-dashes.md` in `_posts/`
2. Add front matter:
   ```yaml
   ---
   layout: post
   title: "Post Title"
   subtitle: "Brief description"
   tags: [ayurveda, health, dosha]
   comments: true
   social-share: true
   ---
   ```

## Content Formatting

### Expandable Sections (for educational content)
```html
<details>
  <summary style="font-weight:bold;">Topic Title</summary>
  <p>Content paragraph with <b>key terms</b> highlighted.</p>
</details>
```

### Images
```html
<!-- Local image -->
<img src="/assets/img/filename.jpg" alt="Descriptive alt text" class="pic">

<!-- Markdown image -->
![alt text](/assets/img/filename.jpg)

<!-- GitHub-hosted image -->
<img src="https://github.com/user-attachments/assets/..." alt="description" class="pic">
```

### Tables
Standard markdown tables for data like food classifications:
```markdown
| Category | Sattvic | Rajasic | Tamasic |
|----------|---------|---------|---------|
| Fruits   | Mango   | Lemon   | Avocado |
```

### Sanskrit Text
Always provide trilingual format where appropriate:
```markdown
**संस्कृत** (Sanskrit transliteration)
Meaning: English translation (German translation)
```

## Ayurveda Terminology Reference

### Three Doshas
| Dosha | Elements | Governs |
|-------|----------|---------|
| **Vata** (वात) | Air + Ether | Movement, circulation, respiration |
| **Pitta** (पित्त) | Fire + Water | Metabolism, digestion, transformation |
| **Kapha** (कफ) | Earth + Water | Structure, stability, immunity |

### Five Elements (Pancha Mahabhuta)
- **Akasha** (आकाश) — Ether/Space
- **Vayu** (वायु) — Air
- **Agni** (अग्नि) — Fire
- **Jala** (जल) — Water
- **Prithvi** (पृथ्वी) — Earth

### Three Gunas
- **Sattva** — Clarity, balance, harmony
- **Rajas** — Activity, stimulation, passion
- **Tamas** — Inertia, heaviness, resistance

### Six Tastes (Shad Rasa)
Sweet (Madhura), Sour (Amla), Salty (Lavana), Pungent (Katu), Bitter (Tikta), Astringent (Kashaya)

## SEO Guidelines for Content
- Use descriptive, keyword-rich titles
- Include subtitle for meta description
- Use proper heading hierarchy (h1 from title, h2/h3 in content)
- Alt text on all images with relevant keywords
- Internal linking between related pages
- Tags on blog posts for categorization

## Content Review Checklist
- [ ] Front matter complete and correct
- [ ] Sanskrit terms include transliteration and meaning
- [ ] Images have alt text
- [ ] Health claims include disclaimer reference
- [ ] Content is factually accurate per Ayurvedic texts
- [ ] Links work (internal and external)
- [ ] Expandable sections use consistent `<details>` format
