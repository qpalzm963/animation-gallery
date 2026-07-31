# Motion Design Field Guide 動畫表現方式圖鑑

English ｜ [繁體中文](README.md)

[![GitHub stars](https://img.shields.io/github/stars/qpalzm963/animation-gallery?style=social)](https://github.com/qpalzm963/animation-gallery/stargazers)

A single-page interactive field guide covering **76 web animation techniques** — from the most
common fades and offsets to rarer ones like FLIP, View Transitions, scroll timelines, gooey
blobs, and glitch art. Every card is a **real, running** implementation: hover it, or press
Replay, to watch it again, with notes on when to use it and the core code you can copy straight
out.

**A single HTML file, zero dependencies, all native CSS / Web Animations API / Canvas / SVG.**
The code snippet shown on each card is the exact string injected into the page — what you see
is what’s actually running.

## Live demo

**https://qpalzm963.github.io/animation-gallery/**

Or open [`index.html`](index.html) directly — no build step or install needed:

```bash
open index.html
# or run a local server (some View Transitions demos need http:// rather than file://)
python3 -m http.server 8991
```

## Contents

12 categories, 76 techniques:

| Category | Includes |
|---|---|
| Basics | Fade, Fade Up, Scale Pop, Spin, Blur In, Flip In, Directional Wipe |
| Timing & Easing | Easing compare, Spring, Overshoot, Anticipation, Stagger, Squash & Stretch, Follow Through |
| Layout Transitions | FLIP, Shared Element, View Transitions API, List Reorder, Shape Morph, Auto Height |
| Scroll-driven | Scroll Reveal, Parallax, Scroll Progress, Sticky Scene, native `animation-timeline` |
| Text Animation | Typewriter, Text Scramble, Split Text, Mask Reveal, Number Counter, Marquee, Variable Font, Kinetic Typography |
| Drawing & Masks | Line Drawing, Path Follow, Clip Reveal, Checkmark Draw, Gradient Mask, Path Morph |
| Physics & Interaction | Magnetic Hover, Cursor Trail, Inertia, Rubber Band, Particles, Ripple |
| Space & 3D | Tilt Card, Card Flip, Cube, Layered Depth, Perspective List |
| Light & Material | Skeleton Shimmer, Gradient Flow, Glow Pulse, Film Grain, Glassmorphism, Gooey / Metaball |
| Experimental | Glitch, Chromatic Aberration, Sprite / Steps, Wave Grid, Curtain Transition, Pixel Dissolve, Elastic Indicator, Orbit |
| Modern CSS Transitions | `@starting-style`, `allow-discrete`, `calc-size()`, `linear()` pure-CSS spring, `@property`, multi-track keyframes |
| View Transitions | Custom old/new, `::view-transition-group()`, direction-aware transitions, name-collision teaching card, list-to-detail, cross-document transitions (`vt-a.html` / `vt-b.html`) |

Also included:

- **The 12 Principles → Interface Equivalents** — Disney’s 12 animation principles translated into interface vocabulary
- **Cross-Platform Reference** — a concept table for CSS/Web, Flutter, and SwiftUI, plus each platform’s exclusive techniques
  (SwiftUI’s `KeyframeAnimator`, `PhaseAnimator`, Liquid Glass; Flutter’s `Hero`, `Curves`)
- **Duration & Easing Cheat Sheet**

## Prompt generator

Every card can copy a structured prompt in one click — paste it into any AI coding agent and get
an idiomatic implementation of that technique in your target framework. Pick a framework from
the toolbar (Flutter / SwiftUI / React + Framer Motion / plain CSS); the prompt carries the
**visual spec**, not a request to translate the CSS line by line, plus a reminder of that
framework’s idioms.

## Features

- Category filtering, keyword search
- Replay a single card / replay all
- UI in five languages — Traditional Chinese / Simplified Chinese / English / Japanese / Korean, toggle in the top right, remembers your choice
- Deep links to every card — click a card’s number to copy its `#t-<id>` link and share a specific technique
- Dark / light theme toggle (defaults to light), remembers your choice
- `prefers-reduced-motion` detection — automatically pauses demo animations with a “show me anyway” option
- Off-screen auto-unmount, so a large number of demos never run at once and tank performance

## License

[MIT](LICENSE) — free to use, modify, and redistribute.

---

If you found this useful, a ⭐ Star in the top right helps more people find it.
