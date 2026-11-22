<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-DEVICES — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Devices is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Pre-silicon device study** runs deterministic `DEVSIM` TCAD sweeps and compiles baseline `OSDI` models.
2. **Post-silicon wafer anchoring** ingests per-wafer scribe-line `WAT`/`PCM` distributions (`V_th`, `I_on`, `I_off`, sheet resistance, area capacitance, ring-oscillator period) and calibrated bench captures to fit silicon-to-SPICE error laws.
3. **Candidate qualification** checks passivity, asymptotic slope, charge conservation and conformal out-of-domain deferral before submitting a change proposal to Circuit Technology.

## Ownership

**This project owns** the planned Circuit Devices records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| production technology profiles | Circuit Technology |
| circuit-level SPICE sign-off | Circuit Analog |
| bench `I-V`/`C-V` acquisition | Circuit Lab |
| wafer-sort `WAT` ingestion and change proposals | Circuit Manufacturing |

## Interpretation

- **Domain of validity.** A compact model's residual bound holds only inside its characterised geometry, bias and temperature box.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
