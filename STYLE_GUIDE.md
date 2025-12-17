# Dreamink Presentation Style Guide

This document defines the official Dreamink color palette and styling guidelines for presentation slides.

## Color Palette

### Brand Colors

#### Primary Color

**Color:** `#1B3C53` (Dark Teal/Navy)

**Usage:** Slide titles, headers, main branding elements, emphasis text, key points

**CSS Variable:** `--dreamink-primary`

The primary color represents trust, professionalism, and calm - core values of Dreamink.

#### Secondary Colors

**Secondary Dark:** `#234C6A`

**Usage:** Subtitles, secondary emphasis, accents, code blocks

**CSS Variable:** `--dreamink-secondary-dark`

**Secondary (Default):** `#456882`

**Usage:** Borders, dividers, backgrounds for content cards, quote blocks

**CSS Variable:** `--dreamink-secondary`

**Secondary Light:** `#D2C1B6` (Warm Beige)

**Usage:** Subtle backgrounds, slide backgrounds, accent highlights, callout boxes

**CSS Variable:** `--dreamink-secondary-light`

---

### Primary Color Shades

For advanced usage, the primary color includes a full shade range:

- `primary-50`: `#E8EEF2` (Lightest - slide backgrounds)
- `primary-100`: `#D1DDE5`
- `primary-200`: `#A3BBCB`
- `primary-300`: `#7599B1`
- `primary-400`: `#477797`
- `primary-500`: `#1B3C53` (Base/DEFAULT)
- `primary-600`: `#163042`
- `primary-700`: `#102432`
- `primary-800`: `#0B1821`
- `primary-900`: `#050C11` (Darkest)

---

### Utility Colors

For functional UI elements and code syntax highlighting:

- **Success:** `green-600`, `green-700` - for checkmarks, success states, positive metrics
- **Error/Danger:** `red-600`, `red-700` - for warnings, error states, critical information
- **Warning:** `yellow-500`, `yellow-600` - for cautions, notes, important callouts
- **Info:** `blue-500`, `blue-600` - for informational blocks, tips, links
- **Neutral/Gray:** `gray-50` through `gray-900` - for general text and backgrounds

---

## Presentation Guidelines

### Slide Titles

**Color:** Primary (`#1B3C53`)

**Font Size:** 2.5em - 3em

**Font Weight:** Bold (700)

```css
h1 {
  color: #1B3C53;
  font-size: 2.5em;
  font-weight: 700;
}
```

### Slide Subtitles

**Color:** Secondary Dark (`#234C6A`)

**Font Size:** 1.5em - 2em

**Font Weight:** Semi-bold (600)

```css
h2 {
  color: #234C6A;
  font-size: 1.5em;
  font-weight: 600;
}
```

### Body Text

**Primary Text:** `gray-900` (default)

**Secondary Text:** `gray-600` (for descriptions, captions)

**Muted Text:** `gray-500` (for footnotes, metadata)

**Font Size:** 1em - 1.2em

**Line Height:** 1.6 - 1.8

### Backgrounds

**Main Slide Background:** `white` or `gray-50`

**Content Card Background:** `white` with `border: 2px solid #D2C1B6`

**Alternate Background:** `#E8EEF2` (primary-50) for variety

**Emphasis Background:** `#D2C1B6` (secondary-light) for callouts

### Code Blocks

**Background:** `#234C6A` (secondary-dark)

**Text Color:** `white` or `primary-50`

**Border:** `2px solid #1B3C53`

```css
pre {
  background: #234C6A;
  color: #E8EEF2;
  border: 2px solid #1B3C53;
  border-radius: 8px;
  padding: 1em;
}
```

### Lists and Bullets

**Bullet Color:** Primary (`#1B3C53`)

**Text Color:** `gray-900`

**Indentation:** 1.5em

### Links and Emphasis

**Link Color:** Primary (`#1B3C53`)

**Link Hover:** Secondary Dark (`#234C6A`)

**Bold Text:** Primary (`#1B3C53`) or default with `font-weight: 700`

**Italic Text:** Secondary Dark (`#234C6A`)

### Borders and Dividers

**Default Border:** `gray-300` (`#D1D5DB`)

**Accent Border:** Secondary (`#456882`)

**Focus Border:** Primary (`#1B3C53`)

**Divider:** `2px solid #D2C1B6`

---

## Slidev-Specific Guidelines

### Layout Styles

#### Title Slide (Portada)

```yaml
---
layout: cover
background: linear-gradient(135deg, #1B3C53 0%, #234C6A 100%)
---
```

**Title Color:** `white`

**Subtitle Color:** `#D2C1B6`

#### Section Divider

```yaml
---
layout: section
background: #E8EEF2
---
```

**Heading Color:** `#1B3C53`

#### Content Slide

```yaml
---
layout: default
---
```

**Background:** `white`

**Accent Color:** `#1B3C53`

### Custom CSS Classes

Create these utility classes in your `style.css`:

```css
/* Background colors */
.bg-primary { background-color: #1B3C53; }
.bg-secondary { background-color: #456882; }
.bg-secondary-light { background-color: #D2C1B6; }
.bg-primary-50 { background-color: #E8EEF2; }

/* Text colors */
.text-primary { color: #1B3C53; }
.text-secondary-dark { color: #234C6A; }
.text-secondary { color: #456882; }

/* Borders */
.border-primary { border-color: #1B3C53; }
.border-secondary { border-color: #456882; }
.border-accent { border-color: #D2C1B6; }

/* Gradients */
.gradient-header {
  background: linear-gradient(135deg, #1B3C53 0%, #234C6A 100%);
}
```

---

## Accessibility

All color combinations meet WCAG 2.1 AA standards for contrast:

- Primary (`#1B3C53`) on white: ✓ AAA (11.2:1)
- Secondary Dark (`#234C6A`) on white: ✓ AAA (8.3:1)
- Secondary (`#456882`) on white: ✓ AA (4.8:1)
- White text on Primary: ✓ AAA (11.2:1)

---

## Quick Reference

### Color Variables for CSS

```css
:root {
  /* Brand Colors */
  --dreamink-primary: #1B3C53;
  --dreamink-secondary-dark: #234C6A;
  --dreamink-secondary: #456882;
  --dreamink-secondary-light: #D2C1B6;

  /* Primary Shades */
  --dreamink-primary-50: #E8EEF2;
  --dreamink-primary-100: #D1DDE5;
  --dreamink-primary-200: #A3BBCB;
  --dreamink-primary-300: #7599B1;
  --dreamink-primary-400: #477797;
  --dreamink-primary-500: #1B3C53;
  --dreamink-primary-600: #163042;
  --dreamink-primary-700: #102432;
  --dreamink-primary-800: #0B1821;
  --dreamink-primary-900: #050C11;
}
```

### Hex Values Quick Copy

```
Primary:          #1B3C53
Secondary Dark:   #234C6A
Secondary:        #456882
Secondary Light:  #D2C1B6
Primary 50:       #E8EEF2
```

---

## Examples

### Slide with Emphasis Box

```markdown
---
layout: default
---

# Main Topic

<div class="bg-secondary-light border-accent p-4 rounded">
  <h3 class="text-primary">Key Point</h3>
  <p>Important information highlighted with brand colors</p>
</div>
```

### Quote Block

```markdown
<blockquote class="border-l-4 border-primary bg-primary-50 p-4">
  "Dreamink represents trust, professionalism, and calm."
</blockquote>
```

### Two-Column Layout

```markdown
<div class="grid grid-cols-2 gap-4">
  <div class="bg-white border-2 border-secondary p-4">
    <h3 class="text-primary">Column 1</h3>
    <p>Content here</p>
  </div>
  <div class="bg-primary-50 border-2 border-accent p-4">
    <h3 class="text-secondary-dark">Column 2</h3>
    <p>Content here</p>
  </div>
</div>
```

---

*This style guide is adapted for Slidev presentations from the Dreamink web application style guide.*
