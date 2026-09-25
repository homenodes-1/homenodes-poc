# Bill of Materials

**Status:** Planned (not yet purchased)
**Last updated:** 2026-09-25
**Currency:** CAD, before GST unless noted

## Purpose

Hardware for a single residential AI compute node, operated as a host on the Vast.ai distributed GPU marketplace. The node provides a live reference system for validating the security, privacy, and energy sections of the HomeNodes Governance Framework.

## Components

| # | Component | Specification | Qty | Est. cost | Supplier | Status |
|---|---|---|---|---|---|---|
| 1 | GPU | NVIDIA GeForce RTX 5080, 16GB GDDR7 | 1 | $1,700 | TBD | Planned |
| 2 | CPU | AMD Ryzen 7 9700X, 8-core | 1 | $450 | TBD | Planned |
| 3 | Motherboard | AM5 B850 ATX, IOMMU support | 1 | $280 | TBD | Planned |
| 4 | Memory | 64GB DDR5-6000 (2x32GB) | 1 | $1,300 | TBD | Planned |
| 5 | Storage | 2TB NVMe PCIe Gen4 SSD | 1 | $300 | TBD | Planned |
| 6 | Power supply | 1000W 80+ Gold, ATX 3.1 | 1 | $220 | TBD | Planned |
| 7 | Case | Mid-tower ATX, high airflow | 1 | $150 | TBD | Planned |
| 8 | CPU cooler | Tower air cooler | 1 | $60 | TBD | Planned |
| 9 | UPS | 1500VA line-interactive | 1 | $350 | TBD | Planned |
| 10 | Firewall | Mini PC, dual NIC, OPNsense | 1 | $350 | TBD | Planned |
| 11 | Energy monitoring | Smart plug with energy metering | 1 | $30 | TBD | Planned |
| 12 | Network | Cat6 cable run and patch cables | 1 | $50 | TBD | Planned |

| | Amount |
|---|---|
| **Subtotal** | $5,240 |
| GST (5%) | $262 |
| **Total** | **$5,502** |
| Approx. USD | ~$3,800 (before tax) |

## Design decisions

**Single consumer GPU.** Representative of what individual residential hosts run. A multi-GPU build would exceed a standard residential circuit and look more like a small commercial operation than a household node.

**RTX 5080 over RTX 5090.** RTX 5090 retail pricing in Canada exceeded $6,000 CAD in September 2026. The RTX 5080 stays within budget while remaining in the high-end consumer class used by marketplace hosts.

**64GB system memory.** Renters favour hosts with system RAM well above GPU VRAM. This is the most expensive line after the GPU due to the 2025 to 2026 DRAM shortage.

**IOMMU-capable motherboard.** Required to enable virtual machine support on the host, which improves verification likelihood and broadens eligible workloads.

**Dedicated firewall.** Isolates the node from the household network and provides traffic logging for the security domain of the framework.

**UPS.** Protects hardware and supports the uptime expectations of the hosting platform.

## Operating environment

| Item | Detail |
|---|---|
| Location | Residential basement, elevated off floor |
| Electrical | Standard 15A / 120V residential circuit |
| Estimated peak draw | ~550W (GPU 360W TDP, CPU 65W TDP, system overhead) |
| Internet | 1 Gbps symmetrical residential fibre/cable |
| Platform | Vast.ai |
| Operating system | Ubuntu Server LTS |

## Excluded

- Monitor, keyboard, and mouse (existing equipment, used for setup only)
- Electrical work (not required at this power level)
- Home router (existing)

## Funding

The HomeNodes BlueDot Impact Rapid Grant application includes USD $1,200 for reference node deployment. Hardware costs above that amount are self-funded by the project.

## Pricing notes

GPU and memory prices in Canada were elevated and volatile in 2026 due to supply shortages driven by AI data centre demand. Estimates reflect Canadian retail pricing in September 2026. Actual costs will be recorded here at purchase, with supplier and date.
