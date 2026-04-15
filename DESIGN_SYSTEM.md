# Design System — Tokens & Usage Guide

This document defines the visual language for the product: colors, typography, shadows, and semantic mappings.

## Overview

The design system is built from design tokens that include primitives such as:
- `gold.default: #ffb700`
- `neutral.dark: #0a0a0a`

**Design Principles:**
- **Dark-Mode First**: Deep neutrals (#121212, #0a0a0a) as the base
- **Neon Accents**: Coral, gold, and teal provide high-contrast highlights
- **High Legibility**: White text with controlled opacity for readability
- **Consistent Meaning**: Semantic tokens ensure consistent interpretation

---

## 1. Color System

### 1.1 Primitive Colors

Primitive colors are the raw building blocks of the system.

| Palette | Default | Light | Dark |
|---------|---------|-------|------|
| **Gold** | `#ffb700` | `#ffc933` | `#cc9200` |
| **Coral** | `#ff5a00` | — | `#cc4800` |
| **Teal** | `#00f0ff` | — | `#00c0cc` |

**Neutral Scale:**
```
#ffffff → #faf6f0 → #b8b0a8 → #888888 → #2a2a2a → #121212 → #0a0a0a → #000000
```

### 1.2 Semantic Colors

Semantic colors map meaning to primitives so UI elements stay consistent.

#### Background

| Token | Value | Usage |
|-------|-------|-------|
| `--color-bg-page` | `#0a0a0a` | Main page background |
| `--color-bg-surface` | `#121212` | Card/container surfaces |
| `--color-bg-surface-elevated` | `#1a1a1a` | Elevated surfaces |
| `--color-bg-overlay` | `rgba(10, 10, 10, 0.85)` | Modal overlays |

#### Text

| Token | Value | Usage |
|-------|-------|-------|
| `--color-text-primary` | `#ffffff` | Headings, primary content |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.75)` | Body text, labels |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.5)` | Placeholder, disabled |
| `--color-text-muted` | `#888888` | Muted/caption text |
| `--color-text-inverse` | `#0a0a0a` | Text on light backgrounds |
| `--color-text-brand` | `#ffb700` | Brand highlights |

#### Borders

| Token | Value | Usage |
|-------|-------|-------|
| `--color-border-subtle` | `rgba(255, 255, 255, 0.08)` | Subtle dividers |
| `--color-border-default` | `rgba(255, 255, 255, 0.15)` | Standard borders |
| `--color-border-brand` | `rgba(255, 183, 0, 0.4)` | Brand-accented borders |
| `--color-border-focus` | `rgba(255, 90, 0, 0.6)` | Focus states |

#### Brand Palette

| Token | Value | Usage |
|-------|-------|-------|
| `--color-brand-primary` | `#ff5a00` (Coral) | Primary actions, CTAs |
| `--color-brand-secondary` | `#ffb700` (Gold) | Secondary actions, highlights |
| `--color-brand-tertiary` | `#00f0ff` (Teal) | Accents, success states |
| `--color-brand-gradient` | `linear-gradient(135deg, coral → gold)` | Gradient backgrounds |

#### Feedback

| Token | Value | Usage |
|-------|-------|-------|
| `--color-feedback-success` | `#00f0ff` (Teal) | Success messages |
| `--color-feedback-warning` | `#ffb700` (Gold) | Warning messages |
| `--color-feedback-error` | `#ff007f` | Error messages |
| `--color-feedback-info` | `#00f0ff` (Teal) | Info messages |

---

## 2. Typography

### Font Families

| Token | Value | Usage |
|-------|-------|-------|
| `--font-family-display` | `'Space Grotesk', 'Poppins', sans-serif` | Hero headings, large marketing text |
| `--font-family-body` | `'Poppins', sans-serif` | Paragraphs, UI labels |
| `--font-family-mono` | `'JetBrains Mono', monospace` | Code, technical UI, metrics |

### Font Sizes

| Token | Size | Usage |
|-------|------|-------|
| `--font-size-xs` | 0.75rem (12px) | Small captions |
| `--font-size-sm` | 0.875rem (14px) | Secondary text |
| `--font-size-base` | 1rem (16px) | Body text |
| `--font-size-lg` | 1.125rem (18px) | Large body |
| `--font-size-xl` | 1.25rem (20px) | Section titles |
| `--font-size-2xl` | 1.5rem (24px) | H3 headings |
| `--font-size-3xl` | 1.875rem (30px) | H2 headings |
| `--font-size-4xl` | 2.25rem (36px) | H1 headings |
| `--font-size-5xl` | 3rem (48px) | Display text |
| `--font-size-6xl` | 3.75rem (60px) | Hero headlines |

### Font Weights

| Token | Value |
|-------|-------|
| `--font-weight-normal` | 400 |
| `--font-weight-medium` | 500 |
| `--font-weight-semibold` | 600 |
| `--font-weight-bold` | 700 |

### Line Heights

| Token | Value |
|-------|-------|
| `--line-height-tight` | 1.25 |
| `--line-height-normal` | 1.5 |
| `--line-height-relaxed` | 1.75 |

---

## 3. Shadows & Glow

### Shadow Colors

| Token | Value |
|-------|-------|
| `--shadow-color-base` | `rgba(0, 0, 0, 0.6)` |
| `--glow-brand` | `rgba(255, 90, 0, 0.4)` |
| `--glow-secondary` | `rgba(0, 240, 255, 0.3)` |

### Shadow Definitions

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-sm` | `0 1px 2px` | Minimal elevation |
| `--shadow-md` | `0 4px 6px` | Cards, modals |
| `--shadow-lg` | `0 10px 15px` | Elevated surfaces |
| `--shadow-xl` | `0 20px 25px` | High elevation |
| `--shadow-2xl` | `0 25px 50px` | Maximum elevation |

### Glow Effects

| Token | Usage |
|-------|-------|
| `--glow-brand-*` | CTA buttons, active states |
| `--glow-secondary-*` | Accents, hover states, neon-tech effects |

---

## 4. Spacing

| Token | Size | Token | Size |
|-------|------|-------|------|
| `--space-0` | 0 | `--space-8` | 2rem (32px) |
| `--space-1` | 0.25rem (4px) | `--space-10` | 2.5rem (40px) |
| `--space-2` | 0.5rem (8px) | `--space-12` | 3rem (48px) |
| `--space-3` | 0.75rem (12px) | `--space-16` | 4rem (64px) |
| `--space-4` | 1rem (16px) | `--space-20` | 5rem (80px) |
| `--space-5` | 1.25rem (20px) | `--space-24` | 6rem (96px) |
| `--space-6` | 1.5rem (24px) | | |

---

## 5. Border Radius

| Token | Size | Token | Size |
|-------|------|-------|------|
| `--radius-none` | 0 | `--radius-xl` | 0.75rem (12px) |
| `--radius-sm` | 0.25rem (4px) | `--radius-2xl` | 1rem (16px) |
| `--radius-md` | 0.375rem (6px) | `--radius-full` | 9999px |
| `--radius-lg` | 0.5rem (8px) | | |

---

## 6. Transitions

| Token | Value |
|-------|-------|
| `--transition-duration-fast` | 150ms |
| `--transition-duration-normal` | 250ms |
| `--transition-duration-slow` | 350ms |
| `--transition-timing-ease` | `cubic-bezier(0.4, 0, 0.2, 1)` |

---

## 7. Z-Index Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--z-index-base` | 0 | Default |
| `--z-index-dropdown` | 100 | Dropdown menus |
| `--z-index-sticky` | 200 | Sticky headers |
| `--z-index-fixed` | 300 | Fixed elements |
| `--z-index-overlay` | 400 | Overlays |
| `--z-index-modal` | 500 | Modals |
| `--z-index-popover` | 600 | Popovers |
| `--z-index-tooltip` | 700 | Tooltips |
| `--z-index-toast` | 800 | Toast notifications |

---

## 8. Semantic Mapping Examples

### Button (Primary)

```css
background-color: var(--color-brand-primary); /* #ff5a00 */
color: var(--color-text-inverse); /* #0a0a0a */
border: 1px solid var(--color-border-brand);
```

**Hover:** lighten coral by 10%  
**Focus:** `var(--color-border-focus)`

### Card Surface

```css
background-color: var(--color-bg-surface-elevated); /* #1a1a1a */
border: 1px solid var(--color-border-subtle);
box-shadow: var(--shadow-md);
```

### Page Layout

```css
background-color: var(--color-bg-page); /* #0a0a0a */
color: var(--color-text-primary); /* #ffffff */
```

Section headers use `var(--color-text-secondary)`.

---

## 9. Pre-built Component Classes

The design tokens CSS file includes ready-to-use component classes:

| Class | Description |
|-------|-------------|
| `.btn-primary` | Primary button with brand colors and glow effects |
| `.card-surface` | Elevated card with subtle border and shadow |
| `.page-layout` | Full-page dark theme container |
| `.section-header` | Styled section heading with display font |
| `.code-block` | Monospace code block styling |
| `.status-success` | Success state color |
| `.status-warning` | Warning state color |
| `.status-error` | Error state color |
| `.status-info` | Info state color |
| `.focus-ring` | Accessible focus ring utility |
| `.gradient-text` | Brand gradient text effect |
| `.neon-accent` | Secondary glow accent |
| `.elevated-glow` | Elevated surface with brand glow |

---

## 10. Implementation

### CSS Variables

Import the design tokens in your project:

```html
<link rel="stylesheet" href="design-tokens.css">
```

Then use tokens throughout your stylesheets:

```css
.my-component {
  background-color: var(--color-bg-surface);
  color: var(--color-text-primary);
  border: 1px solid var(--color-border-default);
  box-shadow: var(--shadow-md);
}
```

### Best Practices

1. **Always use semantic tokens** instead of primitive colors directly
2. **Maintain contrast ratios** for accessibility (WCAG AA minimum)
3. **Use glow effects sparingly** for maximum impact
4. **Test in dark mode first** — this is a dark-mode-first system
5. **Leverage component classes** for consistency

---

## Quick Reference

```css
/* Colors */
var(--color-bg-page)          /* Page background */
var(--color-text-primary)     /* Primary text */
var(--color-brand-primary)    /* Coral CTA */
var(--color-feedback-error)   /* Error state */

/* Typography */
var(--font-family-display)    /* Headlines */
var(--font-family-body)       /* Body text */
var(--font-family-mono)       /* Code */

/* Effects */
var(--shadow-md)              /* Card shadow */
var(--glow-brand-md)          /* Brand glow */
var(--transition-fast)        /* Quick animation */
```
