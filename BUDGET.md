# Budget and Milestones

**Status:** Phase 1 budget. The Phase 2 planning estimate is in [PHASE-2-BUDGET.md](https://github.com/homenodes-1/homenodes-framework/blob/main/PHASE-2-BUDGET.md).
**Last updated:** 2026-10-09
**Currency:** Funding amounts in USD. Purchase costs in CAD, as recorded in [hardware/BOM.md](hardware/BOM.md). Conversions use roughly 1 CAD = 0.73 USD.

## Phase 1 at a glance

| | |
|---|---|
| Period | 16 weeks from funding decision (target Oct 2026 to Jan 2027) |
| Funding need | USD $4,950 for node hardware and the dedicated internet line. No external funding secured yet |
| Self-funded | Electricity, website, domain, and email |
| Research time | Unfunded. Provided by the project lead alongside a full-time role |

## Phase 1 funding need (USD $4,950)

| Line | Amount | What it pays for | Milestone |
|---|---|---|---|
| Node hardware | $4,030 | All components in the BOM: CAD $5,523 including GST | M1 |
| Price buffer | $92 | GPU and memory prices in Canada are volatile (see risk R1). Any unspent amount is reported and returned or applied to project hardware with the funder's agreement | M1 |
| Dedicated internet line | $828 | CAD $1,133.79 including GST. Breakdown below | M2 to M7 |
| **Total** | **$4,950** | | |

**Internet line breakdown (CAD).** The node runs on a separate line from a local cable reseller whose terms allow servers for commercial use (see gap log G-001). Month-to-month, no contract, setup fee waived. Budgeted for four months, build to close-out.

| Item | Amount |
|---|---|
| Static public IPv4 address, no blocked inbound ports (one-time) | $600.00 |
| 1000 Mbps down, 50 Mbps up plan, unlimited data ($99.95 x 4 months) | $399.80 |
| Static IP service ($10 x 4 months) | $40.00 |
| Modem rental ($10 x 4 months) | $40.00 |
| Subtotal | $1,079.80 |
| GST (5%) | $53.99 |
| **Total** | **$1,133.79** |

If Phase 1 runs longer than four months, each extra month costs CAD $125.95 including GST and is self-funded.

**Why hardware and connectivity.** The research question is what a residential host can see and measure. That requires being a host. Renting cloud GPUs cannot answer it, and no existing dataset covers it. Hosting also requires a connection whose terms allow it, with a public IP address renters can reach. The household's standard residential service prohibits hosting (gap log G-001). The node and its line are the costs the project cannot work around, and the rest of Phase 1 can proceed without further funding.

**After Phase 1.** The node stays in service as the project's reference node for Phase 2. It is not resold for personal gain. Rental income is handled as set out below.

## Self-funded costs

| Item | Amount | Notes |
|---|---|---|
| Electricity for the study period | About CAD $150 | Up to about 1,000 kWh over 11 weeks at peak draw. City residential energy rate is $0.07/kWh plus surcharge and delivery charges. CAD $0.15/kWh used as a conservative all-in planning figure |
| Website, domain, and email | Recorded at actual cost | Squarespace, homenodes.ca, Microsoft 365 |
| Dedicated internet line beyond four months | CAD $125.95 per month | Only if Phase 1 runs past the budgeted four months |

## Not yet funded

These are part of the Phase 1 plan but not included in the Phase 1 funding need. They proceed on a volunteer basis unless separate funding is secured.

| Item | Status |
|---|---|
| Research time (protocol, gap analysis, framework drafting, Phase 1 report) | Provided by the project lead, unpaid |
| Expert interviews (compute governance researchers, platform operators, privacy specialists) | Planned without honoraria. Honoraria may be sought separately if response rates are low (see risk R3) |

## Rental income

Phase 1 rental income from the live platform is recorded here and applied to project costs, mainly electricity (see [RESEARCH-LIMITS.md](RESEARCH-LIMITS.md)).

| Period | Income (USD) | Applied to |
|---|---|---|
| | | |

## Milestones

Week 0 is the funding decision. Target dates assume a decision in October 2026.

| # | Milestone | Week | Target | Evidence of completion |
|---|---|---|---|---|
| M1 | Hardware purchased, actual costs recorded in the BOM | 2 | Oct 2026 | Updated BOM with suppliers, dates, and prices |
| M2 | Node built, hardened, isolated on the home network | 4 | Oct 2026 | Build log and sanitized configuration |
| M3 | Protocol v1.0 committed, baseline period complete | 6 | Nov 2026 | PROTOCOL.md v1.0 commit (pre-registration), baseline benchmark data |
| M4 | Node listed, operation period starts | 6 | Nov 2026 | First visibility audit entry, first gap log entries |
| M5 | Expert interviews complete | 8 | Nov 2026 | Anonymized interview summary |
| M6 | Gap analysis v0.2 and draft framework v0.5 | 12 | Dec 2026 | Both documents published in homenodes-framework |
| M7 | Operation and close-out complete, Phase 1 report published | 16 | Jan 2027 | Visibility matrix, identifiability results, energy dataset, gap log, public report |

## Funding sources

| Source | Amount | Status | Covers |
|---|---|---|---|
| Self-funded | See above | Committed | Electricity, website, research time |
| External funding | USD $4,950 | None secured | Node hardware and dedicated internet line |

No cost is funded twice. If more than one funder supports the project, any line covered by one is removed from the others, each funder is told, and the change is recorded here.

## Actual spend

Recorded as costs are incurred.

| Date | Item | Amount (CAD) | Funded by |
|---|---|---|---|
| | | | |

## Phase 2 and later

A planning estimate for Phase 2 is published in [PHASE-2-BUDGET.md](https://github.com/homenodes-1/homenodes-framework/blob/main/PHASE-2-BUDGET.md): about CAD $42,400 for five homes and about CAD $80,200 for ten. It is revised once Phase 1 data shows actual energy use and operating effort, and before any household is recruited. Later phases are not yet budgeted.
