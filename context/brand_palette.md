# Brand Palette

## Golden palette — always use these

| Token       | Hex       | Usage                                      |
|-------------|-----------|--------------------------------------------|
| Gold primary | `#D4A843` | Accents, badges, CTAs, borders, highlights |
| Gold dark   | `#B88D2C` | Gradient end, darker accents               |
| Gold light  | `#E8C060` | Secondary badges, warm text                |
| Black       | `#000000` | Hero, contact, footer backgrounds          |
| Near-black  | `#1D1D1F` | Stats band, about, partner sections        |
| Off-white   | `#F5F5F7` | Services, case studies light sections      |
| Slate text  | `#94A3B8` | Body text on dark backgrounds              |
| Muted text  | `#64748B` | Secondary text                             |

Extended warm tokens (banners, cards, dark panels):

| Token       | Hex       | Use                         |
|-------------|-----------|-----------------------------|
| --midnight  | `#2C1E00` | Dark backgrounds, banners   |
| --espresso  | `#3D2B00` | Cards, panels, secondary bg |
| --gold      | `#C8880A` | Primary brand, borders, CTAs |
| --amber     | `#E5A120` | Secondary accent            |
| --honey     | `#F2C45A` | Headings on dark            |
| --cream     | `#FDF3DC` | Light background            |
| --parchment | `#F5E6C0` | Card backgrounds            |
| --sand      | `#E8D49A` | Dividers, subtle borders    |
| --charcoal  | `#2C2010` | Body text on light          |

## Forbidden colors — never use

`#085041` `#1D9E75` `#5DCAA5` `#9FE1CB` `#E1F5EE`

Any CSS class or variable name containing `teal` or `green`.

Allowed exceptions: `#A78BFA` (badge-indigo, tertiary accent) and `#FCD34D` (badge-amber).

## CSS badge / button classes

```css
.badge        { display: inline-flex; align-items: center; padding: 3px 12px; border-radius: 100px; font-size: .72rem; font-weight: 600; letter-spacing: .05em; }
.badge-gold   { background: rgba(212,168,67,.12); color: #D4A843; border: 1px solid rgba(212,168,67,.28); }
.badge-warm   { background: rgba(232,192,96,.1);  color: #E8C060; border: 1px solid rgba(232,192,96,.25); }
.badge-amber  { background: rgba(245,158,11,.12); color: #FCD34D; border: 1px solid rgba(245,158,11,.25); }
.badge-indigo { background: rgba(99,102,241,.12); color: #A78BFA; border: 1px solid rgba(99,102,241,.25); }

.btn-primary   { background: linear-gradient(135deg, #D4A843, #B88D2C); color: #000; font-weight: 700; }
.btn-secondary { border: 1px solid rgba(148,163,184,.3); color: #94A3B8; }
.btn-secondary:hover { border-color: #D4A843; color: #D4A843; }

.dark-tile    { background: rgba(255,255,255,.04); border: 1px solid rgba(212,168,67,.15); border-radius: 16px; }
.service-card { background: #fff; border: 1px solid #E2E8F0; border-radius: 18px; }
.service-card:hover { border-color: rgba(212,168,67,.45); }

.status-dot   { width: 8px; height: 8px; border-radius: 50%; background: #D4A843; animation: pulse-dot 2s ease-in-out infinite; }
```

## Section background alternation

```
Hero          → #000000
Stats band    → #1D1D1F
Services      → #F5F5F7  (light)
Tech Arch     → #000000
Case Studies  → #F5F5F7  (light)
Partners      → #1D1D1F
About         → #1D1D1F
Contact       → #000000
Footer        → #000000
```
