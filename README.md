# AE Expansion Dashboard

**A signal-driven expansion playbook tool for Account Executives, powered by Staircase AI and Gainsight CS.**

---

## Overview

The AE Expansion Dashboard surfaces accounts showing upsell and cross-sell readiness based on Staircase AI's expansion analysis. It gives AEs a single view of their expansion-ready portfolio, pre-built playbooks with recommended next actions and draft outreach, and a direct path to create CSQL CTAs in Gainsight CS.

This tool was built to solve a common gap in the AE workflow: expansion signals exist in Staircase AI, but AEs lack a fast, actionable way to see which accounts are ready, understand why, and take the next step. This dashboard closes that loop.

## What It Does

### Portfolio-Level Visibility
- Displays all accounts flagged by Staircase AI for expansion readiness, scored on a 1-5 scale
- Segments accounts into **High Signal (5/5)** and **Medium Signal (4/5)** tiers
- KPI summary cards show total expansion-ready accounts, high-signal count, and medium-signal count at a glance

### Filtering and Navigation
- **Owner filter** scopes the view to a specific CSM/AE's book of business (15 owners mapped from Staircase AI)
- **Signal strength filter** narrows to High or Medium signal accounts
- **Search** filters by account name or expansion area keywords
- **Tabbed views** for All Accounts, High Signal only, Medium Signal only, and Expansion Themes

### Pre-Built Expansion Playbooks
Every account has a ready-to-use playbook generated from Staircase AI signal data, including:
- **Signal Analysis** -- what Staircase is seeing and why the account is flagged
- **Recommended Next Action** -- a specific, concrete step for the AE
- **Outreach Talking Points** -- three signal-backed reasons to reach out
- **Draft Expansion Email** -- a personalized, consultative email the AE can edit, copy, and send

### Expansion Themes
A portfolio-wide view of the most common expansion areas across all accounts, with percentage breakdowns and account lists per theme.

### CSQL CTA Creation
After reviewing a playbook, the AE can create an Expansion-type CSQL CTA in Gainsight CS directly from the dashboard.

## Data Sources

| Source | What It Provides |
|--------|-----------------|
| **Staircase AI** (EmailMonkey instance) | Expansion readiness scores, signal summaries, expansion areas, account-to-owner mapping |
| **Gainsight CS** (Demo instance) | CTA type/status/priority/reason configurations for CSQL creation |

## Accounts Covered

- **30 accounts** at readiness level 5 (High Signal)
- **26 accounts** at readiness level 4 (Medium Signal)
- **56 total** expansion-ready accounts across 15 CSM/AE owners

## Tech Stack

- Single-file HTML application (no build step required)
- React 18 via CDN with Babel for JSX transpilation
- All data pre-loaded (no external API calls required for the static version)
- Designed for GitHub Pages deployment

## Deployment

1. Clone or fork this repository
2. The app is a single `index.html` file -- no dependencies to install
3. Enable GitHub Pages in **Settings > Pages** (source: main branch, root)
4. Access at `https://[username].github.io/ae-expansion-dashboard/`

## Claude.ai Integration

When run as an artifact inside Claude.ai, additional capabilities are available:
- **AI-powered playbook regeneration** via Claude Opus 4.6
- **Live CSQL CTA creation** in Gainsight CS through the MCP connector
- **Email regeneration** with fresh AI-drafted outreach
- **Refresh from Staircase** button pulls latest expansion signals via MCP

## Built With

This dashboard was built collaboratively in Claude.ai using:
- **Staircase AI MCP** for expansion signal data
- **Gainsight CS MCP** (Demo instance) for CTA configuration and creation
- **Claude Opus 4.6** for playbook generation
- Iterative design informed by the [CSM Risk Dashboard](https://ahumitz-coder.github.io/csm-risk/) pattern
