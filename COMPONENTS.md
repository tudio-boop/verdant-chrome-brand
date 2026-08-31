# Stonehaven — parts already on the site

Do not invent new component families. Use these.

## Navigation

Liquid glass pill from `stonehaven-psg` `LiquidGlassNavigation`.

- Position: fixed, centered, `min(980px, 100vw - 1.25rem)`
- Fill: `rgba(12, 13, 16, 0.42)`
- Blur: `22px`, saturate `1.2`
- Border: `1px solid rgba(255,255,255,0.14)`
- Rim: top highlight `rgba(255,255,255,0.42)`
- Inset: `inset 0 1px 0 rgba(255,255,255,0.28)`
- Mark: Syne, 0.92rem, tracking `0.18em`, `STONEHAVEN`
- Sub: IBM Plex Mono, 0.52rem, uppercase
- Links: mono, 0.58rem, tracking `0.12em`, uppercase
- Current: fill `rgba(255,255,255,0.12)` + 1px inner stroke
- Compact on scroll: fill darkens to `rgba(8,9,12,0.58)`, sub collapses

Website wireframe nav (B/W stack pages): 44px bar, 1px ink rule, boxed links, invert current.

## Kinetic sphere

`<stonehaven-avatar theme="threshold">` on the landing center pane.

Fallback chrome (when WebGL is off):

```
radial at 32% 26%  white 85% → transparent
radial at 68% 78%  #17181E 75% → transparent
radial at 50% 50%  #D8DAE2 → #A9ABB6 42% → #383A44 78% → #17181E
inset highlight + inset shade
```

Lane rings:

| Theme | Ring |
|-------|------|
| entertainment | `1px rgba(154,104,255,0.22)` + glow `rgba(122,60,255,0.18)` |
| promotions | `1px rgba(47,107,255,0.14)` |
| threshold | hairline `rgba(20,20,26,0.06)` |

Caption glass: `rgba(250,250,249,0.55)`, blur 16px saturate 1.4, radius 12px. Entertainment caption inverts to dark glass.

## Labeled box

From `css/wireframe.css`.

- 1px solid currentColor
- Corner index: 11px mono, uppercase, tracking `0.06em`, sits on the top-left rule
- Padding: `28px 16px 16px`
- Empty slots: dashed `#888` on `#F4F4F4`

Indexes: `landing · left/center/right`, `e1–e6`, `p1–p6`.

## Buttons / CTAs

Wireframe:

- Outline: 1px ink, pad `6px 12px`
- Solid: ink fill, paper type
- Hover: invert

Do not use pill greens, glows, or scale-bounce.

## Forms

- Label: 12px mono, uppercase, tracking `0.05em`
- Field: 1px ink, transparent fill, pad `6px 8px`, max-width 480px
- Submit: solid CTA
- Mail: `info@stonehavenentertainment.com` with subject `[Entertainment Contact]` or `[Promotions Contact]`

## Type

| Role | Face | Notes |
|------|------|-------|
| Display / hero | Syne 700 | tracking `-0.045em`, line-height `0.92` |
| Body | Sora 300–400 | line-height `1.55` |
| Index, nav, labels | IBM Plex Mono | uppercase, tracking `0.12em–0.22em` |

Hero size: `clamp(2.6rem, 9.2vw, 7.4rem)`.

## Motion

- Ease: `cubic-bezier(0.22, 1, 0.36, 1)`
- Duration: `520ms` (`1ms` if `prefers-reduced-motion`)
- Nav compact: same ease
- Kinetic word: 180deg white gradient clip, not a shimmer sweep
- Film grain: 3.5% fractal noise, `mix-blend-mode: soft-light`

## What not to add

Blobs, emoji principles, lime/teal “organic,” five invented palettes, DM Sans, glow CTAs, gradient-text logos, fake metrics.
