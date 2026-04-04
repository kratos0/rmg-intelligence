# RMG Intelligent Operations Platform — Prototype

Claude-powered prototype of the RMG WFM intelligence layer. Validates that production bot prompts and the data injection pattern work identically on Claude as on Microsoft Copilot.

## Bots Included
- **Intraday Bot v2.1** — Morning Outlook, Midday Check-In, EOD Post Mortem, Daily Summary, Next Day Outlook
- **Short Range Bot v1.1** — Week Outlook, Optimize Schedule, Shift Bid, Week Brief
- **Long Range Bot v1.1** — Weekly Variance Review, Driver Analysis, Meeting Prep, 13-Week Forecast Review
- **Intelligence Bot v1.0** — Daily Brief, Weekly Summary, Monthly Review

## How to Use
1. Open the hosted URL (or `index.html` locally in Chrome)
2. Enter your Anthropic API key (`sk-ant-...`) — used in-browser only, never stored
3. Select a TRC (ONC / RARE / PACE / ALL)
4. Click any trigger button or type a custom phrase
5. Claude runs the analysis using your actual bot system prompts + synthetic staffing data

## Architecture
- Single `index.html` — no build step, no backend
- React 18 + Babel Standalone via CDN
- Synthetic interval-level staffing data (seeded by date, repeatable)
- Claude `claude-sonnet-4-6` via direct browser API call
- Evernorth brand palette (Tempermint / Hypermint / Champagne / Darkmint)

## Data
Synthetic data substitutes for Verint/SharePoint. Seeded by date so every session on the same day produces identical data. ONC, RARE, PACE queues with realistic vol/AHT/headcount ranges.

---
*Internal prototype — Evernorth RMG | Confidential*
