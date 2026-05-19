# Hafo Medical Management — Project Briefing

## What this project is
Single-page marketing website for **Hafo Medical Management Pte. Ltd.** — an AI-first dental operations platform targeting the **Google Cloud for Startups AI Program** ($350k credits). The site must simultaneously impress Google Cloud reviewers (technical credibility, real deployments, Vertex AI usage) and dental clinic operators (clinical trust, concrete ROI).

Live URL: **www.hafomedical.com**
GitHub: **github.com/meganho456/hafo-site**
Deployed via: **Vercel** (PAAD team, auto-deploys on push to `main`)

## Tech stack
- Plain HTML + Tailwind CSS (CDN, v3 Play)
- Vanilla JavaScript (no framework)
- Google Fonts: Inter + JetBrains Mono
- Single file: `index.html`

---

## Design system

### Color palette — GOLDEN (never use teal, cyan, or green accents)

| Token | Hex | Usage |
|-------|-----|-------|
| Gold primary | `#D4A843` | Accents, badges, CTAs, borders, highlights |
| Gold dark | `#B88D2C` | Gradient end, darker accents |
| Gold light | `#E8C060` | Secondary badges, warm text |
| Black | `#000000` | Hero, contact, footer backgrounds |
| Near-black | `#1D1D1F` | Stats band, about, partner sections |
| Off-white | `#F5F5F7` | Services, case studies light sections |
| Slate text | `#94A3B8` | Body text on dark backgrounds |
| Muted text | `#64748B` | Secondary text |

**Forbidden colors:** `#085041` `#1D9E75` `#5DCAA5` `#9FE1CB` `#E1F5EE` and any CSS class or variable containing `teal` or `green` (except the indigo/purple badge-indigo `#A78BFA` which is allowed as a tertiary accent, and the amber badge `#FCD34D` which is also allowed).

### CSS classes
```css
.badge-gold   { background: rgba(212,168,67,.12); color: #D4A843; border: 1px solid rgba(212,168,67,.28); }
.badge-warm   { background: rgba(232,192,96,.1);  color: #E8C060; border: 1px solid rgba(232,192,96,.25); }
.badge-amber  { background: rgba(245,158,11,.12); color: #FCD34D; border: 1px solid rgba(245,158,11,.25); }
.badge-indigo { background: rgba(99,102,241,.12); color: #A78BFA; border: 1px solid rgba(99,102,241,.25); }

.btn-primary  { background: linear-gradient(135deg, #D4A843, #B88D2C); color: #000; font-weight: 700; }
.btn-secondary { border: 1px solid rgba(148,163,184,.3); color: #94A3B8; }
.btn-secondary:hover { border-color: #D4A843; color: #D4A843; }

.dark-tile    { background: rgba(255,255,255,.04); border: 1px solid rgba(212,168,67,.15); }
.service-card { background: #fff; border: 1px solid #E2E8F0; }
.service-card:hover { border-color: rgba(212,168,67,.45); }
```

### Section background alternation
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

---

## Content & messaging

### Core positioning
- **For Google reviewers:** AI-first platform, Vertex AI + MedLM, PDPA-compliant, real deployments, Vertex AI time-series forecasting for inventory
- **For clinic operators:** reduce admin overhead, intelligent scheduling, no more manual rescheduling

### Key phrases to preserve exactly
- `"AI-Powered Operations for Modern Dental Clinics"` — hero headline
- `"Built securely on Singapore's PDPA compliant framework, leveraging Google Vertex AI and MedLM for customized fine-tuning."` — tech architecture quote
- `"Currently deployed and validated across premier partner clinics in Silicon Valley and Singapore"` — case studies

### Contact email
`hello@hafomedical.com` — do NOT use hafo.ai (domain not owned)

---

## Page sections (in order)
1. **Navbar** — fixed, transparent → frosted black on scroll, gold CTA button
2. **Hero** — black, grid pattern, gold radial glow, SVG agent diagram
3. **Stats band** — `#1D1D1F`, 4 metrics
4. **Services** — `#F5F5F7`, 2-col grid, 5 cards (4 regular + 1 full-width)
5. **Tech Architecture** — `#000`, PDPA/Vertex AI quote banner + code window + 3 pillars
6. **Case Studies** — `#F5F5F7`, Silicon Valley + Singapore location cards + deployment callout
7. **Partner Clinics** — `#1D1D1F`, 3-col grid of seed clinics
8. **About** — `#1D1D1F`, mission + 4-value grid
9. **Contact** — `#000`, partnership request form
10. **Footer** — `#000`, 4-col layout

---

## Service modules (5 total)
1. **Administrative AI Agent** — patient-doctor conversations, intelligent rescheduling, multi-channel comms
2. **Smart Practice Workflows** — multi-location scheduling, capacity balancing, waitlist backfill
3. **Data-Driven Operational Analytics** — production dashboards, no-show risk scoring, reporting
4. **Clinical Documentation AI** *(Coming Soon)* — MedLM voice-to-note, treatment plan docs
5. **AI Inventory Intelligence** — Vertex AI time-series forecasting, predictive reorder, expiry tracking

---

## Validated partner clinics
| Clinic | Location | Key credential | Website |
|--------|----------|---------------|---------|
| Palo Alto Advanced Dentists | Palo Alto, CA 🇺🇸 | Dr. James Ho DMD/MPH Harvard · Invisalign Elite Top 1% · 20+ yrs | paloaltoadvanceddentists.com |
| G Dental Center | Singapore (Ghim Moh + Orchard) 🇸🇬 | Est. 2001 · Invisalign · iTero · 2 locations | gdental.com.sg |
| GPlus Dental Center | Camden Medical Centre, Orchard 🇸🇬 | Dr. Javious + Dr. Bell · 30+ yrs · Implants + Aesthetics | gplusdental.com.sg |

---

## Deployment workflow
```bash
# Make changes to index.html, then:
git add index.html
git commit -m "describe change"
git push
# Vercel auto-deploys to www.hafomedical.com within ~30 seconds
```

## Domain & hosting
- **Registrar:** Squarespace (DNS managed there)
- **Host:** Vercel (PAAD team, Pro Trial)
- **DNS:** A record `@` → `76.76.21.21` · CNAME `www` → `cname.vercel-dns.com`
- **Email:** hello@hafomedical.com (to be set up via Google Workspace)
