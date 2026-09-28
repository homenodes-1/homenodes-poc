# Research Limits and Acceleration Risk

**Status:** Project commitment. Applies to all phases.
**Last updated:** 2026-09-28

## The concern

The proof-of-concept node rents GPU time on a public compute marketplace. That adds capacity to the marketplace, and a project about residential compute could be read as encouraging more of it. This document explains why we accept that small footprint and what the project will not do.

## Why the footprint is small

The POC is one consumer GPU (the RTX 5080 build in `hardware/BOM.md`). Marketplaces like Vast.ai already host large numbers of consumer and data center GPUs. One more card does not change what renters can do.

It also does not add frontier capability. Frontier training runs use tens of thousands of data center GPUs with high-speed interconnects. A single residential consumer GPU cannot contribute to that work in any meaningful way. The concern this project studies is the long-term trend, not the capability of any one node.

## Why the research needs a live node

The core question is what a residential host can and cannot see about the workloads on their hardware, and whether power and bandwidth use are enough to identify a workload. That can't be answered from outside.

We considered two alternatives:

- **Simulated workloads only.** Useful for power baselines, and we will run them. They can't show what a host sees about real renters.
- **Interviewing existing hosts.** Useful, and planned for Phase 2. It gives self-reported answers, not measured ones.

A live node, combined with both of the above, is the smallest setup that produces direct evidence.

## What the project will not do

1. **No promotion of hosting.** We will not publish earnings figures as an incentive, guides to maximizing income, or anything that presents hosting as a side business. Build and configuration notes are published only at the level needed to reproduce the research.
2. **No scaling beyond the research sample.** One node in Phase 1. No more than ten homes in Phase 2, each under a written research protocol with a fixed end date. No further expansion without new funding, a new protocol, and public notice.
3. **No commercial product.** The enclosure concept and the distribution models (builder, ISP, utility) are governance research variables. They are not a business plan, and the project will not manufacture, sell, or broker nodes.
4. **No open-ended operation.** Each node comes off the marketplace at the end of its study period. A node is also pulled early if we find evidence it is being used for clearly harmful work.
5. **No evasion playbook.** Findings that could help someone avoid oversight (for example, which workloads can't be identified from power data) will be shared with compute governance researchers before publication, and published at the level of detail needed for policy, not for evasion.

## Rental income

Rental income is reported in the project's public records and applied to project costs, mainly electricity. It is not a funding source the project depends on.

## Review

These limits are reviewed at the end of each phase. Any change is recorded in the CHANGELOG.
