# HomeNodes Proof of Concept

Documentation for a single residential AI compute node, operating in Medicine Hat, Alberta.

## Purpose

The node is the Phase 1 study: one live residential node, measured under a protocol fixed in advance. It shows what a household hosting AI compute can see, what its power and network data reveal, and where existing rules stop applying. Findings feed the risk and governance work in [homenodes-framework](../../../homenodes-framework).

## Contents

| Folder | Contents |
|---|---|
| `hardware/` | Bill of materials, component specs, build photos |
| `build-log/` | Dated build and operations entries |
| `diagrams/` | Network, system architecture, and energy monitoring diagrams |
| `config/` | Setup scripts and configuration files |
| `monitoring/` | Monitoring setup and dashboard screenshots |
| `gap-log/` | Governance gap log, one entry per gap |
| `enclosure-concept/` | Future-phase enclosure concept. Not the POC spec |

Folders are added as work progresses.

## Status

**Phase 1:** Single-node study. Planned. Hardware has not been purchased.

## Research

| Document | Contents |
|---|---|
| [PHASE-1.md](PHASE-1.md) | Phase 1 at a glance: questions, setup, schedule, cost, and limits, with a diagram. Start here. |
| [PROTOCOL.md](PROTOCOL.md) | Phase 1 measurement protocol: research questions, study periods, methods, and planned analysis. Draft until the node is listed. The v1.0 commit date is the pre-registration date. |
| [RESEARCH-LIMITS.md](RESEARCH-LIMITS.md) | What the project will and will not do about adding compute to a public compute platform (no promotion of hosting, no scaling beyond the research sample, no commercial product). |
| [BUDGET.md](BUDGET.md) | Phase 1 budget, milestones, and actual spend. |

## Security note

Published configuration and diagrams are sanitized. IP addresses, credentials, device identifiers, and ISP account details are removed or replaced with placeholders.

## Related

- Governance framework: [homenodes-framework](../../../homenodes-framework)
- Project site: [homenodes.ca](https://homenodes.ca)
- Contact: research@homenodes.ca

## License

Code and configuration files are licensed under the [MIT License](LICENSE).
