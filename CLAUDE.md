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

## Contact email
`hello@hafomedical.com` — do NOT use hafo.ai (domain not owned)

---

## Context files

@context/brand_palette.md
@context/pms_compatibility.md
@context/architecture_spec.md

---

## Page sections (in order)
1. **Navbar** — fixed, transparent → frosted black on scroll, gold CTA button
2. **Hero** — black, grid pattern, gold radial glow, SVG agent diagram
3. **Stats band** — `#1D1D1F`, 4 metrics
4. **Services** — `#F5F5F7`, 2-col grid, 5 cards (4 regular + 1 full-width)
5. **Tech Architecture** — `#000`, PDPA/Vertex AI quote banner + code window + pillars + PMS Compatibility component
6. **Case Studies** — `#F5F5F7`, Silicon Valley + Singapore location cards + deployment callout
7. **Partner Clinics** — `#1D1D1F`, 3-col grid of seed clinics
8. **About** — `#1D1D1F`, mission + 4-value grid
9. **Contact** — `#000`, partnership request form
10. **Footer** — `#000`, 4-col layout + PMS badge strip

## Service modules (5 total)
1. **Administrative AI Agent** — patient-doctor conversations, intelligent rescheduling, multi-channel comms
2. **Smart Practice Workflows** — multi-location scheduling, capacity balancing, waitlist backfill, PMS compatibility bullet
3. **Data-Driven Operational Analytics** — production dashboards, no-show risk scoring, reporting
4. **Clinical Documentation AI** *(Coming Soon)* — MedLM voice-to-note, treatment plan docs
5. **AI Inventory Intelligence** — Vertex AI time-series forecasting, predictive reorder, expiry tracking

## Validated partner clinics
| Clinic | Location | Key credential | Website |
|--------|----------|----------------|---------|
| Palo Alto Advanced Dentists | Palo Alto, CA 🇺🇸 | Dr. James Ho DMD/MPH Harvard · Invisalign Elite Top 1% · 20+ yrs | paloaltoadvanceddentists.com |
| G Dental Center | Singapore (Ghim Moh + Orchard) 🇸🇬 | Est. 2001 · Invisalign · iTero · 2 locations | gdental.com.sg |
| GPlus Dental Center | Camden Medical Centre, Orchard 🇸🇬 | Dr. Javious + Dr. Bell · 30+ yrs · Implants + Aesthetics | gplusdental.com.sg |

## Key phrases to preserve exactly
- `"AI-Powered Operations for Modern Dental Clinics"` — hero headline
- `"Built securely on Singapore's PDPA compliant framework, leveraging Google Vertex AI and MedLM for customized fine-tuning."` — tech architecture quote
- `"Currently deployed and validated across premier partner clinics in Silicon Valley and Singapore"` — case studies

## Core positioning
- **For Google reviewers:** AI-first platform, Vertex AI + MedLM, PDPA-compliant, real deployments, Vertex AI time-series forecasting for inventory
- **For clinic operators:** reduce admin overhead, intelligent scheduling, PMS-agnostic deployment, no migration required

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

## Extended context files
- context/architecture_spec.md — full sync agent technical spec
- context/pms_compatibility.md — full PMS integration details and Plato note
