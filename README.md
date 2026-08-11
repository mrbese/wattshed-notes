# WattShed — Engineering Notes

**Live product: [wattshed.co](https://wattshed.co)** · The code is private by choice; the live app is the artifact. These notes document the design so the work is readable without opening the source.

WattShed is a rebate program creator and clearinghouse for private funders of residential energy efficiency: hyperscalers buying grid capacity and social license around data centers, and VPP operators buying dispatchable headroom. Funders pay contractors directly; WattShed designs and prices the program, verifies completion evidence, and issues payment instructions. It never custodies program funds.

## The one-number design

The client predetermines exactly one constant: dollars per kW of permanent demand reduction. Everything else derives from it.

For a hyperscaler, that number bakes the equivalent generation investment plus the community narrative into a single figure. Beyond the load reduction, the funder is buying social approval: the town's story flips from "the data center will raise my electric bill" to "the data center paid for my insulation, and my bill dropped the next month."

For a VPP, the number prices a resale opportunity: reducing a home's consumption frees the most profitable load at the most expensive hours, which the VPP sells back to the grid at prime time, on a horizon of up to 10 years.

Reducing the client's entire decision to one input was the point. A funder's leadership does not want a rebate methodology; they want a number they can compare against building generation.

## How it works

1. **Funders** design and price a program for any of 50 states + DC on a public, no-login program designer, computed live in the browser.
2. **Residents** apply through a guided wizard: address eligibility, upgrade categories, guided phone photos.
3. A **vision model** turns the capped photo set into a structured home audit. The server fetches photo bytes itself and hashes every image; client-supplied URLs are never trusted.
4. A **pure deterministic TypeScript qualification engine** computes savings, peak-kW relief, cost, and payout limits from the audit. The LLM packages results but cannot approve, deny, or reprice. The funding contract is math, not vibes.
5. **Milestones** clear against photo evidence, with rebates paid directly to the contractor. (Money movement is staged in v1; the live site says so plainly.)

## The engine

- Deemed-savings methodology digested from the regulator's own sources; the reference build implements Oncor / Texas TRM v13.0 (Climate Zone 3 HVAC and attic-insulation measures). The platform itself is methodology-universal, not Texas-specific.
- Modified-bin hourly simulation, UA envelope model, and degree-day engines with both summer and winter peak-kW methodologies.
- National coverage: 50 states + DC, 3,143 county entries, 30 NOAA climate packs.
- A 41-document building-physics research corpus behind the methods (ISO 6946, ASHRAE parallel-path, ORNL modified-zone, balance-point analysis, M&V rigor).

## Verification discipline

- 605 tests across 53 files; in the math modules, test lines outnumber source lines.
- A grid audit (19 climate packs × 3 fuels × 3 setpoints × 2 sizes) exposed negative envelope savings in 54 of 540 mild-climate scenarios. Root cause: the modified-bin cooling path lacked a free-cooling cutoff. Fixed so d(cooling)/d(UA) is strictly positive, verified zero negatives across the full grid.
- An adversarial cross-model review before merge produced 11 findings, including a missing winter-peak methodology. All 11 closed, with the closure recorded in the commit history.
- Retry counters increment before the model call, so a crash can never grant a free inspection attempt.

## Timeline

- **2026-07-20 → 07-21:** empty repository to live product in two days (29 commits), built during OpenAI's Build Week and configured for OpenAI's Freebird program.
- **2026-08-05:** national expansion, one demo county to 50 states + DC with the browser-computed program designer.
- **2026-08-08:** engine audit closing all adversarial findings, plus a full public-site redesign, in one day.

Built solo, with AI agent orchestration.

## Rights

Copyright © 2026 Omer Bese / Bonjuur, Inc. All rights reserved. These notes are published for reading. No permission is granted to copy, reuse, adapt, or redistribute any part of this repository or the product design it describes.
