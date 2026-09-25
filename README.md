# WattShed Engineering Notes

**Live product: [wattshed.co](https://wattshed.co)**

WattShed is software that creates, verifies and pays residential energy-efficiency rebates. A public, no-login designer covers all 50 states and DC, with methodology offerings that vary by location. The wider product turns program terms, homeowner evidence, deterministic calculations, and contractor milestones into an auditable operating record.

These notes make the work inspectable without publishing the implementation. They describe the product boundary, methodology, and verification record, not source code, prompts, secrets, or operational security details.

## Start here

- [Architecture at a glance](docs/architecture.md) explains the public product flow and the separation between AI-assisted review and deterministic decisions.
- [Methodology and data](docs/methodology-and-data.md) describes the calculation families, coverage, and estimation boundary.
- [Verification record](docs/verification-record.md) records the checked test result and the limits of that result.
- [Product boundaries](docs/product-boundaries.md) states what WattShed does and does not do, including its no-custody position.
- [Industrial Compute decision memo](docs/industrial-compute-decision-memo.md) frames the infrastructure problem the product is intended to address.

## Current public footprint

- 50 states plus DC in the no-login program designer
- 3,143 county records and 30 TMY3 climate packs
- 40 named modules across six suites, of which 30 were marked live self-serve in the checked source snapshot
- 1,416 passing automated tests in the verified local run on 2026-08-27

Those figures describe the repository snapshot reviewed on 2026-08-27. They are not a promise of future coverage, availability, savings, or program outcomes.

## Rights

Copyright © 2026 Omer Bese / Bonjuur, Inc. All rights reserved. These notes are published for reading. No permission is granted to copy, reuse, adapt, or redistribute any part of this repository or the product design it describes.
