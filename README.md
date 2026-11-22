<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-DEVICES — repository foundation
-->

# Circuit Devices

Circuit Devices is being built as the conditional specialist repository for semiconductor device physics, `DEVSIM` TCAD simulation, wafer-acceptance-test scribe-line anchoring and `OpenVAF-Reloaded` `OSDI` compact-model extraction and qualification — operating completely deterministically without requiring AI. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed TCAD study runner, compact-model extractor, OSDI compiler wrapper or qualified record schema.

Circuit Devices is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- a TCAD study runner, parameter extractor or `OSDI` compact-model qualifier;
- a registered runtime record schema;
- a qualified custom compact model.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Device study | `DEVSIM` TCAD mesh, doping/oxide geometry, bias/temperature/radiation sweep and measured `I-V`/`C-V` or per-wafer scribe-line electrical-test (`WAT`/`PCM`) input distributions |
| Compact-model candidate | Verilog-A source, separate-process `OpenVAF-Reloaded` `.osdi` binary digest, silicon-to-SPICE residual error law anchored on per-wafer `WAT`/`PCM` distributions, thermodynamic passivity/Gummel symmetry/charge-conservation checks and conformal out-of-domain deferral bounds |

**Static imports:** only Circuit Core and Circuit Technology.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Core and Circuit Technology | entity references, design views, operation profiles and technology profiles |
| Circuit Lab | measurement associations and calibrated bench captures |
| Circuit Manufacturing | change proposals, per-wafer `WAT`/`PCM` scribe-line distributions and corrective-action records |
| Circuit Flow | design-step learning records |

**Capability registration and handoffs:** Registers under the specialist tool-profile manifest with Circuit Core and supplies compact-model candidates to Circuit Analog, Circuit Technology, Circuit Lab, Circuit Manufacturing and Circuit Acceptance.

**Explicit non-claims and operating boundaries:**
- Every TCAD simulation and compact-model extraction flow works deterministically without machine learning (`DEVSIM`, Apache-2.0).
- Candidate equations from symbolic regression (`PySR`, Apache-2.0) or TCAD fits never enter Circuit Technology directly: they must compile via separate-process `OpenVAF-Reloaded` (`GPL-3.0`), pass passivity, charge-conservation, dual-SPICE and conformal shift-deferral gates, and carry an approved change proposal.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
