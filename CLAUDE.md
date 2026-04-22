# Clay.com Personalized Landing Pages — Project Brief

## What This Project Is

An account executive at clay.com is building **personalized static HTML landing pages** for outbound prospects. Each page is tailored to a specific prospect — their company, role, and inferred pain points — with Clay's value proposition mapped directly to those pain points. The goal is hyper-personalized outreach at scale.

---

## Files in This Folder

| File | Purpose |
|---|---|
| `landing-page-prospects.csv` | The prospect list (5 contacts) — includes `personalized_url` column |
| `clay_icp.txt` | Clay's Ideal Customer Profile |
| `clay_value_prop.txt` | Clay's value proposition, use cases, and stats |
| `index.html` | Main landing page index — links to all 5 prospect pages |
| `sarah-mitchell-retool.html` | Landing page — Sarah Mitchell, Retool ✅ |
| `marcus-chen-linear.html` | Landing page — Marcus Chen, Linear ✅ |
| `emily-rodriguez-loom.html` | Landing page — Emily Rodriguez, Loom ✅ |
| `james-okonkwo-webflow.html` | Landing page — James Okonkwo, Webflow ✅ |
| `rachel-goldstein-airtable.html` | Landing page — Rachel Goldstein, Airtable ✅ |
| `CLAUDE.md` | This file |

---

## Prospect List

| Name | Title | Company | Website |
|---|---|---|---|
| Sarah Mitchell | VP of Revenue Operations | Retool | retool.com |
| Marcus Chen | Head of Growth | Linear | linear.app |
| Emily Rodriguez | Director of Sales Development | Loom | loom.com |
| James Okonkwo | GTM Engineer | Webflow | webflow.com |
| Rachel Goldstein | VP of Sales | Airtable | airtable.com |

---

## What's Been Built

### `sarah-mitchell-retool.html` ✅

A fully self-contained static HTML landing page for **Sarah Mitchell, VP of Revenue Operations at Retool**.

**Research on Retool used to inform the page:**
- ~466 employees, ~$120M ARR, hybrid PLG + enterprise sales motion
- 68 quota-carrying reps, full SDR team, dedicated RevOps function
- Outbound motion ramped aggressively since 2022, targeting VPs of Engineering and Internal Platform Leads
- Rapid sales team growth (3 AEs in 2020 → 68+ reps) = layered, fragmented GTM stack

**Four pain points featured:**
1. Enrichment gaps for niche technical personas (VPs of Engineering, Internal Platform Leads)
2. Fragmented GTM stack from rapid sales team growth (Apollo + ZoomInfo + Outreach + Clearbit)
3. SDR research overhead — 30–45 min per account for technical buyers
4. Stale CRM data at scale (68+ reps, Salesforce records going stale)

**Four Clay solutions mapped to each pain point:**
1. Waterfall Enrichment — cascades through 150+ providers, 43% → 91% coverage example
2. Claygent AI Research Agent — auto-researches accounts, generates SDR briefs in seconds
3. GTM Stack Consolidation — replaces 5 tools with one platform
4. Automated CRM Enrichment Sync — job-change detection, auto-updates Salesforce records

**Page sections (top to bottom):**
- Sticky nav (official Clay logo + personalization chip + "Book Demo" CTA button)
- Hero (split layout: left = headline + CTAs, right = live mock Clay product table)
- Pain Points (4 numbered statement list items — bold statement + consequence line)
- Solutions (4 alternating two-column blocks, each with copy + live visual panel + result badge)
- Social Proof (1 featured quote + 2-column quote grid + 3 stat cards + customer logo strip)
- CTA section (demo bullet list + interactive calendar)
- Footer

**Design (redesigned — session 2):**
- Deep dark theme (`#080808` background)
- Accent: warm orange `#f97316`
- Fonts: `Space Grotesk` (headlines) + `DM Sans` (body) — replaces Inter
- Official Clay primary logo from clay.com CDN (AVIF, inline `<img>`)
- Split hero with floating mock Clay product panel (enrichment statuses, Claygent briefs)
- Gradient mesh (orange + violet) + noise texture overlay on hero
- Custom orange scrollbar, glow CTA button, result badges on each solution
- Pain points as numbered statement list (not cards)
- 3 customer quotes: featured full-width + 2-column grid

**Calendar:**
- Custom-built interactive calendar widget (vanilla JS)
- Shows available weekday slots for the next ~45 days
- Selecting a day shows 30-min time slots
- Confirming opens Calendly in a new tab
- **Calendly URL placeholder:** `https://calendly.com/your-link` — swap this string when ready

---

### `marcus-chen-linear.html` ✅

**Research:** Linear — 178 employees, $100M ARR, Series C ($1.25B valuation), PLG-first motion scaling upmarket.

**3 pain points:** (1) PLG usage signals not tied to enriched contact data for enterprise buyers, (2) Apollo/ZoomInfo miss niche engineering personas (CTOs at developer-tool startups), (3) Custom enrichment pipelines require engineering time to build and maintain.

**3 Clay solutions:** Waterfall Enrichment (38% → 89% on eng personas), Claygent AI briefs from GitHub/hiring signals, GTM Stack Consolidation.

**Accent color:** Purple `#8b5cf6`

---

### `emily-rodriguez-loom.html` ✅

**Research:** Loom — acquired by Atlassian for $975M, 120K customers, PLG + sales-assisted motion, Director of Sales Development role.

**3 pain points:** (1) 120K self-serve users with no enriched view of enterprise conversion targets, (2) Post-Atlassian acquisition, SDRs need Atlassian ecosystem context they can't research at scale, (3) High research time + low personalization quality = broken SDR motion.

**3 Clay solutions:** Waterfall Enrichment (self-serve users → enriched enterprise prospects), Claygent (Atlassian signal detection), Automated CRM Enrichment Sync.

**Accent color:** Teal `#06b6d4`

---

### `james-okonkwo-webflow.html` ✅

**Research:** Webflow — $212M ARR (66% YoY growth), 1,292 employees, $4B valuation, hybrid PLG + enterprise, GTM Engineer role.

**3 pain points:** (1) Usage analytics and Salesforce are siloed — reps lack product signals in CRM, (2) Every new enrichment use case requires a custom pipeline from the GTM engineer, (3) 200K+ users with no scalable way to surface enterprise-ready accounts.

**3 Clay solutions:** GTM Stack Consolidation (replace custom scripts), Automated CRM Sync (no custom code), Waterfall Enrichment at scale.

**Accent color:** Blue `#3b82f6`

---

### `rachel-goldstein-airtable.html` ✅

**Research:** Airtable — $478M ARR, 134 quota-carrying reps, 500K+ customers, 80% of Fortune 100, land & expand motion, AI-native pivot announced.

**3 pain points:** (1) 500K customers × 134 reps = impossible to prioritize without real-time enrichment, (2) Land & expand requires org charts to find next buyer — 30–45 min per account manually, (3) AI-native rebrand requires identifying AI-workflow accounts — no signal layer exists in current stack.

**3 Clay solutions:** Waterfall Enrichment (real-time expansion signals), Claygent (AI workflow signals + next-buyer research), Automated CRM Enrichment (500K records kept fresh).

**Accent color:** Gold `#eab308`

---

## Design Decisions & Conventions to Carry Forward

- **One file per prospect** — fully self-contained HTML, no build step, no external dependencies except Google Fonts + Clay CDN logo
- **File naming:** `[first-name]-[last-name]-[company].html` (e.g. `sarah-mitchell-retool.html`)
- **Personalization depth:** Research each company before writing copy. Infer role-specific pain points. Map Clay's features to those specific pains with concrete examples in callout boxes.
- **CTA placement:** "Book a Demo" / calendar is at the **bottom** of the page, after all pain points and solutions have been addressed
- **Calendar:** Always use the same custom calendar widget with the Calendly placeholder URL
- **No external JS frameworks** — vanilla HTML/CSS/JS only
- **Logo:** Always use the official Clay logo from `https://cdn.prod.website-files.com/61477f2c24a826836f969afe/6778506d788ebf16fef48551_Clay%20primary%20logo.avif`
- **Fonts:** `Space Grotesk` for headlines, `DM Sans` for body — do not revert to Inter
- **Hero layout:** Split (left: copy + CTAs, right: mock Clay product panel) — hide right panel on mobile
- **Pain points:** Numbered statement list format (not cards)
- **Solutions:** Alternating blocks with `result-badge` under each callout
- **Social proof:** Always include 3 quotes minimum (1 featured full-width + 2 in a grid)

---

## All Pages — Status

- [x] Sarah Mitchell — VP of Revenue Operations — Retool
- [x] Marcus Chen — Head of Growth — Linear
- [x] Emily Rodriguez — Director of Sales Development — Loom
- [x] James Okonkwo — GTM Engineer — Webflow
- [x] Rachel Goldstein — VP of Sales — Airtable

**All 5 pages are complete and live.**

---

## Deployment

All pages are hosted on Vercel. **Production URL:** https://clay-landing-pages-dun.vercel.app

| Prospect | Live URL | Accent Color |
|---|---|---|
| Sarah Mitchell · Retool | `/sarah-mitchell-retool.html` | Orange `#f97316` |
| Marcus Chen · Linear | `/marcus-chen-linear.html` | Purple `#8b5cf6` |
| Emily Rodriguez · Loom | `/emily-rodriguez-loom.html` | Teal `#06b6d4` |
| James Okonkwo · Webflow | `/james-okonkwo-webflow.html` | Blue `#3b82f6` |
| Rachel Goldstein · Airtable | `/rachel-goldstein-airtable.html` | Gold `#eab308` |

**To redeploy after changes:** run `vercel --prod --yes` from the project folder.

---

## Per-Page Color Differentiation

Each page keeps the same dark theme and orange Clay CTA buttons, but the headline gradient text and accent highlights differ per prospect:
- The `.grad` CSS class controls the headline gradient color
- `stat-num` gradient, scrollbar color, and panel border glows match per page
- Bold text in pain points uses the page's accent color

---

## CSV & Clay Integration

- `landing-page-prospects.csv` has a `personalized_url` column with all 5 live page URLs
- All 5 rows have been sent to Clay via webhook (POST to Clay webhook endpoint)
- Each row was sent as JSON with all fields including `personalized_url`

---

## GitHub

Project is version-controlled and pushed to GitHub.

- **Repository:** https://github.com/HimPaul98/clay-landing-pages
- **GitHub account:** HimPaul98
- **Branch:** `main`
- **Files tracked:** all 10 project files (5 landing pages, index, CLAUDE.md, CSV, ICP + value prop txts)

**To push future changes:**
```
git add .
git commit -m "describe what you changed"
git push
```

---

## Owner

Account Executive at clay.com — Himadri Paul (`himadripaul98@gmail.com`)
