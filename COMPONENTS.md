# Component Specifications — Verdant Chrome

Design system components for the Chrome × Organic × Liquid Glass brand language.

---

## Buttons

### Primary (Organic)
| Property | Value |
|----------|-------|
| Background | `#4ADE80` |
| Text | `#0D1410` |
| Font | DM Sans, 600, 15px |
| Height | 44px (md) |
| Padding | 0 24px |
| Radius | `--radius-full` |
| Shadow | `0 0 32px rgba(74,222,128,0.3)` |
| Hover | Scale 1.02, shadow intensifies |
| Active | Scale 0.98 |
| Transition | 300ms `--ease-liquid` |

### Secondary (Glass)
| Property | Value |
|----------|-------|
| Background | `rgba(212,232,212,0.08)` |
| Border | 1px `rgba(255,255,255,0.14)` |
| Text | `#F0F4F0` |
| Backdrop blur | 32px |
| Hover bg | `rgba(212,232,212,0.12)` |
| Inset highlight | `inset 0 1px 0 rgba(255,255,255,0.24)` |

### Chrome (Accent CTA)
| Property | Value |
|----------|-------|
| Background | `linear-gradient(135deg, #9CA89C, #D4DCD4, #EEF2EE)` |
| Text | `#0D1410` |
| Border | Chrome gradient pseudo-element |
| Hover | Shimmer sweep animation (500ms) |
| Use sparingly | Max 1 per viewport section |

### Ghost
| Property | Value |
|----------|-------|
| Background | transparent |
| Text | `rgba(240,244,240,0.72)` |
| Hover | Glass fill at 8% opacity |

---

## Cards

### Glass Card (Default)
```
┌─────────────────────────────────┐  ← 1px glass border + chrome top highlight
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │  ← backdrop-blur: 32px
│  ░  Title (Syne 600)          ░  │
│  ░  Body text (DM Sans 400)   ░  │
│  ░  ─────────────────────     ░  │
│  ░  [Action]                  ░  │
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │
└─────────────────────────────────┘
```

| Property | Value |
|----------|-------|
| Background | `--color-glass-fill` |
| Blur | `--blur-glass-md` (32px) |
| Border | 1px `--color-glass-border` |
| Radius | `--radius-lg` (20px) |
| Padding | `--space-6` (24px) |
| Shadow | specular inset + depth shadow |
| Hover | Border brightens, bg +4% opacity |

### Feature Card (Elevated)
Same as glass card with:
- Blur: 48px
- Shadow: `--glass-depth-lg`
- Optional organic blob behind (z-index -1, 40% opacity)

---

## Navigation

| Property | Value |
|----------|-------|
| Height | 72px |
| Background | `rgba(13,20,16,0.72)` + blur 32px |
| Border bottom | 1px `rgba(255,255,255,0.08)` |
| Logo | Chrome gradient or organic mark |
| Links | 15px, weight 500, secondary text color |
| Link hover | Primary text + subtle organic underline glow |
| CTA slot | Primary button, right-aligned |

Sticky behavior: gains stronger blur and border on scroll.

---

## Input Fields

| Property | Value |
|----------|-------|
| Height | 48px |
| Background | `rgba(212,232,212,0.06)` |
| Border | 1px `rgba(255,255,255,0.12)` |
| Radius | `--radius-md` (12px) |
| Text | `#F0F4F0`, 16px |
| Placeholder | tertiary text color |
| Focus border | `#4ADE80` at 60% opacity |
| Focus glow | `0 0 0 3px rgba(74,222,128,0.15)` |
| Label | 13px, weight 500, secondary color, 8px gap |

---

## Typography Hierarchy

| Level | Font | Size | Weight | Line Height | Use |
|-------|------|------|--------|-------------|-----|
| Display | Syne | 61px (5xl) | 700 | 1.15 | Hero headlines |
| H1 | Syne | 49px (4xl) | 600 | 1.15 | Page titles |
| H2 | Syne | 39px (3xl) | 600 | 1.15 | Section headers |
| H3 | Syne | 31px (2xl) | 600 | 1.35 | Subsections |
| H4 | DM Sans | 25px (xl) | 600 | 1.35 | Card titles |
| Body | DM Sans | 16px (base) | 400 | 1.5 | Paragraphs |
| Small | DM Sans | 13px (sm) | 400 | 1.5 | Captions, meta |
| Label | DM Sans | 11px (xs) | 500 | 1.5 | Tags, badges |
| Mono | JetBrains | 14px | 400 | 1.5 | Code, data |

Chrome gradient text: apply to one keyword per headline maximum.

---

## Badges & Tags

| Variant | Background | Text | Border |
|---------|------------|------|--------|
| Organic | `rgba(74,222,128,0.15)` | `#4ADE80` | none |
| Chrome | chrome gradient | `#0D1410` | none |
| Glass | glass fill | secondary | glass border |
| Amber | `rgba(251,191,36,0.15)` | `#FBBF24` | none |

Height: 28px · Padding: 0 12px · Radius: full · Font: 11px, weight 600, tracking 0.04em

---

## Dividers

### Refraction Divider (Signature)
- Height: 1px
- Background: linear gradient with organic accent at center
- `transparent → rgba(74,222,128,0.3) → transparent`
- Optional: wavy SVG overlay at 20% opacity

### Glass Divider
- 1px `--color-glass-border`
- Margin: `--space-8` vertical

---

## Modal / Dialog

| Property | Value |
|----------|-------|
| Overlay | `rgba(13,20,16,0.8)` + blur 8px |
| Panel | Glass card elevated |
| Max width | 560px |
| Radius | `--radius-xl` |
| Enter animation | Scale 0.95→1, opacity 0→1, 300ms liquid ease |
| Exit | Reverse, 200ms smooth |

---

## Icon Style (Dew-Drop)

- Stroke width: 1.5px
- Color: secondary text or organic primary
- Specular dot: 2px circle, top-left at 25%/25%, white at 60% opacity
- Chrome icons: gradient fill instead of flat color
- Size scale: 16 / 20 / 24 / 32px

---

## Organic Blob (Background Element)

| Property | Value |
|----------|-------|
| Shape | SVG blob or CSS border-radius blob |
| Fill | `--gradient-organic-blob` |
| Size | 400–800px |
| Position | Partially off-canvas |
| Animation | Slow drift, 8s ease, infinite alternate |
| Blur | Optional 60px for depth |
| Opacity | 0.4–0.6 |
| Count | Max 2 per section |

---

## Motion Specs

| Interaction | Duration | Easing | Transform |
|-------------|----------|--------|-----------|
| Button hover | 300ms | liquid | scale(1.02) |
| Button press | 100ms | smooth | scale(0.98) |
| Card hover | 300ms | smooth | translateY(-2px) |
| Page enter | 500ms | liquid | opacity + translateY(16px) |
| Chrome shimmer | 500ms | smooth | bg-position sweep |
| Blob drift | 8000ms | drift | translate + morph |
| Modal open | 300ms | liquid | scale + opacity |
| Focus ring | 200ms | smooth | box-shadow expand |

---

## Spacing System

Section vertical padding: `--space-24` (96px) desktop, `--space-16` (64px) mobile.

Component gaps:
- Tight (inline elements): `--space-2` (8px)
- Default (stack): `--space-4` (16px)
- Comfortable (sections): `--space-8` (32px)
- Generous (hero): `--space-16` (64px)

Grid: 12 columns, `--space-6` gap, max-width `--container-xl`.

---

## Accessibility

- Minimum contrast: 4.5:1 for body text on glass surfaces
- Focus indicators: organic green ring, never removed
- Glass panels: ensure 8%+ fill opacity for readability
- Motion: respect `prefers-reduced-motion` — disable blob drift and shimmer
- Touch targets: minimum 44×44px
