# Changelog

All notable changes to the HomeNodes proof of concept are recorded here.

Dates use YYYY-MM-DD.

## [Unreleased]

### Planned
- Build log with dated entries
- Network diagram and system architecture diagram
- Energy monitoring setup
- Node setup script

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
- BOM: funding note updated. Full hardware cost is in the planned BlueDot Impact application
- PROTOCOL: compute platform is now a research variable. RQ1 split into a desk comparison of three platform types and a live trial on one platform, run only on a connection whose terms allow hosting. Offer end date set to the end of the operation period. 16GB GPU memory limitation added
- RESEARCH-LIMITS: item 4 corrected. Hosts cannot end rental contracts early, so harmful use is reported to the platform and the node is unlisted
- BUDGET: internet line for the node added as a cost to be confirmed

## [Phase 1] - 2026-09-25

### Added
- Repository created
- README with purpose, structure, and security note
- MIT license
- Planned bill of materials (hardware/BOM.md)
- OS selection and rationale (config/OS.md)
