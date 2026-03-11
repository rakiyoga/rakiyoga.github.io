# Example: Adding a New Blog Post

## Goal
Publish a new Ayurveda blog post about seasonal eating.

## Steps

### 1. Create the Post File
Create `2025-03-11-seasonal-eating-spring.md` in `_posts/`:

```markdown
---
layout: post
title: "Spring Eating: Ayurvedic Guide to Seasonal Nutrition"
subtitle: "How to balance Kapha dosha as winter transitions to spring"
tags: [ayurveda, nutrition, seasonal, kapha, detox]
comments: true
social-share: true
cover-img: /assets/img/spring_foods.jpg
thumbnail-img: /assets/img/spring_foods_thumb.jpg
---

As winter melts into spring, Ayurveda teaches us that accumulated **Kapha dosha** begins to liquefy and can cause congestion, lethargy, and allergies. This is the perfect time for a gentle cleanse.

## Vasanta Ritu (Spring Season)

**वसन्त ऋतु** (Vasanta Ritu)
Meaning: The spring season in Ayurvedic seasonal framework (Ritucharya).

During spring, favor:
- **Light, warm foods** to counteract Kapha heaviness
- **Bitter and astringent tastes** (Tikta and Kashaya)
- **Pungent spices** like ginger, black pepper, and turmeric

## Recommended Spring Foods

| Food Group | Include | Reduce |
|-----------|---------|--------|
| Grains | Barley, millet, quinoa | Wheat, rice |
| Vegetables | Leafy greens, radish | Sweet potato, cucumber |
| Spices | Turmeric, ginger, pepper | Heavy sauces |

Embrace the season's natural bounty and let your diet support your body's innate wisdom.

---

*This information is for educational purposes. Please consult a healthcare professional for personalized advice.*
```

### 2. Add Images (optional)
Place cover/thumbnail images in `assets/img/`:
- `spring_foods.jpg` — wide cover image
- `spring_foods_thumb.jpg` — square thumbnail

### 3. Test
```bash
bundle exec jekyll serve --future
# Visit http://localhost:4000 — post should appear in the feed
```

### 4. Verify
- [ ] Post appears on the Wisdom/blog feed page
- [ ] Cover image displays at the top of the post
- [ ] Thumbnail appears in the feed
- [ ] Tags are clickable
- [ ] Social share buttons work
- [ ] Comments section appears
- [ ] Post is properly dated
