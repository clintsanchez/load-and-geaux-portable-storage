# Load and Geaux Design System
**Version 1.0 — Site Refresh**

**Last Updated:** July 22, 2026  
**Created for:** Load and Geaux Portable Storage Site Refresh  
**Audience:** Design team, developers, content creators

---

## Philosophy

This design system reflects Load and Geaux's brand DNA: **Professional, Friendly, Locally Rooted**. Every design decision—color, typography, layout, component—should feel like it comes from a Baton Rouge-based company that knows portable storage inside and out, without corporate sterility.

The system prioritizes:
- **Clarity over cleverness** — Customers need to understand storage solutions quickly
- **Warmth over minimalism** — Louisiana-specific palette and proportions
- **Real over stylized** — Genuine product photography and customer stories
- **Functional first** — Every component serves a job before it looks good

---

## Color System

### Primary Palette

| Name | Hex | RGB | Use | Notes |
|------|-----|-----|-----|-------|
| **Forest Green** | #2D5016 | 45, 80, 22 | Primary brand color, headings, CTAs | Deep, warm, authoritative |
| **Warm Off-White** | #FAF9F7 | 250, 249, 247 | Page backgrounds, card backgrounds | Slightly warm—feels grounded, not sterile |
| **Steel Gray** | #6B7280 | 107, 114, 128 | Body text, secondary copy | Warm gray; pairs well with Forest Green |
| **Light Gray** | #F3F4F6 | 243, 244, 246 | Borders, dividers, subtle backgrounds | Neutral but slightly cool for contrast |

### Accent Palette

| Name | Hex | RGB | Use | Notes |
|------|-----|-----|-----|-------|
| **Louisiana State Green** | #004D40 | 0, 77, 64 | Hover states, secondary accents, highlights | Slightly darker/cooler than Forest Green |
| **Dark Charcoal** | #1F2937 | 31, 41, 55 | Dark text, secondary headings | Not pure black—warmer, more readable |

### Semantic Colors

| Name | Hex | Use | Notes |
|------|-----|-----|-------|
| **Success Green** | #10B981 | Form validation, confirmations | Distinct from brand green—clearly positive |
| **Warning Amber** | #F59E0B | Alerts, cautions, important info | Warm, high-contrast |
| **Error Red** | #EF4444 | Errors, critical alerts, destructive actions | Clear and legible |
| **Info Blue** | #3B82F6 | Information, tips, secondary CTAs | Cool enough to distinguish from brand green |

### Dark Mode Palette

When `prefers-color-scheme: dark` or `data-theme="dark"`:

| Token | Light | Dark | Notes |
|-------|-------|------|-------|
| **Background** | #FAF9F7 | #111827 | Deep charcoal, not pure black—better for eyes |
| **Surface** | #FFFFFF | #1F2937 | Cards and containers adjust accordingly |
| **Text Primary** | #1F2937 | #F3F4F6 | Reverses for readability |
| **Text Secondary** | #6B7280 | #9CA3AF | Slightly lighter gray in dark mode |
| **Border** | #F3F4F6 | #374151 | Subtle dividers work on dark background |
| **Accent** | #2D5016 | #86EFAC | Lightened green for visibility on dark |

### Color Usage Rules

- **Forest Green (#2D5016)** for:
  - Primary CTAs (buttons with full background)
  - Main headings (H1, H2)
  - Logo and brand elements
  - Active tab states
  - Primary form field borders on focus

- **Louisiana State Green (#004D40)** for:
  - Hover states on Forest Green elements
  - Secondary interactive states
  - Accent borders or left-side bars on cards
  - Highlights within content

- **Steel Gray (#6B7280)** for:
  - Body text (16px and smaller)
  - Secondary headings (H3, H4)
  - Caption text and metadata
  - Disabled states

- **Off-White (#FAF9F7)** for:
  - Page backgrounds
  - Card backgrounds
  - Content areas that need visual separation

- **Never:**
  - Use pure white (#FFFFFF) as main background in light mode
  - Use pure black (#000000) for text
  - Layer multiple accent colors—keep accent work to one hue

---

## Typography System

### Typeface Pairs

**Display Face:** A warm, geometric sans-serif with character
- Examples: Inter (Bold/ExtraBold), Poppins (Bold/SemiBold), or Grotesk-style face
- Used for: H1, H2, major headings, brand-forward moments
- Characteristics: Wide counters, warm proportions, confident without being cold

**Body Face:** Highly legible, warm-toned sans-serif
- Examples: Inter, Segoe UI, or system stack (-apple-system, BlinkMacSystemFont)
- Used for: Paragraph text, body copy, longer-form content
- Characteristics: High x-height, generous spacing, reads well at small sizes

**Utility Face:** Monospace or tight sans for data/prices
- Examples: Courier New, Menlo, Monaco, or `font-family: monospace`
- Used for: Pricing, specifications, data tables, code
- Characteristics: Fixed-width, clear differentiation between similar characters

### Type Scale

Use a consistent scale throughout. Base = 16px (mobile) / 16px (desktop).

| Level | Mobile | Desktop | Line Height | Weight | Use |
|-------|--------|---------|-------------|--------|-----|
| **H1** | 32px | 40px | 1.2 | Bold (700) | Page titles, major headings |
| **H2** | 24px | 32px | 1.3 | Bold (700) | Section headings, service titles |
| **H3** | 20px | 24px | 1.4 | SemiBold (600) | Subsection headings, card titles |
| **H4** | 18px | 20px | 1.4 | SemiBold (600) | Small headings, block titles |
| **Body** | 14px | 16px | 1.6 | Regular (400) | Running text, paragraphs |
| **Small** | 12px | 14px | 1.5 | Regular (400) | Captions, metadata, helper text |
| **Label** | 12px | 12px | 1.5 | SemiBold (600) | Form labels, tag labels |

### Typography Rules

- **Headings:** Use `text-wrap: balance` so line breaks feel intentional
- **Body text:** Max line length ~65 characters for readability
- **Line height:** 1.6+ for body text (readable spacing)
- **Letter spacing:** Add subtle `letter-spacing` to uppercase labels (0.05em)
- **Font pairing:** Never use the same typeface for both display and body
- **Hierarchy:** Use weight and size for hierarchy, not color alone

### Text Colors

- **Headings:** Dark Charcoal (#1F2937) or Forest Green (#2D5016)
- **Body text:** Steel Gray (#6B7280)
- **Secondary text:** Light Gray (#9CA3AF) or Steel Gray
- **Links:** Forest Green (#2D5016) with underline; hover to Louisiana State Green (#004D40)
- **Disabled text:** Light Gray (#D1D5DB) on Warm Off-White background

---

## Layout & Spacing System

### Spacing Scale

Use multiples of 8px for consistency:

| Token | Value | Use |
|-------|-------|-----|
| **xs** | 4px | Tight spacing (rarely used) |
| **sm** | 8px | Small gaps between elements |
| **md** | 16px | Standard spacing between components |
| **lg** | 24px | Section padding, vertical rhythm |
| **xl** | 32px | Large gaps, section margins |
| **2xl** | 48px | Major section separation |
| **3xl** | 64px | Between major content sections |

### Grid & Layout

- **Container width:** 1200px max (desktop), 100% with padding (mobile)
- **Mobile padding:** 16px on left and right
- **Desktop padding:** 32-48px on left and right
- **Column layout:** Use CSS Grid or Flexbox with `gap` property (no margin-based spacing)
- **Sections:** 64px (3xl) vertical spacing between major sections
- **Subsections:** 32px (xl) vertical spacing between related content blocks

### Responsive Breakpoints

| Device | Breakpoint | Layout |
|--------|-----------|--------|
| **Mobile** | < 640px | Single column, full-width |
| **Tablet** | 640px–1024px | 2-column or stacked, narrow containers |
| **Desktop** | > 1024px | 2-3 columns, 1200px max container |

---

## Component System

### Buttons

#### Primary Button (CTA)
```
Background: Forest Green (#2D5016)
Text: White (#FFFFFF)
Padding: 12px 24px (mobile) / 14px 32px (desktop)
Border radius: 4px
Font: Body face, Bold, 14px/16px
Cursor: pointer
Transition: 200ms ease

Hover: Background to Louisiana State Green (#004D40)
Focus: Add 2px outline in Forest Green, 4px offset
Active: Darker shade or slight scale reduction
Disabled: Background to Light Gray (#D1D5DB), text to Gray
```

#### Secondary Button
```
Background: Transparent or Warm Off-White (#FAF9F7)
Border: 2px solid Forest Green (#2D5016)
Text: Forest Green (#2D5016)
Padding: 12px 24px (mobile) / 14px 32px (desktop)
Border radius: 4px
Font: Body face, Bold, 14px/16px

Hover: Background to Warm Off-White, border to Louisiana State Green
Focus: Outline as primary button
```

#### Tertiary / Text Button
```
Background: Transparent
Text: Forest Green (#2D5016)
Padding: 8px 0
Font: Body face, Regular, 14px/16px
Border-bottom: 1px solid Forest Green

Hover: Text to Louisiana State Green, border to Louisiana State Green
Focus: Add subtle background highlight
```

### Form Fields

#### Text Input / Textarea
```
Background: White (#FFFFFF)
Border: 1px solid Light Gray (#F3F4F6)
Padding: 10px 12px
Border radius: 4px
Font: Body face, Regular, 14px/16px
Text color: Steel Gray (#6B7280)

Focus: 
  - Border color to Forest Green (#2D5016)
  - Box shadow: 0 0 0 3px rgba(45, 80, 22, 0.1)

Placeholder: Light Gray (#9CA3AF), italic
Disabled: Background to Light Gray (#F3F4F6), text to disabled gray
Error: Border to Error Red (#EF4444)
```

#### Labels
```
Font: Body face, SemiBold, 12px/14px
Color: Dark Charcoal (#1F2937)
Letter spacing: 0.05em
Margin bottom: 8px
```

#### Required Field Indicator
```
Color: Error Red (#EF4444)
Display: Optional red asterisk after label text
Font: SemiBold
```

### Cards

#### Standard Card
```
Background: White (#FFFFFF)
Border: 1px solid Light Gray (#F3F4F6)
Border radius: 4px
Padding: 24px
Box shadow: 0 1px 3px rgba(0,0,0,0.05)
Spacing gap: 16px between cards (use CSS grid gap)

Accent variant:
  - Add 4px left border in Forest Green (#2D5016)
  - Adjust padding-left to 20px (compensate for border)
```

#### Service Card (with icon/image)
```
Structure:
  - Hero image or icon (120×120px minimum)
  - Service title (H3)
  - 2–3 bullet points or brief description
  - "Learn more" link or CTA button

Spacing:
  - 16px between image and title
  - 8px between title and description
  - 16px before CTA
```

### Navigation

#### Primary Navigation
```
Background: White (#FFFFFF) or Forest Green (#2D5016)
Text (white background): Forest Green (#2D5016)
Text (dark background): White (#FFFFFF)
Font: Display face, SemiBold, 14px/16px
Padding: 16px (vertical)
Gap: 32px between nav items

Active state: Underline or background highlight in Louisiana State Green
Hover: Text to Louisiana State Green, or opacity change
Mobile: Stack vertically, larger touch targets (44px minimum)
```

#### Footer Navigation
```
Background: Dark Charcoal (#1F2937)
Text: Light Gray (#F3F4F6)
Font: Body face, Regular, 14px
Links: Light Gray, hover to Warm Off-White (#FAF9F7)
Spacing: 24px between footer sections
```

### CTA Section / Hero

#### Hero Banner
```
Background: Forest Green (#2D5016) or high-quality hero image
Text: White (#FFFFFF) or Dark Charcoal (#1F2937)
Layout: Centered or left-aligned text, generous padding (64px top/bottom)
Image: Real photography (container in use, truck, Baton Rouge landmark)
CTA: Primary button, positioned clearly
Spacing: 24px between headline and subheading, 16px before CTA button
```

#### In-Page CTA Section
```
Background: Warm Off-White (#FAF9F7)
Border top: 1px solid Light Gray (#F3F4F6)
Padding: 48px (xl) horizontal and vertical
Text alignment: Center or left-aligned
Heading: H2, Forest Green (#2D5016)
Description: Body text, Steel Gray (#6B7280)
CTA: Primary or secondary button
```

### Testimonials / Reviews

#### Testimonial Card
```
Background: White (#FFFFFF)
Border: 1px solid Light Gray (#F3F4F6)
Border-left: 4px solid Louisiana State Green (#004D40)
Padding: 24px
Layout: 
  - Quote (italic, Steel Gray)
  - Author name (Bold, Dark Charcoal)
  - Author title/role (Small, Light Gray)
  - Star rating (optional, using semantic amber color)
  
Spacing: 12px between quote and author
Image: Optional customer photo (40×40px, rounded)
```

### Status & Feedback

#### Success Message
```
Background: rgba(16, 185, 129, 0.1) [light green]
Border-left: 4px solid Success Green (#10B981)
Text: Dark Charcoal (#1F2937)
Icon: Checkmark in Success Green
Padding: 16px
Border radius: 4px
Font: Body face, Regular, 14px
```

#### Warning Message
```
Background: rgba(245, 158, 11, 0.1) [light amber]
Border-left: 4px solid Warning Amber (#F59E0B)
Text: Dark Charcoal (#1F2937)
Icon: Alert triangle in Warning Amber
Padding: 16px
Border radius: 4px
```

#### Error Message
```
Background: rgba(239, 68, 68, 0.1) [light red]
Border-left: 4px solid Error Red (#EF4444)
Text: Dark Charcoal (#1F2937)
Icon: Exclamation or X in Error Red
Padding: 16px
Border radius: 4px
Tone: Specific ("Phone number must include area code"), not vague
```

---

## Imagery & Photography

### Guidelines

**What to use:**
- ✅ Real product photography (containers in customer scenarios)
- ✅ Actual delivery vehicles and equipment
- ✅ Local Baton Rouge landmarks and scenery
- ✅ Customer lifestyle photos (people, projects, real use cases)
- ✅ AI-generated images from client's own photos (via Gemini/Claude)
- ✅ Professional infographics with brand color accents

**Never use:**
- ❌ Clip art or hand-drawn SVGs of real objects (containers, trucks)
- ❌ Overly stylized cartoon imagery
- ❌ Generic stock photos that don't feel authentic to Baton Rouge
- ❌ Unbranded storage imagery

### Image Sizes & Formats

| Context | Size | Format | Notes |
|---------|------|--------|-------|
| **Hero banner** | 1200×600px (desktop) / 600×400px (mobile) | JPEG / WebP | Optimize for web; target <150KB |
| **Card image** | 400×300px | JPEG / WebP | Use aspect ratio 4:3 |
| **Thumbnail** | 150×150px | JPEG / WebP / PNG | Square, optimized |
| **Icon/Logo** | 40×40px–120×120px | SVG / PNG | Use SVG when possible |
| **Full-width section** | 1920×600px | JPEG / WebP | Optimize heavily <250KB |

### Image Treatment

- **Borders:** Subtle shadow (0 4px 12px rgba(0,0,0,0.08)) or none
- **Corners:** 4px border-radius for cards; no radius for hero images
- **Overlay:** Optional semi-transparent dark overlay on photos with text (rgba(0,0,0,0.3)–0.5)
- **Aspect ratios:** Consistent within sections (don't mix 16:9 and 4:3 in same gallery)

---

## Accessibility & Dark Mode

### Color Contrast

Ensure WCAG AA compliance (4.5:1 for text, 3:1 for graphics):

- **Forest Green (#2D5016) on Warm Off-White (#FAF9F7):** ✅ 8.2:1
- **Steel Gray (#6B7280) on Warm Off-White (#FAF9F7):** ✅ 4.8:1
- **Light Gray text on white:** ⚠️ Use only for secondary/decorative (< 3:1)
- **White text on Forest Green:** ✅ 10.5:1

### Focus States

- All interactive elements must have visible focus states
- Use outline, border change, or background highlight
- Avoid `outline: none` without providing alternative focus indicator
- Focus ring: 2px solid in Forest Green, 4px offset

### Motion & Animation

Respect `prefers-reduced-motion: reduce` for users who need it:
```css
@media (prefers-reduced-motion: reduce) {
  * { animation-duration: 0.01ms !important; }
}
```

### Dark Mode Implementation

When switching to dark mode (`prefers-color-scheme: dark` or `data-theme="dark"`):
- Backgrounds invert (Off-White → Deep Charcoal)
- Text inverts (Dark Charcoal → Light Gray)
- Accent lightens (Forest Green → Light Green)
- Borders adjust for visibility
- Contrast maintained at AA compliance

---

## Logo & Branding

### Logo Usage

**Primary logo:** Horizontal green logo on light backgrounds  
**Alternate:** White logo on dark backgrounds (Forest Green backgrounds)  
**Minimum size:** 120px wide for web  
**Clearspace:** Minimum 20px margin on all sides  

**Never:**
- Stretch or distort the logo
- Use outdated versions
- Change colors or remove elements
- Use as background pattern

### Favicon & App Icons

- **Favicon:** 32×32px, square green logo variant
- **Apple touch icon:** 180×180px, square green logo on white background
- **Android:** 192×192px and 512×512px square variants

---

## Component Specifications

### Sizing

**Heights (touch targets, minimum 44px on mobile):**
- Button: 40px (mobile) / 44px (desktop)
- Input field: 40px
- Navigation item: 44px (mobile touch), 32px (desktop)

**Widths:**
- Container: 1200px max
- Card: Full width on mobile, constrained on desktop
- Form field: 100% of container, max 500px on wide screens

### Shadows

**Subtle (cards, dropdowns):**
```
box-shadow: 0 1px 3px rgba(0, 0, 0, 0.08), 0 1px 2px rgba(0, 0, 0, 0.04)
```

**Medium (elevated sections, modals):**
```
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12), 0 2px 4px rgba(0, 0, 0, 0.08)
```

**Large (overlays, floating elements):**
```
box-shadow: 0 20px 25px rgba(0, 0, 0, 0.15), 0 10px 10px rgba(0, 0, 0, 0.05)
```

### Borders

- **Default:** 1px solid Light Gray (#F3F4F6)
- **Accent:** 2–4px solid Forest Green (#2D5016) for highlighted elements
- **Disabled:** 1px solid Light Gray (#D1D5DB)
- **Radius:** 4px for components; 0px for hero images

---

## Dark Mode Palette Reference

### CSS Custom Properties

```css
:root {
  --color-forest-green: #2D5016;
  --color-state-green: #004D40;
  --color-off-white: #FAF9F7;
  --color-steel-gray: #6B7280;
  --color-light-gray: #F3F4F6;
  --color-dark-charcoal: #1F2937;
  --color-success: #10B981;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #3B82F6;

  /* Light mode backgrounds */
  --bg-primary: var(--color-off-white);
  --bg-secondary: #FFFFFF;
  --text-primary: var(--color-dark-charcoal);
  --text-secondary: var(--color-steel-gray);
  --border-color: var(--color-light-gray);
  --accent-color: var(--color-forest-green);
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #111827;
    --bg-secondary: #1F2937;
    --text-primary: #F3F4F6;
    --text-secondary: #9CA3AF;
    --border-color: #374151;
    --accent-color: #86EFAC;
  }
}

/* Allow user theme toggle to override */
:root[data-theme="dark"] {
  --bg-primary: #111827;
  --bg-secondary: #1F2937;
  --text-primary: #F3F4F6;
  --text-secondary: #9CA3AF;
  --border-color: #374151;
  --accent-color: #86EFAC;
}

:root[data-theme="light"] {
  --bg-primary: var(--color-off-white);
  --bg-secondary: #FFFFFF;
  --text-primary: var(--color-dark-charcoal);
  --text-secondary: var(--color-steel-gray);
  --border-color: var(--color-light-gray);
  --accent-color: var(--color-forest-green);
}
```

---

## Implementation Checklist

- [ ] Color tokens defined in CSS custom properties
- [ ] Typography scale applied consistently
- [ ] Spacing scale documented and used
- [ ] Buttons styled (primary, secondary, tertiary)
- [ ] Form fields styled (input, select, textarea, labels)
- [ ] Cards and layout components ready
- [ ] Dark mode implemented and tested
- [ ] Accessibility audit completed (WCAG AA)
- [ ] Focus states implemented on all interactive elements
- [ ] Responsive breakpoints tested on mobile/tablet/desktop
- [ ] Image optimization and lazy-loading configured
- [ ] Favicon and app icons prepared
- [ ] Component library or pattern library published

---

## Usage Guidelines

### For Designers

1. Reference this document before creating mockups
2. Use the exact colors, typography, and spacing defined here
3. When creating new components, follow the same principles
4. Test all designs in both light and dark modes
5. Check contrast ratios for accessibility

### For Developers

1. Implement CSS custom properties from the palette section
2. Use the spacing scale (multiples of 8px) throughout
3. Build components matching the specifications
4. Test responsive behavior at all breakpoints
5. Ensure keyboard navigation works on all interactive elements
6. Validate HTML and CSS for standards compliance

### For Content Creators

1. Write headlines using the benefit-focused style from brand-style-guide.md
2. Keep body text at 14–16px minimum
3. Use active voice and second person ("You," "Your")
4. Provide alt text for all images
5. Use the CTA copy guidelines from the brand guide

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Jul 22, 2026 | Initial design system for site refresh |

---

## Questions or Feedback?

This design system is a living document. As the site refresh progresses, we'll refine and add to it. If a component or pattern isn't covered here, reference the principles:

- **Clarity over cleverness**
- **Warmth over minimalism**
- **Real over stylized**
- **Functional first**

---

**Design System Created:** July 22, 2026  
**For:** Load and Geaux Portable Storage Site Refresh  
**Maintained By:** Design Team / Clint Sanchez
