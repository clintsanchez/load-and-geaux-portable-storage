# Design System — Quick Reference
**Load and Geaux Portable Storage Site Refresh**

A one-page cheat sheet for designers and developers. See DESIGN.md for full specifications.

---

## Color Palette

### Primary Colors
```
Forest Green:          #2D5016  (Primary brand, headings, CTAs)
Warm Off-White:        #FAF9F7  (Page backgrounds)
Steel Gray:            #6B7280  (Body text)
Light Gray:            #F3F4F6  (Borders, dividers)
Dark Charcoal:         #1F2937  (Dark text)
Louisiana State Green: #004D40  (Hover states, accents)
```

### Semantic Colors
```
Success Green:         #10B981  (Confirmations)
Warning Amber:         #F59E0B  (Alerts)
Error Red:             #EF4444  (Errors)
Info Blue:             #3B82F6  (Information)
```

### Dark Mode
```
Background:   #111827  (Deep charcoal)
Surface:      #1F2937  (Cards/containers)
Text:         #F3F4F6  (Primary text)
Text Muted:   #9CA3AF  (Secondary text)
Borders:      #374151  (Subtle dividers)
Accent:       #86EFAC  (Lightened green)
```

---

## Typography

### Type Scale

| Element | Mobile | Desktop | Weight |
|---------|--------|---------|--------|
| H1      | 32px   | 40px    | Bold   |
| H2      | 24px   | 32px    | Bold   |
| H3      | 20px   | 24px    | SemiBold |
| Body    | 14px   | 16px    | Regular |
| Small   | 12px   | 14px    | Regular |

### Fonts
- **Display:** Bold sans-serif (Inter Bold, Poppins Bold, Grotesk)
- **Body:** Clean sans-serif (Inter, Segoe UI, -apple-system)
- **Utility:** Monospace (Courier New, Menlo) for data/pricing

### Rules
- Headings: Use `text-wrap: balance`
- Body text: Max 65 characters wide, 1.6+ line-height
- Links: Forest Green with underline; hover to Louisiana State Green
- Labels: SemiBold, 0.05em letter-spacing

---

## Spacing Scale

```
xs:    4px    (rarely used)
sm:    8px    (small gaps)
md:    16px   (standard spacing)
lg:    24px   (section padding)
xl:    32px   (large gaps)
2xl:   48px   (major separation)
3xl:   64px   (between sections)
```

**Container:** 1200px max (desktop), 100% + 16px padding (mobile)  
**Section spacing:** 64px vertical  
**Grid gap:** Use CSS `gap` property, not margins

---

## Components at a Glance

### Primary Button
```css
background: #2D5016
color: #FFFFFF
padding: 12px 24px (mobile) / 14px 32px (desktop)
border-radius: 4px
hover: background #004D40
focus: outline 2px solid #2D5016, offset 4px
```

### Secondary Button
```css
background: transparent
border: 2px solid #2D5016
color: #2D5016
padding: 12px 24px / 14px 32px
hover: background #FAF9F7, border #004D40
```

### Form Input
```css
background: #FFFFFF
border: 1px solid #F3F4F6
padding: 10px 12px
border-radius: 4px
focus: border #2D5016, box-shadow 0 0 0 3px rgba(45,80,22,0.1)
```

### Card
```css
background: #FFFFFF
border: 1px solid #F3F4F6
border-radius: 4px
padding: 24px
box-shadow: 0 1px 3px rgba(0,0,0,0.05)
accent variant: 4px left border in #2D5016
```

### Hero Section
```css
background: #2D5016 or hero image
color: #FFFFFF
padding: 64px vertical
image: Real product photography (container, truck, landmark)
CTA: Primary button
```

---

## Images & Photography

✅ Use:
- Real product photos (containers in actual customer scenarios)
- Local Baton Rouge landmarks and scenery
- Customer lifestyle photography
- AI-generated images from client's own photos
- Professional infographics with brand color accents

❌ Don't use:
- Clip art or hand-drawn SVGs of real objects
- Overly stylized cartoon imagery
- Generic stock photos
- Unbranded storage imagery

**Sizes:**
- Hero: 1200×600px (desktop) / 600×400px (mobile)
- Card: 400×300px (4:3 ratio)
- Optimize: <150KB for hero, <50KB for cards

---

## Responsive Breakpoints

```
Mobile:   < 640px    (1 column, full-width)
Tablet:   640–1024px (2 column, narrow)
Desktop:  > 1024px   (2–3 columns, 1200px max)
```

---

## Accessibility Checklist

- ✓ Contrast ratio 4.5:1 for text (WCAG AA)
- ✓ Focus states on all interactive elements (2px outline)
- ✓ Alt text on all images
- ✓ Semantic HTML (button, a, form, input, etc.)
- ✓ `prefers-reduced-motion` respected
- ✓ Dark mode implemented and tested
- ✓ Touch targets minimum 44px (mobile)
- ✓ Links underlined (not just color)

---

## Dark Mode Implementation

Redefine CSS custom properties at media query:

```css
:root {
  --bg-primary: #FAF9F7;
  --text-primary: #1F2937;
  --accent: #2D5016;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #111827;
    --text-primary: #F3F4F6;
    --accent: #86EFAC;
  }
}
```

Then allow theme toggle to override:
```css
:root[data-theme="dark"] { /* dark mode overrides */ }
:root[data-theme="light"] { /* light mode overrides */ }
```

---

## Logo & Branding

- **Primary:** Horizontal green logo on light backgrounds
- **Alternate:** White logo on Forest Green backgrounds
- **Minimum size:** 120px wide
- **Clearspace:** 20px margin on all sides
- **Never:** Stretch, distort, change colors, or use outdated versions

---

## Button Text Examples

❌ Poor:  "Click here," "Submit," "Process"  
✅ Good: "Get a free quote," "Schedule delivery," "Explore sizes," "Request a quote"

---

## Shadows

**Card:** `0 1px 3px rgba(0,0,0,0.08), 0 1px 2px rgba(0,0,0,0.04)`  
**Medium:** `0 4px 12px rgba(0,0,0,0.12), 0 2px 4px rgba(0,0,0,0.08)`  
**Large:** `0 20px 25px rgba(0,0,0,0.15), 0 10px 10px rgba(0,0,0,0.05)`

---

## Form Validation

**Success:** Green left border, Success Green icon, light green background  
**Warning:** Amber left border, Warning Amber icon, light amber background  
**Error:** Red left border, Error Red icon, light red background + specific error message  

Example: "Phone number must include area code" (not "Invalid input")

---

## Common Mistakes to Avoid

- ❌ Using pure white (#FFFFFF) as background (use #FAF9F7)
- ❌ Using pure black (#000000) for text (use #1F2937)
- ❌ Mixing multiple accent colors (stick to Forest Green)
- ❌ Skipping dark mode
- ❌ Focus states that are invisible
- ❌ Text <14px without good reason
- ❌ Generic stock photography
- ❌ Over-designed components (keep it simple)

---

## File Locations

- **Full system:** DESIGN.md (complete specifications)
- **Brand guide:** brand-style-guide.md (tone and voice)
- **Logo files:** brand/logos/ (30+ variations)
- **CSS properties:** Defined in component HTML files
- **Component specs:** See "Components at a Glance" above

---

## Questions?

1. Check DESIGN.md for full specifications
2. Review brand-style-guide.md for tone and writing
3. Look at component specifications above
4. When in doubt, prioritize clarity and warmth

---

**Last Updated:** July 22, 2026  
**Design System Version:** 1.0  
**For:** Load and Geaux Portable Storage Site Refresh
