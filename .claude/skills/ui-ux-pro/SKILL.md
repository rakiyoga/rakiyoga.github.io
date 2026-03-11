---
name: ui-ux-pro
description: UI/UX design system and best practices for Beautiful Jekyll Ayurveda wellness website
---

# UI/UX Pro Skill

## Overview
Premium design guidelines for the Raki Yoga website. This skill ensures consistent, accessible, and visually appealing design across all pages.

## Design Philosophy
- **Natural & Calming**: Reflect the holistic nature of Ayurveda
- **Clean & Professional**: Build trust for health consultancy services
- **Content-First**: Let educational content shine without visual clutter
- **Accessible**: WCAG 2.1 AA compliance as a goal

## Color System

### Primary Palette
| Name | Hex | Usage |
|------|-----|-------|
| Forest Green | `#2E7D32` | Navbar, footer, primary CTAs |
| Leaf Green | `#4CAF50` | Links, accents |
| Dark Green | `#388E3C` | Hover states |
| Pale Green | `#E8F5E9` | Page background |
| Light Green | `#A5D6A7` | Borders, secondary accents |

### Neutral Palette
| Name | Hex | Usage |
|------|-----|-------|
| Charcoal | `#333333` | Body text |
| White | `#FFFFFF` | Navbar text, footer text |

### Extended Colors (for future use)
| Name | Hex | Dosha Association |
|------|-----|-------------------|
| Warm Gold | `#F9A825` | Pitta |
| Earth Brown | `#8D6E63` | Kapha |
| Sky Blue | `#64B5F6` | Vata |

## Typography

### Font Stack
```css
/* Headings */
font-family: 'Lora', 'Times New Roman', serif;

/* Body */
font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
```

### Scale Guidelines
- **h1**: Page titles — bold, generous spacing
- **h2**: Section headers — clear hierarchy
- **h3**: Subsection headers
- **Body**: 16px base, 1.5 line-height for readability
- **Small**: Captions, disclaimers

## Layout Patterns

### Responsive Breakpoints (Bootstrap 4)
| Breakpoint | Width | Target |
|------------|-------|--------|
| xs | < 576px | Mobile portrait |
| sm | ≥ 576px | Mobile landscape |
| md | ≥ 768px | Tablet |
| lg | ≥ 992px | Desktop |
| xl | ≥ 1200px | Large desktop |

### Content Width
- Max container width: Bootstrap default (1140px at xl)
- Reading width: ~70ch for optimal readability in blog posts

### Expandable Sections Pattern
Used extensively in Ayurveda Fundamentals and Recipes:
```html
<details>
  <summary style="font-weight:bold;">Section Title</summary>
  <p>Content with <b>bold terms</b> and Sanskrit text.</p>
</details>
```

## Image Guidelines
- **Format**: JPEG for photos, PNG for graphics/screenshots
- **Class**: Use `class="pic"` for consistent styling
- **Alt text**: Descriptive, include content context
- **Hosting**: Local (`/assets/img/`) preferred; GitHub CDN for large images
- **Aspect ratio**: Maintain natural proportions
- **Logo**: Square format, displayed as circle via `round-avatar: true`

## Component Patterns

### Navigation Bar
- Forest green background (`#2E7D32`)
- White text with light green hover
- Round avatar logo (left)
- 6 navigation items matching content pages

### Footer
- Matches navbar color
- Social media icons (Font Awesome)
- Copyright notice

### Blog Post Cards (Home Layout)
- Post title, excerpt (50 words), tags
- Chronological ordering with pagination (5 per page)

### Forms
- Contact form (`_includes/contact-form.html`)
- Clean input fields with green accent on focus

## Accessibility Checklist
- [ ] All images have descriptive `alt` attributes
- [ ] Sufficient color contrast (4.5:1 for text)
- [ ] Keyboard navigable interactive elements
- [ ] Semantic HTML structure (`<nav>`, `<main>`, `<footer>`)
- [ ] Focus indicators visible
- [ ] No auto-playing media
- [ ] Readable font sizes (≥16px body)

## Performance Guidelines
- Static site: inherently fast
- Minimize external CDN dependencies
- Optimize images before upload (compress JPEGs)
- Leverage browser caching via GitHub Pages headers
- Consider lazy loading for below-fold images

## Design Enhancement Opportunities
1. **Micro-animations**: Subtle hover effects on cards and links
2. **Dosha color coding**: Use extended palette for Vata/Pitta/Kapha content
3. **Dark mode**: Optional dark theme toggle
4. **Custom icons**: SVG icons for Ayurveda concepts (doshas, elements)
5. **Hero sections**: Full-width cover images on key pages
