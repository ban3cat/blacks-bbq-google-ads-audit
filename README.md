# Google Ads Campaign Audit & Restructure — The Original Black's BBQ

## What It Is

A full Google Ads account audit and restructure for The Original Black's BBQ, a legendary Central Texas BBQ chain (est. 1932) with locations in Austin, Lockhart, New Braunfels, and San Marcos. The analysis diagnosed a budget allocation flaw that was quietly starving the account's most efficient markets, then produced a step-by-step restructure plan to fix it.

---

## The Problem

The non-brand campaign was running all four locations under a single shared $30/day budget using Maximize Clicks. On the surface, the numbers looked fine — low CPCs, decent volume. But under the hood, Austin's massive search volume was consuming 60%+ of the daily budget before Lockhart and New Braunfels could capture their audiences.

The result: the account's best-performing market (New Braunfels, $8.00 CPA) was receiving roughly $3.20/day, while Austin ($17.90 CPA) was burning through $18+/day. The algorithm was optimizing for volume, not efficiency — and nobody had looked at the location-level data to see it.

Additional issues surfaced in the search term report:
- **Brand cannibalization:** 310 clicks and $59.91 in spend were being consumed by the client's own brand name inside the non-brand campaign — traffic that should have routed through the separate $10/day Brand campaign
- **Competitor leakage:** 407 competitor-related search terms (Terry Black's, Bill Miller, Cooper's, etc.) were triggering non-brand ads, wasting budget on users who were explicitly looking for a competitor

---

## The Solution & Impact

**Diagnosis:** Pulled location-level performance data and mapped CPA and conversion rate by market, revealing a 2x+ CPA gap between Austin ($17.90) and New Braunfels ($8.00) within the same campaign.

**Restructure plan delivered:**

1. **Campaign split** — Isolated Austin into its own campaign to stop it from hogging shared budget. Grouped New Braunfels, San Marcos, and Lockhart into a dedicated Regional campaign with its own $25/day budget
2. **Bidding strategy shift** — Recommended transitioning from Maximize Clicks to Maximize Conversions on the Regional campaign, which had crossed the 30-conversion/month threshold required for Google's ML to optimize effectively
3. **Macro budget reallocation** — Shifted Conquer campaign from $10/day to $5/day and redirected $10 more/day into the non-brand structure, increasing total non-brand budget from $30 to $40/day
4. **Negative keyword build** — Added phrase-match negatives for own brand terms ("black's", "blacks", "the original black's") and 8+ competitor names to stop budget leakage
5. **Competitor keyword strategy** — Built a structured keyword list for the Conquer campaign by market (Austin, New Braunfels, San Marcos, Lockhart), targeting competitors by name with phrase match to control CPC and intent

**Performance snapshot (April 2026 — period analyzed):**

| Metric | Non-Brand | Brand | Conquer | Account Total |
|---|---|---|---|---|
| Spend | $912.29 | $304.34 | $304.04 | $1,520.68 |
| Clicks | 3,406 | 3,802 | 1,280 | 8,488 |
| Conversions | 64 | 121.5 | 36.5 | 222 |
| CPA | $14.25 | $2.50 | $8.33 | $6.85 |
| Conv. Rate | 1.88% | 3.20% | 2.85% | 2.62% |

**Location-level efficiency gap (non-brand campaign):**

| Location | Spend | Conversions | CPA | Conv. Rate |
|---|---|---|---|---|
| Austin | $548.84 | 30.67 | $17.90 | 1.56% |
| San Marcos | $142.78 | 9.33 | $15.30 | 1.64% |
| Lockhart | $124.66 | 12.00 | $10.39 | 2.42% |
| New Braunfels | $96.01 | 12.00 | $8.00 | 3.20% |


The location-level gap was the core finding: same campaign, same budget, same keywords — but New Braunfels was converting at 2x the rate of Austin at less than half the CPA.

---

## Tech Stack

`Google Ads` · `Looker Studio` · `Google Ads Search Terms Report` · `Google Ads Keyword Planner`

---

## Demo / Screenshots

📊 [View the Looker Studio Dashboard (April 2026)](./Original_Black's_BBQ_Dashboard.pdf)

> *Dashboard includes: account overview, campaign performance, ad group breakdown, keyword performance, search query report, device split, demographic data, and geographic performance.*

---

## How It Works

1. **Export & audit** — Pulled the Search Terms report (2,690+ unique queries) and mapped performance by location ad group to surface the budget allocation problem
2. **Location-level analysis** — Compared CPA and conversion rate across all four markets within the single campaign to quantify the efficiency gap
3. **Structural diagnosis** — Identified that Maximize Clicks + shared budget = Google optimizes for click volume in high-search-volume markets, not for conversion efficiency
4. **Negative keyword mining** — Scanned the search term report for brand and competitor terms bleeding into the non-brand campaign; built phrase-match negative lists to block them
5. **Restructure blueprint** — Produced a prioritized action plan: campaign split, bidding shift, budget reallocation, negative keyword implementation, and ad scheduling recommendations
6. **Competitor keyword build** — Mapped the Central Texas BBQ competitive landscape by city and built a structured phrase-match keyword list for the Conquer campaign

---

## What I Learned / Key Decisions

- **Structure before budget.** The instinct when a campaign is "limited by budget" is to raise the budget. The right move was to diagnose *why* the budget was being consumed — the fix was structural, not financial.
- **Let location data tell the story.** The account-level numbers (3,406 clicks, $0.27 CPC) looked healthy. The efficiency gap only became visible when the data was broken out by location ad group. Rollup metrics can hide serious inefficiency.
- **Don't dismiss Google's recommendations — understand them.** The "Missing enough relevant keywords" alert looked like a gap to fill. It was actually a signal that tight match types were working as intended, and Google's algorithm was flagging them because they limited its expansion options. Knowing the difference saved the client from diluting a lean, efficient keyword set.

---

## Setup & Usage

This project documents an audit and strategy engagement — it is not a standalone script or tool. The methodology is replicable for any multi-location Google Ads account:

1. Pull 30-day Search Terms report filtered by location ad group
2. Break out CPA and conversion rate by location (not just campaign rollup)
3. Cross-reference search query report against brand and competitor term lists
4. Identify whether bidding strategy and campaign structure match the account's data maturity (conversion volume threshold for Smart Bidding: ~30 conv/month per campaign)
5. Apply campaign split before raising budget

---

*Part of a series documenting real agency work in paid search, reporting, and marketing operations.*
