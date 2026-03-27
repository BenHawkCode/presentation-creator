# The Coach Consultant — Design System

Reference design extracted from the live presentation pages:
- https://benhawkcode.github.io/presentation-creator/
- https://benhawkcode.github.io/gus-strategy/

Use this system for ALL presentations, Instagram carousels, and visual outputs.

---

## Colour Palette

| Colour | Hex | Usage |
|--------|-----|-------|
| **Primary Teal** | `#5B9A9A` | Main accent, buttons, highlights, dividers |
| **Teal Dark** | `#3d7a7a` | Gradient endpoints, hover states |
| **Teal Light** | `#7abfbf` | Highlighted text on dark backgrounds |
| **Accent Orange** | `#FF6B35` | Secondary accent, alerts, emphasis |
| **Accent Yellow** | `#FFD166` | Tertiary accent, stats, highlights |
| **Black** | `#0a0a0a` | Primary dark background |
| **Dark Grey** | `#141414` | Secondary dark background |
| **White** | `#ffffff` | Primary text on dark backgrounds |
| **Grey Text** | `#aaaaaa` | Muted/secondary text |
| **Status Red** | `#ff4444` | Negative indicators |
| **Status Green** | `#44ff88` | Positive indicators |

### Background Gradients
- **Primary Dark**: `linear-gradient(135deg, #0a0a0a 0%, #1a2a2a 100%)`
- **Teal**: `linear-gradient(135deg, #5B9A9A 0%, #3d7a7a 100%)`
- **Orange Accent**: `linear-gradient(135deg, #FF6B35 0%, #ff8f65 100%)`
- **Dark Neutral**: `linear-gradient(135deg, #0a0a0a 0%, #1a1a0a 100%)`

---

## Typography

### Fonts
- **Headings**: Space Grotesk (Google Font)
  - H1: `clamp(36px, 5vw, 72px)`, weight 900, line-height 1.1
  - H2: `clamp(28px, 3.5vw, 52px)`, weight 800, line-height 1.2
  - H3: `clamp(20px, 2.5vw, 32px)`, weight 700
  - Big Numbers: `clamp(48px, 7vw, 140px)`, weight 900
- **Body**: Inter (Google Font)
  - Body: `clamp(15px, 1.5vw, 19px)`, weight 400, line-height 1.7
  - Large body: 24px, line-height 1.6
- **Labels/Tags**: Inter, 12-14px, weight 600, uppercase, letter-spacing 2-4px

### Google Fonts Import
```css
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700;800;900&display=swap');
```

---

## Card Design

```css
.card {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;
  padding: 30px;
  transition: all 0.4s ease;
}

.card:hover {
  transform: translateY(-4px);
  border-color: #5B9A9A;
  box-shadow: 0 8px 30px rgba(91, 154, 154, 0.15);
}
```

### Card Variants
- **Left-accent card**: Add `border-left: 4px solid #5B9A9A` (or orange/yellow/red/green)
- **Metric card**: Centred, big number top, label below
- **Icon card**: Icon left or top, title + description

---

## Tags / Pills

```css
.tag {
  padding: 6px 16px;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 600;
}

.tag-teal {
  background: rgba(91, 154, 154, 0.15);
  color: #7abfbf;
}

.tag-orange {
  background: rgba(255, 107, 53, 0.15);
  color: #FF6B35;
}
```

---

## Dividers

```css
.divider {
  width: 80px;
  height: 4px;
  background: #5B9A9A;
  border-radius: 2px;
  margin: 24px 0;
}
```

---

## Progress Bars

```css
.progress-bar {
  height: 8px;
  border-radius: 4px;
  background: linear-gradient(90deg, #5B9A9A, #7abfbf);
}
```

---

## Layout

### Slide/Section Dimensions
- Full viewport: `min-height: 100vh` (presentations)
- Instagram carousel: `1080px x 1080px` (fixed square)
- Container max-width: `1100px`
- Padding: `60px 80px` (desktop), `40px 24px` (mobile)

### Grid Systems
- **2-column**: `grid-template-columns: repeat(auto-fit, minmax(320px, 1fr))`, gap 24px
- **3-column**: `grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))`, gap 20px
- **Icon grid**: `repeat(auto-fit, minmax(140px, 1fr))`

---

## Decorative Elements

### Background Circles (depth effect)
```css
.bg-circle {
  position: absolute;
  width: 500px;
  height: 500px;
  border-radius: 50%;
  opacity: 0.03;
  background: #5B9A9A;
  filter: blur(100px);
}
```

### Floating Particles
```css
.particle {
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: #5B9A9A;
  opacity: 0.3;
  animation: float 8s ease-in-out infinite;
}
```

---

## Navigation (Presentations)

- **Progress bar**: 4px height, teal, fixed top of page
- **Arrow buttons**: 44x44px circles, `rgba(255,255,255,0.08)` background
- **Dot nav**: Fixed right side, 10px dots, teal active state
- **Slide counter**: Bottom-right, small text

---

## Applying This System

### For Instagram Carousels
- Use 1080x1080 slides with these colours, fonts, and card styles
- Dark backgrounds (gradient `#0a0a0a → #1a2a2a`) for most slides
- Teal gradient for accent/stat slides
- Space Grotesk for headlines, Inter for body
- Card-style content blocks where appropriate

### For Presentations
- Full-viewport slides with the same design system
- Include progress bar, navigation arrows, and slide counter
- Use pop-in animations and hover effects on cards
- Decorative background circles for depth

### Asset Libraries (in this folder)
- `icon-emblem-library.html` — Icon and emblem assets
- `overlay-asset-library.html` — Overlay design assets
- `social-media-asset-library.html` — Social media visual assets
- `social-media-asset-library-doc.html` — Social media asset documentation
