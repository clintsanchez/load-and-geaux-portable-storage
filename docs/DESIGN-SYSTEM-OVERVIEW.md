# Design System Overview — Site Refresh
**Load and Geaux Portable Storage**

**Created:** July 22, 2026  
**Status:** ✅ Complete (v1.0)  
**Next Phase:** Component Library & Mockups

---

## What We Built

A **comprehensive, distinctive design system** for Load and Geaux's upcoming site refresh. This isn't a generic template—it's built specifically for a Baton Rouge-based portable storage company that values clarity, warmth, and authenticity.

---

## Philosophy

Every design choice reflects the brand's DNA:
- **Professional + Friendly + Locally Rooted**
- **Clarity over cleverness** (customers need to understand storage solutions quickly)
- **Warmth over minimalism** (Louisiana-specific palette, not tech-cold)
- **Real over stylized** (genuine product photography, no clip art)
- **Functional first** (every component serves a job)

---

## System Components

### 1. Color Palette
**Primary:**
- Forest Green (#2D5016) — authoritative, warm, locally-rooted
- Warm Off-White (#FAF9F7) — grounded, not sterile
- Steel Gray (#6B7280) — warm gray for body text

**Accent & Semantic:**
- Louisiana State Green (#004D40) — hover states, highlights
- Success/Warning/Error colors for feedback states
- Dark Mode variants for nighttime reading

**Why this palette:**
The green family echoes Louisiana's bayou and natural landscape. The warm off-white grounds the design without feeling corporate. Steel gray pairs beautifully with Forest Green and reads as deliberately chosen, not defaulted.

### 2. Typography System
**Display Face:** Warm, geometric sans-serif (Inter Bold, Poppins, Grotesk-style)
- Used for H1, H2, major headings
- Confident without being cold

**Body Face:** Highly legible, warm-toned sans (Inter, Segoe UI)
- 16px desktop, 14px mobile
- 1.6+ line-height for breathing room
- Max 65 characters wide for readability

**Utility Face:** Monospace for pricing, specs, data (Courier, Menlo)
- Used for service details, cost breakdowns

**Why this pairing:**
Display and body faces are distinctly different, preventing visual monotony. Both lean warm (not tech-neutral), reinforcing the friendly + professional voice.

### 3. Spacing System
8px-based scale:
- 4px (xs), 8px (sm), 16px (md), 24px (lg), 32px (xl), 48px (2xl), 64px (3xl)
- Predictable, scalable, easy to implement

**Container:** 1200px max (desktop), full-width + padding (mobile)  
**Section spacing:** 64px vertical between major sections  
**Mobile padding:** 16px left/right  

**Why 8px multiples:**
Industry standard, scales consistently across devices, reduces design debt.

### 4. Component Library
Complete specifications for:
- **Buttons** (Primary, Secondary, Tertiary)
- **Form Fields** (input, label, validation states)
- **Cards** (standard, accent variant, service card)
- **Navigation** (primary nav, footer, mobile)
- **CTA Sections** (hero banner, in-page CTA)
- **Testimonials** (quote cards with ratings)
- **Status Messages** (success, warning, error, info)

**Every component includes:**
- Exact hex colors
- Padding, margins, border-radius
- Font size, weight, line-height
- Hover, focus, active, disabled states
- Dark mode variants

### 5. Photography Guidelines
**Use:**
✅ Real product photos (containers in actual customer scenarios)  
✅ Actual delivery vehicles and equipment  
✅ Local Baton Rouge landmarks  
✅ Customer lifestyle photography  
✅ AI-generated from client's own photos  
✅ Professional infographics with brand colors  

**Never:**
❌ Clip art or hand-drawn SVGs of real objects  
❌ Overly stylized cartoon imagery  
❌ Generic stock photos  
❌ Unbranded storage imagery  

### 6. Responsive Design
Three main breakpoints:
- **Mobile:** < 640px (1 column, full-width)
- **Tablet:** 640–1024px (2 column, narrow)
- **Desktop:** > 1024px (2–3 columns, 1200px max)

### 7. Accessibility
- WCAG AA contrast compliance (4.5:1 for text)
- Visible focus states on all interactive elements
- Dark mode support with CSS custom properties
- Respect for `prefers-reduced-motion`
- Minimum 44px touch targets on mobile

### 8. Dark Mode
Complete dark mode palette:
- Background: #111827 (deep charcoal, not pure black)
- Surface: #1F2937
- Text: #F3F4F6 (light gray)
- Accent: #86EFAC (lightened green for visibility)

Implemented via CSS custom properties, with user toggle support.

---

## What Makes This System Distinctive

### 1. Louisiana-Specific, Not Generic
The green palette echoes the state's natural landscape. Typography and spacing feel warm and approachable, not tech-neutral. This isn't a system that could work for any SaaS—it's built for a Baton Rouge storage company.

### 2. Clarity First
No flashy animations, no over-designed components. Every button, card, and form field prioritizes ease of use. The design gets out of the way of the content.

### 3. Warmth Over Minimalism
The color choices and typography pair feel intentional, not defaulted. Warm off-white instead of pure white. Steel gray that's actually warm-toned. Typography that's approachable, not sterile.

### 4. Authentic Imagery
Real photos of containers, trucks, and Baton Rouge landmarks. No clip art, no stock photo clichés. Customers see themselves in the imagery.

### 5. Functional Components
Every component has a job: buttons signal action, cards organize information, forms capture data. Design serves function, not the other way around.

---

## Documents in This System

### 📘 Full System (DESIGN.md)
659 lines covering:
- Color palette (light + dark modes)
- Typography system (scale, pairings, rules)
- Layout & spacing (grid, breakpoints, responsive)
- Component specs (buttons, forms, cards, navigation, CTAs)
- Imagery guidelines
- Accessibility standards
- CSS custom properties for implementation
- Implementation checklist

### 📋 Quick Reference (DESIGN-QUICK-REFERENCE.md)
One-page cheat sheet:
- Color palette at a glance
- Type scale and fonts
- Spacing scale
- Components in shorthand
- Dark mode CSS pattern
- Accessibility checklist
- Common mistakes to avoid

### 📖 Brand Guide (brand-style-guide.md)
Tone, voice, and content standards:
- Brand personality and voice
- Writing guidelines (headlines, body copy, CTAs)
- Social media tone
- Email and marketing copy
- Logo usage
- Imagery philosophy

---

## How to Use This System

### For Designers
1. Reference DESIGN.md before creating mockups
2. Use exact colors, typography, spacing from system
3. When creating new components, follow the same principles
4. Test all designs in light AND dark modes
5. Check color contrast (WCAG AA minimum)
6. Use the component specs as templates

### For Developers
1. Define CSS custom properties from the palette section
2. Implement spacing using 8px multiples
3. Build components matching the specifications
4. Test responsive behavior at all breakpoints
5. Ensure keyboard navigation works
6. Validate HTML/CSS for standards compliance
7. Implement dark mode with CSS properties

### For Content Creators
1. Follow brand voice guidelines (brand-style-guide.md)
2. Use benefit-focused headlines
3. Keep body text 14–16px minimum
4. Use active voice and second person
5. Provide alt text for all images
6. Follow CTA copy guidelines

---

## Next Steps

### Phase 1: Component Library
- Create reusable HTML/CSS components based on system
- Build component variations (buttons, cards, forms, etc.)
- Test components in isolation and in context
- Document component usage with examples

### Phase 2: Site Mockups
- Create high-fidelity mockups for homepage, service pages, blog
- Apply system components to real content
- Test layouts at all breakpoints
- Gather feedback and refine

### Phase 3: Development
- Implement system in WordPress theme/template
- Create reusable component blocks
- Set up dark mode toggle
- Optimize images and performance
- Run accessibility audit

### Phase 4: Launch & Iteration
- Deploy site refresh
- Monitor performance metrics
- Gather user feedback
- Refine system based on real-world usage

---

## Design System Statistics

| Metric | Value |
|--------|-------|
| **Colors defined** | 13 (+ dark mode variants) |
| **Typography scale levels** | 6 (H1–H4, Body, Small) |
| **Spacing scale tokens** | 7 (4px to 64px) |
| **Components specified** | 12 major categories |
| **Responsive breakpoints** | 3 (mobile, tablet, desktop) |
| **Accessibility standards** | WCAG AA (4.5:1 contrast) |
| **Dark mode support** | ✅ Full coverage |

---

## Key Principles to Remember

**Clarity over cleverness** — Customers need to find storage solutions quickly, not decipher clever design.

**Warmth over minimalism** — Louisiana-specific palette and typography that feels approachable.

**Real over stylized** — Genuine product photography, authentic customer stories, no generic imagery.

**Functional first** — Every component serves a purpose. Design supports content, not the reverse.

**Consistency matters** — Same colors, same spacing, same typography everywhere builds trust.

---

## File Locations

- **Full System:** `DESIGN.md` (read this first)
- **Quick Reference:** `DESIGN-QUICK-REFERENCE.md` (desktop cheat sheet)
- **Brand Voice:** `brand-style-guide.md` (tone and writing)
- **Logos:** `brand/logos/` (30+ variations)
- **Color swatches:** Copy hex values from DESIGN.md

---

## Questions to Ask When Designing

1. **Does this follow the system?** (Colors, typography, spacing, components)
2. **Is this warm or sterile?** (Should feel Louisiana-rooted, not tech-cold)
3. **Is this authentic?** (Real imagery, not stock photos or clip art)
4. **Does this serve the customer?** (Not designer ego)
5. **Does this work in dark mode?** (Test both themes)
6. **Is this accessible?** (4.5:1 contrast, visible focus states)
7. **Is this simple enough?** (No unnecessary flourishes)

---

## Success Metrics

A successful site refresh using this system will:
- ✅ Load fast (optimized images, clean code)
- ✅ Feel distinctive (not templated or generic)
- ✅ Be accessible (WCAG AA compliant)
- ✅ Convert well (clear CTAs, intuitive forms)
- ✅ Work everywhere (responsive across devices)
- ✅ Feel warm and approachable (Louisiana-rooted)
- ✅ Maintain brand consistency (same system throughout)

---

## Version Control

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Jul 22, 2026 | Initial design system for site refresh |

Future updates will track refinements as mockups and components are built.

---

## Support & Feedback

This design system is a living document. As the site refresh progresses:
- Refine components based on implementation feedback
- Add new components as needed
- Update dark mode palette based on user testing
- Document any exceptions or special cases

**Document owner:** Design Team / Clint Sanchez  
**Last updated:** July 22, 2026

---

**END OF DESIGN SYSTEM OVERVIEW**

The system is ready. Next step: Build component library and create site mockups.
