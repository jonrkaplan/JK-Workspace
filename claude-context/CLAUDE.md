# CustomGPT.ai — GTM & Operations Context

*Last updated: 2026-04-16 | Source files: CustomGPT_HubSpot_Playbook_v2.docx, GTM_Operations_Observations_v19.docx, PageZero.rtf, Strategy.rtf*

---

## How to Help Me

- At the end of every session, update this file with new insights, decisions, and patterns learned.

---

## Who Is Jon Kaplan

Jon is CustomGPT.ai's Operations/GTM leader (~4 weeks in as of April 2026). MBA-educated, experienced across multiple orgs. Brought in to diagnose and fix the GTM engine while simultaneously firefighting the sales vacuum. Reports to Alden Do Rosario (CEO). Works closely with Raj Kapoor (CEO advisor, Amazon operational background).

**Jon's dual mandate:** (1) Execute now — close deals in front of us, (2) Build for scale — fix process/systems gaps preventing growth 3–5 months out.

---

## The Team

| Person | Role | Assessment |
|--------|------|------------|
| Alden Do Rosario | CEO | Approves decisions; supports Jon taking operational direction |
| Raj Kapoor | CEO Advisor | Amazon rigor framework; drives "vocally self-critical" culture |
| Bobby Duquette | Post-sales / AM | HubSpot owner ID 78926705; insanely bright but chases shiny objects; needs focused lanes |
| Cameron / Cam | Solutions Engineering | HubSpot owner ID 81643110; technically sharp, client-facing; underleveraged on low-value calls |
| Ally | AE / Sales Rep | Nearly hit $80K quota with zero coaching structure; asked Jon for help; deserves proper eval once support is in place |
| Obby / Abby | Sales Leader | Not functioning as leader; acts as senior IC; no process/framework; lied to Jon; sandbagging numbers — change may be necessary |
| Abhi | Sales Team | Runs daily deal sync with Ali/Jon |

---

## Company Context

- **Product:** CustomGPT.ai — enterprise AI deployment platform (V3 launched: Web Search, Doc Analyst)
- **Model:** Bootstrapped (no venture cushion — every person, hour, dollar must produce)
- **Philosophy:** AI-first (scale 1 to 20 people doing work of 100; don't hire out of problems)
- **Growth target:** 200–500%
- **Headline diagnosis:** "Zero operational rigor. Sales is broken. The GTM engine cannot deliver growth targets in its current state."
- **AI multiplier principle:** AI amplifies whatever system it's pointed at — broken process × AI = faster dysfunction

---

## Account Management Infrastructure

### Two-Pipeline Model
1. **Jon's Pipeline** — renewal deals at current ARR (Renewal Pipeline ID: 709891656)
2. **Expansion Revenue Pipeline** — incremental ARR only

### Renewal Tranche Model
| Tranche | Criteria | Action |
|---------|----------|--------|
| Will Grow | Green/yellow health, risk 0–3, multi-dept, active engagement | Proactive expansion push |
| Will Renew | Stable, risk 3–5, single dept, moderate engagement | Standard renewal motion |
| Churn Risk | Red health, risk 6+, underutilizing, declining usage, no contact 60–90+ days | Immediate intervention |

### NRR Formula
`(Beginning ARR + Renewal Increase ARR + Expansion Won ARR - Churned ARR) / Beginning ARR`

### 7 Automated Remote Triggers (Anthropic cloud infrastructure)
| Day | Time | Automation |
|-----|------|-----------|
| Monday | 7:30 AM | Deal Stage Progression — auto-moves renewal deals based on renewal_date thresholds |
| Monday | 8:00 AM | Enterprise Weekly News Digest — scans Gmail, Calendar, BigQuery, Slack, web; ranks as Action Required / Watch / Expansion / Healthy |
| Monday | 8:00 AM | Renewal Countdown Alerts — 30/14/7-day thresholds |
| Tuesday | 8:00 AM | Renewal Data Flags — missing tranche, probability, health, stale activity alerts |
| Wednesday | 8:00 AM | Usage Decline Alerts — BigQuery scan for >20% MoM decline, 30+ days no login |
| Thursday | 8:00 AM | Open Issue Scan — #customer-issues + #acct- threads within 90 days of renewal |
| Friday | 8:00 AM (bi-weekly) | Product Update Matching — #product-updates → account use case matching |
| Daily | Weekday mornings | Daily Digest Canvas — posts to #daily-digest (book snapshot, open issues, renewal queue, tasks, expansion pipeline) |

All automations run at https://claude.ai/code/scheduled. Plain text markdown only (no Block Kit, no JSON blocks).

### HubSpot Key Properties
`renewal_tranche`, `renewal_increase_arr`, `expansion_type`, `expansion_trigger` (9 options), `hs_forecast_probability`, `hs_forecast_amount`

**Expansion Trigger options:** Usage Near Limit, Overage Active, Renewal Approaching, New Champion, Feature Released, EBR Insight, Customer Request, Self-Serve, Outbound Proactive

### Slack Structure
38 enterprise account channels (#acct-[companyname]). Bobby and Cameron invited to all. GDrive links pinned in each.

---

## 13 Structural GTM Gaps (Priority Remediation)

1. **Focus the GTM Motion** — No defined ICP; spread across too many segments. Define target segment hypothesis (Apr 16), align outbound to ICP (May 1).
2. **Pipeline Quality Over Volume** — Enterprises negotiated down to $2K; activity confused with qualification. Hard disqualification criteria (Apr 16), qualification challenge questions (May 1).
3. **Marketing Not Connected to GTM** — Separate track; no ICP collaboration; not accountable to pipeline. Bring into weekly GTM cadence (May 1).
4. **Deal Execution Lacks Structure** — No call prep/debrief, no slides, deals go dark silently. Daily deal standup (started Apr 7), pre-call prep standard (Apr 14).
5. **Sales Leadership vs. Management** — Obby not developing reps, not owning forecast. Redefine expectations (Apr 16); evaluate fit (May 7).
6. **PoC Model Needs Restructuring** — 90-day cycles without advancing deals; unclear ownership. Shift to 12-month agreements with opt-out clauses (May 1).
7. **Forecasting Not Operational** — Doesn't live in HubSpot; $150K projected 2 days before month-end vs. $60K confirmed. Migrate to HubSpot with stage-exit criteria (May 7).
8. **AM Blind Spots** — Baulig churned as surprise; single-threaded accounts; reps don't know existing customers. Multi-threading standard: min 2 contacts per enterprise, 1 exec (May 7).
9. **Product Velocity Constraint** — Baulig built competing solution in hours; stickiness beyond deployment speed needed. Push stickiest features into every account (May 7).
10. **Solutions Engineering Underleveraged** — Cam on low-value calls. Audit Cam's load (Apr 16); redirect to high-leverage work (May 1).
11. **No Operational Infrastructure** — No playbooks, no RACI clarity, no documented deal lifecycle. Document lifecycle + RACIs (May 7); SOPs for top 3 workflows (May 15).
12. **Morale Needs Attention** — Team sees churn/sales gaps; structurally demoralized, not lazy. 1:1s (Apr 16); weekly cadence highlights wins; moving to dedicated office May 1.
13. **AI Use Standard** — Team using AI to replace thinking, not augment it. Define AI+human standard per workflow (May 7); human judgment layer on all customer-facing deliverables (Apr 16).

---

## Key Frameworks

### 3Ps Reporting (PageZero — Wednesday AM with Alden)
- **Progress** — Key wins, closed deals, strategic moves, customer highlights
- **Problems** — Structural blockers, technical issues, team challenges, customer friction
- **Plans** — Next actions, upcoming campaigns, infrastructure builds
Format: Smart brevity / Axios style — 2 bullets per category.

### Amazon Operational Rigor (Raj Kapoor)
- Vocally self-critical: "Here's where we screwed up, here's our plan"
- Action items: Step A/B/C/D + owner + target date
- Monthly review: Last meeting's items → current status
- Nothing is "impossible" — list inputs, list what needs to happen, go make it happen

---

## Key Dates & Milestones

| Date | Milestone |
|------|-----------|
| Apr 7 | Daily deal standups launched |
| Apr 14 | Weekly forecast call launched |
| Apr 16 | ICP segment hypothesis; renewal calendar; Cam audit; Obby expectations; 1:1s |
| Apr 17–27 | Jon OOO |
| Apr 28 | Full sync resumes |
| May 1 | PoC model restructure; marketing in GTM cadence; sales leader expectations redefined; office move |
| May 7 | Pipeline audit; HubSpot forecast migration; multi-threading standard; deal lifecycle documented |
| May 15 | Demo enablement/cert; AI+human standards; Cam redirected; SOPs for top 3 workflows |
| Jun 1 | Forecast accuracy baseline review |
| Aug 1 | 90-day retrospective on revenue translation from ICP focus |

---

## Key Accounts Referenced

**Churned / Churn Risk:** Baulig (built own solution; single-threaded; no exec sponsor — post-mortem planned), Lappin (deal stalled Jan–Mar; rep didn't follow up)

**Active Enterprise Book:** Bernco, Pepperdine, ALPA, Skuld, MCW, FranConnect, CIR Realty, Roodbont, TaxWorld, Sandals Church, Hamilton COOs, Kotter, GEMA, EK, Fuji, and others (see GDrive folder map in global CLAUDE.md)

---

## Technical Infrastructure Notes

- **HubSpot connectors required:** HubSpot, Slack, Gmail, Google Calendar, BigQuery
- **BigQuery datasets:** `customgpt-data-warehouse.prod_gold.gold_customer`, `gold_daily_usage`
- **Remote triggers:** https://claude.ai/code/scheduled (not local machine)
- **Dedicated Slack alerts account** required (not Jon's personal)
- **Slack Canvas API** used for daily digest
- **MCP tool discovery** required in all trigger prompts

## Session End Protocol
At the end of every session, always run: git add . && git commit -m 'Session update' && git push
