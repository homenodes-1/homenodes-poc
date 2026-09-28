# N1 Enclosure Concept (Future Phase)

**Status:** Concept only. Not part of the proof of concept. Nothing in this folder has been built, priced, or tested.

## POC hardware

The proof of concept spec is [`BOM.md`](/hardware/BOM.md): the RTX 5080 desktop build. That remains the only hardware being purchased and tested in the current phase.

## What this folder is

Early design work for a modem-sized node that could be shipped to homes and installed in later phases. It is sized for DGX Spark class hardware (compact unified-memory compute module), which is a different hardware class from the POC desktop build. The two are not interchangeable, and results from the POC node will not transfer directly to this enclosure.

The enclosure is here because form factor affects the governance questions in the framework (physical security, installation, liability, who can open the box). Hardware targets in these boards are research variables, not a finalized spec. See `homenodes-framework/drafts/distribution-models.md` for how install paths map to the five governance domains.

## Boards

| File | Shows |
|---|---|
| `n1-exterior.png` | Vertical enclosure, about 220 x 180 x 60 mm. Chimney airflow, single status light, side vents, tamper-sensing lid. |
| `n1-internals.png` | Cross-section, top to bottom: exhaust fan, tamper switch, heat sink, compute module, encrypted NVMe storage, TPM and management board, energy meter, power supply, intake filter. |
| `n1-rear-panel-and-mounting.png` | Two external cables only (power and a dedicated 10 GbE network port), sealed fasteners, service port behind a sealed cover, lock slot, wall-mount keyholes, and the three install path options. |

## Revision history

- 2026-09-28: Boards exported and added.
