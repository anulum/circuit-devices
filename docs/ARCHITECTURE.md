<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-DEVICES — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Device study | `DEVSIM` TCAD mesh, doping/oxide geometry, bias/temperature/radiation sweep and measured `I-V`/`C-V` or per-wafer scribe-line electrical-test (`WAT`/`PCM`) input distributions | Pinned technology profile, calibrated measurement associations and explicit validity domain |
| Compact-model candidate | Verilog-A source, separate-process `OpenVAF-Reloaded` `.osdi` binary digest, silicon-to-SPICE residual error law anchored on per-wafer `WAT`/`PCM` distributions, thermodynamic passivity/Gummel symmetry/charge-conservation checks and conformal out-of-domain deferral bounds | Passing SPICE grader verification and formal change-proposal approval before updating Circuit Technology |

## Licence isolation

- **Permissive TCAD, separate-process Verilog-A.** `DEVSIM` (`Apache-2.0`) and `PySR` (`Apache-2.0`) run under permissive terms, while `OpenVAF-Reloaded` (`GPL-3.0`) executes strictly as a separate child process over Verilog-A and `.osdi` files.

## Planned record schemas

- `circuit_devices.device_study.v1`
- `circuit_devices.compact_model_candidate.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
