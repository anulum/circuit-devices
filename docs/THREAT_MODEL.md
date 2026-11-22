<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-DEVICES — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- TCAD meshes, process parameters and Verilog-A sources;
- bench `I-V`/`C-V` captures and wafer scribe-line distributions.

They grant no authority to:
- overwrite a production technology profile without an approved change proposal;
- link `GPL` Verilog-A compilers in-process;
- extrapolate compact models silently outside their conformal domain.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Overfitted symbolic or TCAD compact models producing non-physical SPICE behaviour outside measured bias ranges | Candidates must pass thermodynamic passivity, Gummel symmetry, charge conservation, per-wafer `WAT`/`PCM` residual anchoring, conformal out-of-domain deferral and change-proposal approval |
| Copyleft Verilog-A compiler contamination | `OpenVAF-Reloaded` (`GPL-3.0`) runs strictly as a separate process over file boundaries |

## Residuals named, not removed

- **Unmeasured wafer lots.** Lot-to-lot drift beyond characterised `WAT`/`PCM` wafers is flagged by conformal shift deferral rather than predicted silently.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
