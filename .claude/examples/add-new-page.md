# Example: Adding a New Content Page

## Goal
Add a new "Yoga" page to the site navigation.

## Steps

### 1. Create the Page File
Create `7_yoga.md` in the project root:

```markdown
---
layout: page
title: Yoga
subtitle: Ancient practices for modern well-being
---

**Discover the transformative power of yoga**

Yoga is one of the six schools of Hindu philosophy (Shad Darshana). At Raki Yoga, we integrate traditional Hatha and Raja yoga practices with Ayurvedic principles for personalized guidance.

<details>
<summary style="font-weight:bold;">Ashtanga: The 8 Limbs of Yoga</summary>

<p>
<b>Yama</b>: Ethical restraints<br>
<b>Niyama</b>: Personal observances<br>
<b>Asana</b>: Physical postures<br>
<b>Pranayama</b>: Breath control<br>
<b>Pratyahara</b>: Sense withdrawal<br>
<b>Dharana</b>: Concentration<br>
<b>Dhyana</b>: Meditation<br>
<b>Samadhi</b>: Absorption
</p>

</details>
```

### 2. Add to Navigation
Edit `_config.yml`:

```yaml
navbar-links:
  About me: "1_aboutme"
  Wisdom: "2_wisdom"
  Ayurveda: "3_ayurveda_fundamentals"
  Recipes: "4_recipes"
  Consultation: "5_consultation"
  Contact: "6_contact"
  Yoga: "7_yoga"            # ← Add this line
```

### 3. Add Images (if needed)
Place images in `assets/img/` and reference them:
```html
<img src="/assets/img/yoga_pose.jpg" alt="Traditional yoga asana" class="pic">
```

### 4. Test
```bash
bundle exec jekyll serve
# Visit http://localhost:4000/7_yoga
```

### 5. Verify
- [ ] Page loads at correct URL
- [ ] Navigation link appears and works
- [ ] Content renders properly
- [ ] Images display correctly
- [ ] Mobile layout is responsive
