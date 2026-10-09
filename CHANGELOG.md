# Changelog

All notable changes to the HomeNodes proof of concept are recorded here.

Dates use YYYY-MM-DD.

## [Unreleased]

### Planned
- Build log with dated entries
- Network diagram and system architecture diagram
- Energy monitoring setup
- Node setup script

## 2026-10-09

### Added
- Phase 1 overview (PHASE-1.md): questions, setup, schedule, cost, and what Phase 1 cannot show
- Phase 1 overview diagram (diagrams/phase-1-overview.svg and .png)

### Changed
- README: purpose rewritten around the Phase 1 study. PHASE-1.md added to the research table
- BUDGET: funder names removed. Phase 2 section now points to the Phase 2 planning estimate in homenodes-framework
- RESEARCH-LIMITS: Phase 2 hardware is loaned and removed at the end. Phase 2 rental income is handled as in Phase 1, because the project owns and operates the nodes
- BUDGET and BOM: funding sections revised to list potential funders without application status. Status is disclosed directly to each funder
- CHANGELOG: funder names removed from earlier entries for the same reason. Amounts and dates are unchanged

## 2026-10-07

### Changed
- BUDGET: funding request rounded to USD $4,950 (nearest $50). Price buffer raised from USD $70 to USD $92
- BOM: funding note updated to the new request amount
- BUDGET and BOM: funding status updated

## 2026-09-29

### Changed
- BUDGET: dedicated internet line moved from self-funded to the funding request. CAD $1,133.79 for four months including the one-time static IP cost and GST. Funding request raised from USD $4,100 to USD $4,928
- BOM: static IP added to the internet line. Funding note updated to the new request amount

## 2026-09-28

### Added
- House system diagram (diagrams/homenodes-house-diagram.svg and .png, planned design)
- Future-phase N1 enclosure concept (enclosure-concept/). Not the POC spec. See hardware/BOM.md for the POC build
- Research limits and acceleration risk (RESEARCH-LIMITS.md)
- Phase 1 measurement protocol, draft v0.1 (PROTOCOL.md)
- Phase 1 budget and milestones (BUDGET.md)
- Governance gap log (gap-log/), first entry G-001: residential ISP terms prohibit hosting. Resolved the same day: a local reseller on the same network permits servers for commercial use

### Changed
- README: added Research section linking the protocol and research limits, and enclosure-concept folder
- BOM: energy monitor must support local data export at 1-second intervals (required by the protocol)
- BOM: funding note updated. Full hardware cost is in the planned funding request
- PROTOCOL: compute platform is now a research variable. RQ1 split into a desk comparison of three platform types and a live trial on one platform, run only on a connection whose terms allow hosting. Offer end date set to the end of the operation period. 16GB GPU memory limitation added
- RESEARCH-LIMITS: item 4 corrected. Hosts cannot end rental contracts early, so harmful use is reported to the platform and the node is unlisted
- BUDGET: dedicated internet line for the node added (about CAD $460 for the study period, self-funded)
- BOM: operating environment updated for the dedicated internet line
- PROTOCOL: live platform selected (Vast.ai) after the dedicated line was confirmed to have a static public IPv4 address with no blocked inbound ports. Upload limit noted
- Gap log G-001: IP address and port details confirmed. Status resolved

## [Phase 1] - 2026-09-25

### Added
- Repository created
- README with purpose, structure, and security note
- MIT license
- Planned bill of materials (hardware/BOM.md)
- OS selection and rationale (config/OS.md)
