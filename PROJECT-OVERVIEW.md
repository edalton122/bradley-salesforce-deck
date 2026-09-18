# Bradley Company — Salesforce Executive Microsite
### Project Overview for Solution Engineers

---

## 🔗 Quick Links

| Resource | URL |
|---|---|
| **Live Microsite** | https://edalton122.github.io/bradley-salesforce-deck/ |
| **Executive Summary** | https://edalton122.github.io/bradley-salesforce-deck/exec-summary.html |
| **Business Value Assessment** | https://edalton122.github.io/bradley-salesforce-deck/bva.html |
| **Team Page** | https://edalton122.github.io/bradley-salesforce-deck/team.html |
| **GitHub Repo** | https://github.com/edalton122/bradley-salesforce-deck |

---

## Account Snapshot

| Field | Detail |
|---|---|
| **Company** | Bradley Company |
| **HQ** | South Bend, IN |
| **Industry** | Commercial Real Estate — Brokerage, Asset Services, Multifamily |
| **Revenue** | ~$540M |
| **Employees** | ~300–350 real estate professionals nationally |
| **Brokers** | 63 active brokers across South Bend, Fort Wayne, Grand Rapids |
| **Key Contacts** | Brianna Gladding (Mgr, Brokerage Ops), John (leadership) |
| **AE** | Justin Earls — jearls@salesforce.com |
| **SE** | Eric Dalton — edalton@salesforce.com |
| **RVP** | Grant Stephens — gstephens@salesforce.com |
| **Implementation Partner** | Fortimize (CRE Salesforce specialist) |

### Current Tech Stack (Pain Points)
- **Yardi Voyager** — property management, financials, AR (stays as system of record)
- **Dealius** — legacy AR system creating a dual-AR-system problem (to be sunset)
- **Outlook** — brokers live here; no CRM sync today
- **Excel / PipeDrive / sticky notes** — deal tracking is fragmented
- **ClickUp** — task management, disconnected from CRM

### Core Narrative
Bradley has a **two AR system problem** (Dealius + Yardi) that creates redundant tech spend and daily manual re-keying. Salesforce solves this by:
1. Becoming the single CRM + deal execution + commission platform
2. Integrating bi-directionally with Yardi (Yardi stays as financial ledger)
3. Enabling native AR functionality (commission tracking, invoice gen, AR aging) so Dealius can be sunset
4. Giving 63 brokers a **mobile-first Agentforce experience** — the primary selling point

---

## Microsite Structure

The deck is a single-page interactive HTML presentation with **10 slides** navigated by a fixed dot-nav on the right side. Each slide is a full-viewport section.

| # | Slide ID | Label | Description |
|---|---|---|---|
| 1 | `slide-1` | **Overview** | Hero with headline "Your Brokers' Easy Button." — key stats ($540M revenue, 63 brokers, 8+ years Salesforce relationship), pain pills, and product stack cards |
| 2 | `slide-2` | **Challenge** | Three flip-card pain points with before/after reveals (Fragmented Intel, Manual Reporting, Dual AR System) |
| 3 | `slide-3` | **Platform** | Salesforce product overview — Sales Cloud, Agentforce, MuleSoft, Service Cloud with expandable detail drawers |
| 4 | `slide-4` | **Broker AI** | Mobile-first Agentforce demo — screen recording plays inside a generic smartphone frame; 3-step flow explanation on the left |
| 5 | `slide-demo` | **Try It** | **Interactive phone simulator** — 8-screen guided demo of a broker's day using Agentforce (see detail below) |
| 6 | `slide-5` | **Connected Ops** | Before/After toggle — chaotic disconnected system lines animate into a Salesforce hub-and-spoke model; Dealius animates into the hub showing AR absorption |
| 7 | `slide-6` | **AI Architecture** | 5-layer stack (Data Sources → Integration → Trust → AI → Applications); clicking each layer reveals a detail panel on the right |
| 8 | `slide-7` | **Dashboard** | Interactive Salesforce Lightning UI mockup — KPI tiles, Deal Pipeline table, Broker Activity bars, Win/Loss donut chart |
| 9 | `slide-bvc` | **Value Calc** | Business Value Calculator with 4 tabbed categories and sliders (see detail below) |
| 10 | `slide-9` | **Path Forward** | "Where This Takes You" growth cards + 6-month Fortimize Project Timeline (interactive Gantt) + Collaboration for Success org chart |

---

## Key Interactive Features

### 🎮 Try It — Interactive Phone Demo (Slide 5)
An 8-screen CSS phone simulator simulating a full broker day powered by Agentforce. Each screen is navigated by tapping the phone. Features:

| Screen | What Happens |
|---|---|
| 1 — Broker's Day | Agentforce daily summary with voice dictation invite |
| 2 — Ask Agentforce | Voice prompt: "What should I focus on today?" |
| 3 — Lead List | 3 near-South-Bend leads; Greenfield Capital pulsates to indicate it's clickable |
| 4 — Lead Detail | Greenfield Capital Partners — $1.8M lease, voice note logging with live typewriter dictation animation |
| 5 — Task Created | Agentforce logs task + suggests email draft ("Want Agentforce to draft an email based on your voice notes?") |
| 6 — Email Draft | Live typewriter generation of a full email; animated send button |
| 7 — Pipeline Dashboard | Salesforce Lightning UI with Deal Velocity tab pulsating; drill into charts |
| 8 — AI Alert | Real-time Agentforce push notification sliding in — AI score increased alert |

**Announcement header** at the top of the slide tells first-time viewers it's interactive with an animated 👇 finger pointing to the phone.

### 📊 Connected Ops — Before/After Toggle (Slide 6)
- **"After Salesforce" button pulses/glows** while in Before state to draw attention
- Clicking triggers a **multi-phase animation**:
  1. Chaotic red lines converge toward the Salesforce hub
  2. UI flips to After state
  3. Dealius card flies into the Salesforce hub, shrinks, fades out
  4. Yardi repositions to center-right with a new horizontal connector
  5. "Commission Tracking · Invoice Gen · AR Aging" badge fades in below the hub
- Fully reversible — clicking Back resets all animations

### 🏗️ AI Architecture — Layer Drill-Down (Slide 7)
5 clickable layers. Selecting any layer slides in a detail panel on the right with:
- Layer name and label
- 3 bullet points explaining capabilities
- A callout quote

**Layers:** Yardi Voyager + Existing Data → Salesforce Integration Layer → Einstein Trust Layer → Agentforce · AI Layer → Sales Cloud + Reports & Dashboards

> **Note:** Data Cloud is intentionally **not** referenced — it is not scoped for this deal. Layer 2 is framed as the "Salesforce Integration Layer" (open API integration).

### 📉 Business Value Calculator (Slide 9)
4 tabbed categories with adjustable sliders. Totals update in real time and sum to a grand total.

| Tab | Key Sliders | Formula |
|---|---|---|
| **Broker Productivity** | # brokers (63), hrs saved/week (3), hourly rate ($75) | brokers × hrs × rate × 52 |
| **Reporting & Forecasting** | hrs/week (8), staff (2), rate ($50) | hrs × staff × rate × 52 |
| **Systems Integration** | re-entry hrs/week (10), staff (3), rate ($35) PLUS AR revenue ($200M), manual error rate (1% → 0.1%) | labor cost + revenue × (manual% − 0.1%) |
| **Revenue Growth** | pipeline $M (15), win rate lift (8%), commission rate (4%) | pipeline × win lift × commission rate |

> **Revenue Leakage stat**: Justin Earls confirmed 1% manual error rate; automated systems benchmark at 0.1%. At $200M AR revenue this is ~$1.8M/year in prevented leakage.

### 📅 Project Timeline — Interactive Gantt (Slide 10)
The Gantt matches the Fortimize proposal exactly. **Click any work stream row** to expand a detail panel with Scope & Deliverables + Business Outcomes pulled verbatim from the Fortimize proposal slides.

| Row | Color | Content on Click |
|---|---|---|
| CRM + Broker Command Center | 🟢 Green | 5 scope bullets + 3 outcomes |
| Brokerage Deal Workflows | 🟢 Green | 3 scope bullets + 3 outcomes |
| Reporting → AR Functionality | 🟢 Light Green | 5 scope bullets + 3 outcomes |
| Data Migration, Outlook & Yardi | 🟡 Gold | 3 scope bullets + 3 outcomes |
| User Testing & Feedback | 🔴 Red | 3 scope bullets + 3 outcomes |
| Change Management | 🔵 Blue | 3 scope bullets + 3 outcomes |

**Milestones:** Kickoff (September) → Go-Live #1 (Month 4) → Go-Live #2 (Month 6)

---

## Supplementary Pages

### `exec-summary.html` — Executive Summary
A clean, print-friendly 1-page overview designed for C-suite sharing. Covers:
- Challenge & narrative (dual AR system problem)
- Solution summary (Sales Cloud, Agentforce, Yardi integration)
- 6-month implementation roadmap (Discovery → Configuration → Enablement)
- CTA with team contact info

### `bva.html` — Business Value Assessment
A print-to-PDF formatted document based on the extracted BVA PDF with improved formatting, including:
- SVG donut chart showing value breakdown by category
- Stacked bar chart for visual comparison
- Detailed assumptions table with basis for each number
- 6-month roadmap (aligned to exec-summary)
- All value assumptions listed with AE commentary

### `team.html` — Account Team Page
Headshot cards for:
- Justin Earls (Account Executive)
- Eric Dalton (Solution Engineer)
- Grant Stephens (Regional Vice President)

---

## Narrative & Messaging Guide

### What NOT to say
| ❌ Avoid | ✅ Use Instead |
|---|---|
| "Replace Dealius" | "Solve the dual-AR-system problem" / "Sunset Dealius" |
| "Data Cloud" | Not in scope — omit entirely |
| "Tableau" | "Salesforce Reports & Dashboards" |
| "Phase 1 / Phase 2 / Phase 3" | "Discovery & Architecture / Configuration & Build / Enablement & Go-Live" |
| "90-day path" | "6-month implementation roadmap" |
| "Pilot project" | "Identify a target feedback group" / "The build process" |
| "AWS Bedrock" | "Model-Agnostic Foundation Models" / "AI Layer" |

### Core value hooks (from discovery)
1. **Mobile-first is the #1 selling point** — brokers don't want to open a laptop; Agentforce on mobile with voice-to-CRM is the "easy button"
2. **Change management is the named blocker** — the deck addresses this directly; framing is always "low friction, broker-shaped"
3. **Dual AR problem** — two separate AR systems (Dealius + Yardi) creating daily re-keying, reconciliation, and redundant spend
4. **Fortimize CRE accelerator** — 60–70% pre-built for CRE brokerage; not a custom build, not a risk
5. **8-year relationship** — Bradley has evaluated Salesforce since 2018; this isn't a product fit gap, it's a trust + ROI-proof gap

---

## File Structure

```
Bradley Company - Executive Deck/
├── index.html          # Main microsite (10 slides, all interactive features)
├── exec-summary.html   # Print-ready executive summary
├── bva.html            # Business Value Assessment (print-to-PDF)
├── team.html           # Account team page with headshots
├── demo-loop.mp4       # Processed Agentforce mobile demo video (Slide 4)
├── photo-ae.png        # Justin Earls headshot
├── photo-rvp.png       # Grant Stephens headshot
└── photo-se.jpg        # Eric Dalton headshot
```

---

## How to Clone and Run Locally

```bash
git clone https://github.com/edalton122/bradley-salesforce-deck.git
cd bradley-salesforce-deck
open index.html
```

No build step, no dependencies. Pure HTML/CSS/JS. Works in any modern browser.

To make changes and push to the live site:
```bash
# Edit files, then:
git add -A
git commit -m "your change description"
git push
# GitHub Pages auto-deploys in ~2 minutes
# Hard refresh: Cmd+Shift+R
```

---

## Reusable Skills (for next customer)

This project generated two reusable Cursor AI skills:

### `customer-deck-generator` skill
Generates a full branded HTML exec deck from scratch given:
- Customer website URL
- Salesforce products in scope
- Tech stack / pain points
- Call transcript or notes
- AE / SE / RVP names and emails

**Path:** `/Users/edalton/.cursor/skills/customer-deck-generator/SKILL.md`

### `mobile-demo-simulator` skill
Generates the interactive CSS phone simulator (the "Try It" slide) for any company/use case. Includes:
- Complete CSS shell for a generic modern smartphone frame
- JS state machine template for multi-screen navigation
- Screen library with 8 archetypes (dashboard, voice dictation, AI draft, notification, etc.)
- Customization checklist and common pitfalls

**Path:** `/Users/edalton/.cursor/skills/mobile-demo-simulator/SKILL.md`

---

## Recent Change Log (last 10 commits)

| Commit | Change |
|---|---|
| `5cf180d` | Make Gantt chart interactive with Fortimize deliverable detail panels |
| `48d8a95` | Replace vertical timeline with Fortimize Gantt + polish org chart |
| `10bfd39` | Add Collaboration for Success org chart from Fortimize proposal |
| `494048a` | Address AE feedback: remove Data Cloud, add revenue leakage BVC slider, 6-month timeline |
| `c3c2d7e` | Update roadmap: replace pilot language with feedback group framing |
| `1c180b9` | Connected Ops: animate Dealius absorption into Salesforce hub |
| `f6004d7` | Update narrative: solve dual-AR-system problem; remove Tableau from scope |
| `3b87da7` | Soften AWS Bedrock references on AI Architecture slide |
| `f2f968a` | Replace all instances of DLAS with Dealius |
| `927becb` | Change hero title to "Your Brokers' Easy Button." |

---

*Built with Cursor AI · Hosted on GitHub Pages · Last updated September 2026*
*Questions: Eric Dalton — edalton@salesforce.com*
