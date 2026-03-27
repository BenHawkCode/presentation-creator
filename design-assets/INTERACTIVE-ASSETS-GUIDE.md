# Interactive Assets — Usage Guide

## What These Are

These HTML asset libraries contain **ready-to-use visual elements** for The Coach Consultant brand. They are **reference examples, not the only assets available**. When creating carousels, presentations, or any visual output, Claude Code should:

1. **Use these libraries as design references** — study the patterns, styles, and element types
2. **Create new assets on the fly** that follow the same design system — don't just copy/paste from these sheets
3. **Match the visual quality and style** of these examples in all new outputs

The goal is consistency, not limitation. If a carousel needs an icon that doesn't exist in the library, create one using the same SVG style. If a presentation needs a new card layout, build one using the same glassmorphism patterns.

---

## Where They Live

The same assets exist in two locations:

| Location | Path |
|----------|------|
| Presentation Creator | `Presentation Creator/design-assets/` |
| Instagram Carousels | `the-coach-consultant/2-instagram/instagram-carousel/Interactive Assets/` |

---

## Asset Libraries

### 1. Icon & Emblem Library (`icon-emblem-library.html`)

**100+ custom SVG icons** across 12 categories:

| Category | Examples |
|----------|----------|
| AI & Technology | Bot, Intelligence, Speed, Automation, Workflow, Analytics |
| Sales & Revenue | Revenue, Conversion, Pipeline, Commission |
| Personal Brand & Content | Authority, Creator, Portfolio, Influence |
| Lead Generation & Funnels | Funnel, Opt-in, Capture, Conversion |
| Mindset & Development | Growth, Transformation, Belief, Shift |
| Business & Strategy | Strategy, Operations, Planning, Scaling |
| App & Software Icons | Popular app logos and software icons |
| AI Tool Icons | ChatGPT, Claude, Midjourney, etc. |
| Social Media Platforms | Instagram, LinkedIn, YouTube, TikTok, etc. |

**Plus reusable elements:**
- **Stamps**: Rotated badges (`-3deg`, 2px border, uppercase, Space Grotesk 900)
- **Number circles**: 30px filled circles with centred numbers
- **CTA buttons**: 20px radius pills, uppercase, 10px font
- **Watermarks**: Low-opacity brand positioning elements

**SVG design pattern**: Dual-colour stroke + fill, teal primary with accent secondary, 44x44px sizing, opacity layering for depth.

### 2. Overlay Asset Library (`overlay-asset-library.html`)

**30+ frosted glass overlay components** designed to layer over photos and video:

**Element types:**
- **Icon badges**: Circle (48px), Square (44px), Pill (inline-flex) — all with backdrop-filter blur
- **Glass panels**: Dark glass, teal-tinted glass, accent-tinted glass (`backdrop-filter: blur(16px)`)
- **Metrics**: Large bold numbers (Space Grotesk 900) with small labels
- **Progress bars**: 6px height, coloured fills, rounded
- **Comparison layouts**: Before/After, Myth vs Truth, Feature tables
- **Result cards**: Transformation metrics (£0 → £10k style)
- **AI stack lists**: Icon + text rows showing tool stacks
- **Stamps**: Rotated quality/authority badges

**Glassmorphism pattern**: `background: rgba(0,0,0,0.65)`, `backdrop-filter: blur(16px)`, semi-transparent borders, designed for transparency over backgrounds.

### 3. Social Media Asset Library (`social-media-asset-library.html`)

**138+ template assets** with platform-specific dimensions:

**Aspect ratios:**
- `1:1` — Instagram posts, carousels (1080x1080)
- `4:5` — Instagram portrait, Reels
- `9:16` — Stories, TikTok, Shorts
- `16:9` — YouTube thumbnails, landscape
- `1.91:1` — LinkedIn, Facebook cards

**Template element types:**

| Element | Class | Description |
|---------|-------|-------------|
| Backgrounds | `.tmpl-dark`, `.tmpl-grad1`, `.tmpl-grad-teal` | Solid, gradient, and split layouts |
| Headlines | `.tmpl-title` | Space Grotesk 900, large |
| Body text | `.tmpl-body` | Inter 400, grey, readable |
| Tags | `.tmpl-tag` | 8px uppercase, teal, spaced |
| Metrics | `.tmpl-metric` | Space Grotesk 900, big numbers |
| Gradient text | `.tmpl-gradient-text` | Teal → orange fill |
| Dividers | `.tmpl-divider` | 40px wide, 3px tall, teal |
| Corner accents | `.tmpl-corner-accent` | 40x40px bordered corners |
| Quote marks | `.tmpl-quote-mark` | 40px teal quotation mark |
| Watermarks | `.tmpl-watermark` | Brand mark, bottom-right |
| Icon boxes | `.tmpl-icon-box` | 36x36px, teal bg at 15% opacity |
| Number circles | `.tmpl-number-circle` | 28px, filled, for sequences |
| Cards | `.tmpl-card` | Glass cards with 4% white bg |
| Accent cards | `.tmpl-card-accent` | Left border 3px orange |
| Teal cards | `.tmpl-card-teal` | Left border 3px teal |
| CTA buttons | `.tmpl-cta-btn` | Solid teal, pill shape |
| Outline buttons | `.tmpl-outline-btn` | Border only, teal |
| Lower thirds | `.tmpl-lower-third` | Video name/title overlay |
| Carousel dots | `.tmpl-carousel-dots` | Navigation indicators |
| Brushstroke | `.brushstroke::after` | Teal background behind text, skewed |

---

## How to Create New Assets

When building carousels, presentations, or visual content, follow these rules:

### Icons
- Use **SVG** with stroke + fill dual-colour design
- Primary stroke: `#5B9A9A` (teal), secondary: `#FF6B35` (orange) or `#FFD166` (yellow)
- Size: 44x44px default, stroke-width: 2, stroke-linecap: round
- Opacity layering: use `opacity: 0.3` for background shapes

### Cards
```css
background: rgba(255, 255, 255, 0.04);
border: 1px solid rgba(255, 255, 255, 0.08);
border-radius: 16px;
padding: 30px;
```
- Add `border-left: 3px solid #5B9A9A` for teal accent cards
- Add `border-left: 3px solid #FF6B35` for orange accent cards

### Glass Overlays
```css
background: rgba(0, 0, 0, 0.65);
backdrop-filter: blur(16px);
border: 1px solid rgba(255, 255, 255, 0.08);
border-radius: 16px;
```

### Badges & Stamps
```css
border: 2px solid #5B9A9A;
padding: 4px 12px;
font-family: 'Space Grotesk';
font-weight: 900;
text-transform: uppercase;
letter-spacing: 2px;
transform: rotate(-3deg);
font-size: 9px;
```

### Number Circles
```css
width: 30px;
height: 30px;
border-radius: 50%;
background: #5B9A9A;
display: inline-flex;
align-items: center;
justify-content: center;
font-family: 'Space Grotesk';
font-weight: 900;
font-size: 13px;
color: white;
```

### CTA Buttons
```css
padding: 7px 18px;
border-radius: 20px;
font-family: 'Space Grotesk';
font-weight: 800;
font-size: 10px;
text-transform: uppercase;
letter-spacing: 1px;
background: #5B9A9A;
color: white;
```

### Progress Bars
```css
/* Container */
height: 6px;
background: rgba(255, 255, 255, 0.06);
border-radius: 3px;

/* Fill */
height: 100%;
border-radius: 3px;
background: linear-gradient(90deg, #5B9A9A, #7abfbf);
```

### Tags / Pills
```css
padding: 5px 12px;
border-radius: 16px;
font-size: 9px;
font-weight: 700;
background: rgba(91, 154, 154, 0.15);
color: #7abfbf;
```

### Decorative Elements
- **Background circles**: 500px, `opacity: 0.03`, `filter: blur(100px)`, teal
- **Corner accents**: 40x40px, `border: 1px solid rgba(255,255,255,0.3)`, positioned absolute
- **Line accents**: `linear-gradient(90deg, #5B9A9A, transparent)`, full width, 1px height
- **Brushstroke**: Pseudo-element behind text, teal bg, `skewX(-2deg)`, `height: 45%`

---

## Colour Reference (Full Palette)

| Colour | Hex | Variable | Usage |
|--------|-----|----------|-------|
| Primary Teal | `#5B9A9A` | `--teal` | Main brand, CTAs, highlights |
| Dark Teal | `#3d7a7a` | `--dark-teal` | Gradients, hover states |
| Light Teal | `#7abfbf` | `--light-teal` | Text highlights on dark |
| Accent Orange | `#FF6B35` | `--accent` | Energy, urgency, secondary |
| Accent Yellow | `#FFD166` | `--accent2` | Premium, stats, warnings |
| Primary Black | `#0a0a0a` | `--bg` | Main background |
| Secondary Black | `#141414` | `--bg2` | Panel backgrounds |
| Dark Grey | `#1a1a1a` | `--bg3` | Deep backgrounds |
| White | `#ffffff` | `--white` | Text, highlights |
| Body Grey | `#aaaaaa` | `--gray` | Secondary text |
| Light Grey | `#cccccc` | `--gray-light` | Subtle text |
| Red | `#ff4444` | `--red` | Negative, alerts |
| Green | `#44ff88` | `--green` | Positive, success |
| Purple | `#9B6DFF` | `--purple` | Premium, special |
| Blue | `#4D9FFF` | `--blue` | Info, links |

---

## Key Principle

**These libraries are starting points, not limitations.** Every new carousel, presentation, or visual output should feel like it belongs in these libraries — same colours, same typography, same glass effects, same element styles — but the specific assets should be created fresh to match the content being presented.

---

## Always Think Visually

When creating any slide or visual output, **always consider what visual representation would communicate the content most effectively**. Never default to plain text when a visual element would be stronger. Ask yourself: could this be shown as a...

### Data Visualisation Options
- **Donut/Pie chart**: `conic-gradient()` for percentage breakdowns (e.g. 70% operational time)
- **Horizontal bar chart**: CSS width percentages for comparing values side by side
- **Vertical bar chart**: CSS height percentages for trend/comparison data
- **Progress bars**: Linear fills showing completion or comparison (before vs after)
- **Radial progress circles**: Circular progress indicators for stats like 92% retention
- **Comparison scales**: Visual weight/size differences (e.g. £62,450 vs £31)

### Structural Visuals
- **Flow charts**: Boxes connected by lines/arrows showing processes (Content → AI)
- **Timelines**: Vertical/horizontal lines with dot markers and year labels
- **Infographic circles**: Large number inside a circle with label below
- **Before/After split**: Two-column visual with contrasting colours (red vs teal)
- **Comparison tables**: Structured grid with headers, rows, and accent borders

### Decorative Enhancements
- **SVG icons**: Custom icons matching the teal stroke + fill pattern (44x44px)
- **Arrow connectors**: SVG arrows between elements to show flow/transformation
- **Growth curves**: Simple upward-sloping SVG paths for revenue/growth visuals
- **Stamp badges**: Rotated authority marks ("PROVEN", "VERIFIED", "RESULTS")

### Logo Usage
- **Always use the watermark logo** (transparent background) from `Presentation Creator/5. Logo/LOGO/WATERMARK/Asset 1@216x.png`
- Apply `mix-blend-mode: screen` on dark backgrounds — this ensures no white box
- Position bottom-right at small size (80-120px width, opacity 0.6-0.8) as a watermark
- On image slides, the watermark should be subtle, not dominant

### Image Slides with Ben
- **NO gradient shadow overlays on image slides. None at all.**
- Text uses `text-shadow: 0 1px 8px rgba(0,0,0,0.6), 0 0 3px rgba(0,0,0,0.4)` for readability — no dark background needed
- Interactive elements (circular rings, tag pills, stat cards) float directly over the image
- If a glass card is needed, use `rgba(0,0,0,0.04)` with `backdrop-filter:blur(8px)` — nearly invisible
- **NEVER crop Ben's head.** Always use `object-fit: cover` with `object-position: center 20%` — this fills the square frame with head + upper body naturally. Never use `top` (empty space) or `center` (crops head)
- Use high-resolution source images — download actual files, not thumbnails
- Use professional images only (stage, presenting, mountain/adventure) — no fitness/gym shots
- All accent colours and gradient text must use brand teal `#5B9A9A` / `#7abfbf` — never use off-brand orange `#FF8C32` for highlights. Orange `#FF6B35` is only for accent slides, not for text highlighting on hook slides
