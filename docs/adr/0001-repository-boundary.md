<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-DEVICES — repository foundation
-->

# Decision: isolate TCAD physics and Verilog-A/OSDI compact-model qualification in a conditional specialist repository

## Context

Standard digital or open-PDK designs consume existing compact models from Circuit Technology, whereas novel neuromorphic synapses, memristive devices, cryo/high-voltage cells or post-silicon corner shifts need dedicated TCAD and Verilog-A qualification.

## Decision

**What Circuit Devices owns:**
- device study;
- compact-model candidate;

**What it imports:** only Circuit Core and Circuit Technology.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| production technology profiles | Circuit Technology |
| circuit-level SPICE sign-off | Circuit Analog |
| bench `I-V`/`C-V` acquisition | Circuit Lab |
| wafer-sort `WAT` ingestion and change proposals | Circuit Manufacturing |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- Circuit Devices stays optional for standard digital flows while anchoring custom and post-silicon `OSDI` models cleanly;
- Circuit Technology updates only on approved, physics-checked candidates.
