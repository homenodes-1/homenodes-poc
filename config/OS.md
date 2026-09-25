# Operating System Selection

**Decision:** Ubuntu Server 24.04 LTS (64-bit, AMD64)
**Status:** Decided, not yet installed
**Last updated:** 2026-09-25

## Decision

The node will run Ubuntu Server 24.04 LTS, installed bare-metal with no desktop environment.

## Rationale

**Platform requirement.** Vast.ai supports Ubuntu Server 22.04 LTS and 24.04 LTS for hosts, with 24.04 recommended. Newer releases are not supported.

**Bare-metal GPU access.** The Vast.ai host daemon needs direct access to the NVIDIA driver to monitor and control the GPU. Windows with WSL2 does not provide this reliably and is not supported.

**Container isolation.** Renter workloads run in Docker containers, isolated using Linux control groups. Ubuntu provides mature, well-documented support for Docker and the NVIDIA Container Toolkit.

**Long-term support.** 24.04 LTS receives standard security updates into 2029, covering all planned project phases.

**Server edition only.** No desktop environment reduces the attack surface, background services, and idle power draw.

## Alternatives considered

| Option | Reason not selected |
|---|---|
| Ubuntu 26.04 LTS | Newer, but not supported by Vast.ai for hosts |
| Ubuntu 22.04 LTS | Supported, but shorter remaining support window |
| Debian 12 | Not the platform's documented host OS |
| Windows 11 with WSL2 | Not supported for hosting; unreliable GPU management |
| Proxmox or other hypervisor | Adds a layer the platform does not require; complicates GPU passthrough and power measurement |

## Governance notes

These constraints are relevant to the security and compliance domains of the framework:

- **Major OS upgrades are prohibited by the platform.** Upgrading between Ubuntu releases breaks the host software. The operator is locked to a release until the machine is rebuilt. Patch-level updates within the release are expected.
- **The platform, not the operator, controls what runs.** Renter workloads are containerized images chosen by the renter. The operator does not see or approve the workload in advance.
- **The operator remains responsible for the host.** Patching, driver updates, physical security, and network isolation sit with the household.

## Planned baseline configuration

Details will be documented separately once the node is built.

- Minimal Ubuntu Server install, OpenSSH only
- SSH key authentication, password login disabled
- Automatic security updates for the base OS (patch level only)
- NVIDIA proprietary or open driver with current CUDA release
- Docker with NVIDIA Container Toolkit
- Vast.ai host daemon
- Node placed on an isolated network segment behind a dedicated OPNsense firewall
- System and network logging retained for research
