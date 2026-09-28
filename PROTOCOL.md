# Phase 1 Measurement Protocol

**Status:** Draft v0.1. To be finalized and committed before the node is listed on Vast.ai. The commit date serves as the pre-registration date.
**Last updated:** 2026-09-28
**Applies to:** The single proof-of-concept node described in [hardware/BOM.md](hardware/BOM.md)
**Related:** [ETHICS.md](https://github.com/homenodes-1/homenodes-framework/blob/main/ETHICS.md), [RESEARCH-LIMITS.md](RESEARCH-LIMITS.md), [ROADMAP.md](https://github.com/homenodes-1/homenodes-framework/blob/main/ROADMAP.md)

## Purpose

This protocol sets out what the proof of concept measures, how, for how long, and how the results will be analyzed. It is written before data collection so the findings can be checked against a plan that was fixed in advance.

## Research questions

| # | Question | Framework domains |
|---|---|---|
| RQ1 | What can a residential host observe about the workloads and renters on their hardware, using only the interfaces normally available to a host? | Security, Liability, Regulatory |
| RQ2 | Can power and network metadata distinguish types of AI workload, and at what measurement resolution does that stop working? | Security, Regulatory |
| RQ3 | How much energy does a residential node use in each operating state, and how does that compare with the household's normal load? | Zoning and land use, Regulatory |
| RQ4 | What governance gaps does a household encounter when setting up and operating a node? | All five |

RQ1 and RQ2 are the core AI safety questions. They test whether oversight approaches built for data centers (hardware telemetry, energy reporting) can reach residential compute.

## Study periods

| Period | Target dates | Node status | Purpose |
|---|---|---|---|
| Baseline | 2 weeks, Oct 2026 | Built, not listed | Idle power, benchmark workloads, measurement checks |
| Operation | 8 weeks, Nov 2026 to Jan 2027 | Listed on Vast.ai | Renter workloads, visibility audit, gap log |
| Close-out | 1 week, Jan 2027 | Unlisted | Repeat benchmarks, compare with baseline |

Dates follow the project roadmap. If the start slips, the durations stay the same.

## RQ1: Host visibility audit

The host visibility audit records what a host is able to see, not what renters are doing. In line with the ethics statement, workload contents and renter identity are never collected.

**Method.** Each interface available to a host is checked at the start of each rental period and once a week during operation:

- Vast.ai host dashboard and host CLI
- Docker container metadata on the host
- GPU process and utilization tools (nvidia-smi)
- Firewall connection metadata (OPNsense)
- Platform notices and emails to the host

For each interface, the audit records only whether each item below is exposed, and at what level of detail (none, partial, full):

- Renter identity or account details
- Container image name or source
- Commands or processes running in the container
- Model or dataset being used
- Network destinations contacted by the workload
- Rental duration and GPU hours

**Recording rule.** The audit records "exposed: yes, partial, or no" and a description of the category. It never records the value itself. For example, if a container image name is visible, the audit notes that image names are visible. It does not record which image was running.

**Output.** A visibility matrix (interface by item), published in full.

## RQ2: Workload identifiability

**Method.** During the baseline and close-out periods, the project runs its own labelled benchmark workloads on the node. Because these are the project's own workloads, their type is known without inspecting any renter activity.

| Label | Workload |
|---|---|
| Idle | Node on, no workload |
| Inference | Open-weight language model serving batched requests |
| Fine-tuning | Small open-weight model fine-tuned on a public dataset |
| Image generation | Open-weight image model generating a fixed batch |
| Non-AI GPU load | Standard GPU stress or rendering benchmark |

Each workload runs at least three times, for at least 30 minutes each, at different times of day.

**Measurements.** Power at the wall (node circuit only), GPU power and utilization from nvidia-smi, and network volume and connection counts at the firewall. All are recorded at 1-second intervals where the hardware allows.

**Analysis.** The data is resampled to three resolutions:

- 1 second (dedicated monitoring hardware)
- 1 minute (typical smart plug or home energy monitor)
- 15 minutes (typical utility interval meter)

At each resolution, a simple classifier is trained on labelled benchmark runs and tested on held-out runs. The result reported is how accurately workload type can be identified at each resolution, and which signals (power, network, or both) carry the information.

Renter-period data is summarized by operating state (idle, low, high load) but not labelled by workload type, since that would require inspecting renter activity.

**Why this matters.** If workloads can't be told apart at utility meter resolution, energy data alone is not a workable oversight tool for residential compute. If they can, it raises privacy questions that the framework needs to address. Either result is useful.

## RQ3: Energy use

**Method.** Power at the node circuit is recorded continuously for all three periods. The node's consumption is cross-checked against the utility meter over a fixed period (see risk R14).

**Reported.**

- Average and peak draw in each operating state
- Total energy use per week and for the full study
- Estimated electricity cost at the published Medicine Hat residential rate
- Node consumption as a share of a typical Medicine Hat household's electricity use, based on published figures (whole-home use of the study household is not measured, per the ethics statement)

## RQ4: Governance gap log

**Method.** Every point where a household faces a question that existing rules don't clearly answer is logged when it happens, from purchase through close-out. Sources include ISP terms, insurance, platform terms, electrical and building rules, privacy obligations, and incident handling.

**Entry format.**

| Field | Content |
|---|---|
| ID | G-001, G-002, ... |
| Date | YYYY-MM-DD |
| Stage | Purchase, setup, listing, operation, incident, close-out |
| Domain | Security, Privacy, Zoning and land use, Liability, Regulatory |
| What happened | The situation, in plain terms |
| Question | The question no rule clearly answers |
| Rules checked | What was consulted, with links where public |
| Outcome | What the household did, and on what basis |
| Framework note | What the framework should say about it |

**Output.** The full gap log, published and mapped to the five domains. It feeds gap analysis v0.2 and draft framework v0.5.

## Data collected and published

| Data | Frequency | Retained | Published as |
|---|---|---|---|
| Node circuit power | 1 s where possible | Study period plus 2 years | Aggregated and time-shifted |
| GPU power and utilization | 1 s | Study period plus 2 years | Aggregated |
| Firewall volume and connection counts | 1 min | Study period plus 2 years | Aggregated, no addresses |
| Rental records (start, end, GPU hours) | Per rental | Study period plus 2 years | Aggregated |
| Visibility audit | Per rental and weekly | Permanent | In full |
| Benchmark run data | Per run | Permanent | In full |
| Gap log | Per event | Permanent | In full |

Nothing listed as not collected in the ethics statement is collected here.

## Equipment

The smart plug in the BOM must support local data export at 1-second or near 1-second intervals. Plugs that only report through a cloud app at longer intervals are not suitable for RQ2. The BOM will be updated with the specific device once selected.

## Deviations

Any change to this protocol after the node is listed is recorded in the CHANGELOG with the date and reason. Findings are reported against the protocol as committed, with deviations noted.

## Outputs

By the end of Phase 1:

1. Host visibility matrix (RQ1)
2. Workload identifiability results at three resolutions (RQ2)
3. Energy dataset and summary (RQ3)
4. Governance gap log (RQ4)
5. Short public report covering all four, including negative findings and limitations

## Limitations

- One node, one household, one platform. Results show what is possible, not how common it is.
- Benchmark workloads are chosen by the project and may not reflect what renters actually run.
- Visibility findings apply to Vast.ai at the time of the study. Platform changes are logged as findings (see risk R9).
- Low rental demand would limit RQ1 and RQ3 data from the operation period (see risk R5). Low demand is itself reported.
