# Claude Design Integration
**Load and Geaux Portable Storage — Design System Bridge**

**Date:** July 22, 2026  
**Status:** ✅ Integrated  
**Claude Design Project:** https://claude.ai/design/p/4ef4b296-b699-486a-aad2-bf96981a5892

---

## Overview

Load and Geaux now has a **dual-system design architecture**:

1. **DESIGN.md (this repo)** — Complete visual system specifications (colors, typography, spacing, components, dark mode, accessibility)
2. **Claude Design Project** — Production-ready component library, templates, and social media toolkit

**Both systems are aligned and source the same brand fundamentals.** This document bridges them.

---

## What's in Claude Design

The Claude Design project contains:

### Components
- **Core:** Button (4 variants), Card (accent bar option)
- **Brand:** LogoLockup (green/white), Badge (4 styles, pill option)
- **Social:** Stat (big number + label), QuoteCard (reviews w/ stars), ContactBar (phone/site footer), PhotoFrame (photo + scrim protection)

### Templates (Landscape 1200×628 + 9:16 1080×1920)
- **Promo / Offer** — headline, CTA, product photo
- **Testimonial / Review** — 5-star customer quote
- **Storage Tip / Educational** — numbered how-to points
- **Stat / Infographic** — big stats on green field
- **Announcement / Photo Hero** — headline over full-bleed photo

### Tokens & Guidelines
- **Colors:** Primary (Forest Green), Accent (State Green), Neutrals, Semantic
- **Typography:** Poppins (display), Inter (body), monospace (data)
- **Spacing:** 8px scale with safe-area padding for social
- **Effects:** Shadows, scrim overlays, corners, transitions
- **Photography:** Container photos, truck, capitol, real scenarios

### Specifications
- **Brand rule:** No illustrations/clip art of real objects (containers, trucks)—only real photography
- **Imagery scrim:** Charcoal scrim for white text, branded green scrim for photos
- **Motion:** 200ms ease; respect `prefers-reduced-motion`
- **Safe areas:** 64px (landscape), 80px (9:16 stories)

---

## Alignment: DESIGN.md ↔ Claude Design

| Element | DESIGN.md | Claude Design | Match |
|---------|-----------|---------------|-------|
| **Primary Color** | Forest Green #2D5016 | Forest Green #2D5016 | ✅ |
| **Accent Color** | State Green #004D40 | State Green #004D40 | ✅ |
| **Off-White** | #FAF9F7 | #FAF9F7 | ✅ |
| **Dark Text** | Charcoal #1F2937 | Charcoal #1F2937 | ✅ |
| **Display Font** | Inter Bold / Poppins | Poppins 700/800 | ✅ |
| **Body Font** | Inter | Inter 400/600 | ✅ |
| **Spacing Scale** | 8px multiples | 8px multiples | ✅ |
| **Border Radius** | 4px (components), 8px (media) | 4px (buttons/cards), 8px (media) | ✅ |
| **Dark Mode** | Full CSS custom properties | Included in styles.css | ✅ |
| **Accessibility** | WCAG AA (4.5:1 contrast) | Spec'd in guidelines | ✅ |
| **Photography Rule** | Real photos, no clip art | Real photos only | ✅ |

**All foundations match 1:1.** Components in Claude Design implement the specs in DESIGN.md.

---

## Using Both Systems

### For Site Refresh (DESIGN.md + New Components)
1. **Reference DESIGN.md** for all specifications
2. **Build HTML components** following the detailed specs
3. **Implement CSS** using the spacing scale and color tokens
4. **Test** in light + dark modes
5. **Verify** accessibility (WCAG AA)

→ **Output:** Production-ready website HTML/CSS

### For Social Media (Claude Design Templates)
1. **Open Claude Design project**
2. **Choose a template** (promo, testimonial, tip, stat, announcement)
3. **Select variant** (landscape 1200×628 or story 1080×1920)
4. **Swap in copy and photos** from real project
5. **Export** as PNG/JPEG for posting

→ **Output:** Brand-accurate social graphics ready to post

### For Marketing Materials (Claude Design Components)
1. **Grab components** (Button, Card, Badge, LogoLockup)
2. **Use in Figma/mockups** or export HTML
3. **Follow component specs** for styling
4. **Ensure brand consistency** across collateral

→ **Output:** Cohesive marketing materials

---

## File Locations

### DESIGN.md System (GitHub)
```
load-and-geaux-portable-storage/
├── DESIGN.md                      # Full specifications
├── DESIGN-QUICK-REFERENCE.md      # Cheat sheet
├── brand-style-guide.md           # Voice & tone
├── BACKLOG.md                     # Work items
└── docs/
    ├── DESIGN-SYSTEM-OVERVIEW.md
    ├── AUDIT-PHASE-2-REPORT.md
    └── CLAUDE-DESIGN-INTEGRATION.md (this file)
```

### Claude Design System (Hosted)
```
claude.ai/design/p/4ef4b296-b699-486a-aad2-bf96981a5892
├── components/
│   ├── core/          (Button, Card)
│   ├── brand/         (LogoLockup, Badge)
│   └── social/        (Stat, QuoteCard, ContactBar, PhotoFrame)
├── templates/
│   ├── promo-offer/
│   ├── testimonial/
│   ├── storage-tip/
│   ├── stat-highlight/
│   └── announcement/
├── tokens/            (CSS custom properties)
├── guidelines/        (Color, Type, Spacing, Brand)
├── assets/            (Logos, photos, favicon)
└── readme.md          (System overview)
```

---

## Integration Workflow

### When Adding a New Component

1. **Design it in DESIGN.md** with full specs (colors, sizing, states)
2. **Build it in Claude Design** using the components library
3. **Export to HTML/CSS** from Claude Design
4. **Add to website** and/or social templates
5. **Link both docs** so future work stays in sync

### When Updating the Brand (e.g., color change)

1. **Update the hex value** in DESIGN.md color section
2. **Update Claude Design tokens** (colors.css)
3. **Re-export components** from Claude Design
4. **Update website CSS** with new tokens
5. **Verify** all templates and pages render correctly

### When Creating Social Content

1. **Open Claude Design project**
2. **Choose template** for platform (Instagram, Facebook, etc.)
3. **Customize copy/photos** for the campaign
4. **Export** as image
5. **Post** with hashtags and caption (follow brand-style-guide.md for tone)

---

## Token Access

Both systems use the same token values. For reference:

### Colors
```css
--color-forest-green: #2D5016;        /* Primary */
--color-state-green: #004D40;          /* Accent */
--color-off-white: #FAF9F7;             /* Background */
--color-dark-charcoal: #1F2937;        /* Dark text */
--color-steel-gray: #6B7280;           /* Body text */
--color-success: #10B981;               /* Positive feedback */
--color-warning: #F59E0B;               /* Alerts & stars */
--color-error: #EF4444;                 /* Errors */
--color-info: #3B82F6;                  /* Info */
```

### Typography
```css
--font-display: "Poppins", sans-serif;  /* Headlines */
--font-body: "Inter", sans-serif;       /* Body copy */
--font-mono: monospace;                 /* Data/pricing */

--font-size-h1: 40px;
--font-size-h2: 32px;
--font-size-h3: 24px;
--font-size-body: 16px;
--font-size-small: 14px;
```

### Spacing
```css
--space-xs: 4px;
--space-sm: 8px;
--space-md: 16px;
--space-lg: 24px;
--space-xl: 32px;
--space-2xl: 48px;
--space-3xl: 64px;
```

---

## Skill Invocation

To use Load and Geaux design system in Claude Code:

```
/load-and-geaux-design
```

This skill gives you access to:
- Component specs and code
- Template examples (landscape + 9:16)
- Brand guidelines and rules
- Real photography and assets
- Typography and color tokens

---

## Maintenance & Updates

### Quarterly Review
- Check if design specs need refinement
- Update DESIGN.md with any brand changes
- Re-sync Claude Design tokens
- Test all templates render correctly

### When Adding New Pages to Site
1. Reference DESIGN.md for component specs
2. Use spacing scale for layout
3. Test in light + dark modes
4. Verify WCAG AA contrast
5. Link components to Claude Design source

### When Refreshing Social Content
1. Pull latest templates from Claude Design
2. Verify colors match current brand
3. Use real photography from assets/
4. Follow copy guidelines from brand-style-guide.md
5. Export and schedule

---

## Quick Links

- **GitHub Repo:** https://github.com/clintsanchez/load-and-geaux-portable-storage
- **Claude Design Project:** https://claude.ai/design/p/4ef4b296-b699-486a-aad2-bf96981a5892
- **Brand Guide:** [brand-style-guide.md](../../brand-style-guide.md)
- **Full Design System:** [DESIGN.md](../../DESIGN.md)
- **Quick Reference:** [DESIGN-QUICK-REFERENCE.md](../../DESIGN-QUICK-REFERENCE.md)

---

## What's Next

### Phase 3: Component Library Implementation
- [ ] Build HTML/CSS components from DESIGN.md specs
- [ ] Create reusable React/Vue/vanilla components
- [ ] Add to WordPress theme (if applicable)
- [ ] Document component API for developers

### Phase 4: Site Refresh
- [ ] Apply design system to new homepage
- [ ] Create service page templates
- [ ] Implement blog component system
- [ ] Optimize performance and accessibility

### Phase 5: Marketing Automation
- [ ] Set up social media posting schedule
- [ ] Create email templates using brand fonts/colors
- [ ] Build landing page variations (A/B testing)
- [ ] Document analytics tracking

---

## Document Metadata

**Created:** July 22, 2026  
**Status:** Integration Complete  
**Owner:** Clint Sanchez / BlakSheep Creative  
**Last Updated:** July 22, 2026

---

**Both systems are live and ready for implementation. Site refresh can proceed with confidence in visual consistency.**
