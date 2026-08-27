# Permanent demand reduction as an Industrial Compute capacity option

**Decision memo**  
**Updated 2026-08-27**

## The decision

The grid has two ways to make room for a new load. Build more capacity or remove demand that is already there.

Industrial Compute teams already compare generation, storage, transmission upgrades, and flexible load. Permanent demand reduction in nearby homes belongs on the same page. It should win only where the reduction occurs at the constrained electrical location, during the constrained hours, for long enough to matter, at a cost and delivery risk that beat the alternatives.

There is a second gate. [OpenAI describes site readiness](https://openai.com/index/building-the-compute-infrastructure-for-the-intelligence-age/) as a combination of power, land, permitting, transmission, workforce, community support, and partner readiness. The communities that host compute infrastructure are also expected to share in its upside. A household upgrade can write to both ledgers. It may reduce peak demand and it may leave a resident with a lower bill, a more comfortable home, and a physical reason to support the project.

Those are different claims. Keep them separate.

## Put every option on the same page

| Option | What it can change | Where it fails | Evidence required |
| --- | --- | --- | --- |
| New generation | Adds energy and capacity | Fuel, interconnection, permitting, construction, and delivery risk | Accredited capacity, delivered cost, schedule, emissions, and interconnection path |
| Storage | Moves energy into the constrained period | Duration ends, recharge is unavailable, or accreditation is lower than nameplate | MW, hours, recharge conditions, degradation, capacity value, and dispatch rights |
| Transmission or grid upgrades | Moves more power through the system | Rights of way, outage windows, cost allocation, or long lead times | Electrical deliverability, upgrade scope, schedule, permitting, and who pays |
| Flexible compute load | Reduces or moves the new load when the grid is stressed | The workload cannot move, the contract is weak, or dispatch is not verified | Curtailable MW, duration, notice, trigger, service-level cost, and enforceability |
| Permanent demand reduction | Removes existing demand through efficiency upgrades | Savings miss the constrained hour, participation is weak, or persistence is unverified | Hourly and locational savings, adoption, installation evidence, persistence, and measurement plan |
| Ordinary community spending | Shares value locally and may improve support | It does not change the electrical constraint | Local priorities, governance, duration, beneficiaries, and credible delivery |

The last row is important because it prevents an accounting trick. A donation can be valuable. It is not capacity. An efficiency program can create both community value and a power-system contribution, but only the verified electrical result belongs in the capacity ledger.

## The operating test

### 1. Name the actual constraint

Start with the substation, transmission zone, or utility planning area. Name the season, hour, expected event duration, and date by which capacity must be available. Annual kWh is not enough. A winter heating measure and a summer cooling measure can have the same annual savings while doing very different work for the grid.

[DOE's resource-adequacy framework](https://www.energy.gov/sites/default/files/2024-04/2024%20The%20Future%20of%20Resource%20Adequacy%20Report.pdf) makes the same point from the supply side. A resource matters when its output aligns with system stress. [Lawrence Berkeley National Laboratory](https://eta.lbl.gov/publications/valuing-residential-energy-efficiency) applies hourly residential efficiency profiles in competition with supply-side resources and finds that lighting, envelope, and space-conditioning measures line up differently with evening and winter peaks.

The constrained hour decides the portfolio.

### 2. Compare delivered capacity, not nameplates

Translate every option into capacity available at the electrical location and time that matter. Then compare cost, schedule, reliability, and execution risk.

A four-hour battery is not the same object as a persistent reduction in heating load. A flexible data-center commitment is not capacity unless somebody has the right to call it, can verify the response, and knows the service impact. A national estimate for residential efficiency is not proof that a particular neighborhood frees a particular feeder.

The unit of comparison should include location, hour, duration, confidence, and date. MW alone hides the decision.

### 3. Price the verification burden

Demand reduction is distributed across homes. That creates a different operating problem from buying one power plant.

The program needs an eligible baseline, measure rules, installation evidence, quality control, persistence assumptions, and a method for converting household results into a portfolio claim. The cost of that machinery belongs in the option price. So does the risk that participation arrives late or the measures do not perform during the constrained hour.

This is where a small pilot earns its keep. It should test conversion, contractor capacity, installation quality, evidence collection, resident experience, and the difference between modeled and measured results before the program is credited in a capacity plan.

### 4. Keep two ledgers

The capacity ledger records verified kW, timing, location, persistence, cost, and delivery risk.

The community ledger records who received value, how quickly they received it, whether the benefit lasts, and whether local institutions helped shape the program. OpenAI's infrastructure position names jobs, schools, local revenue, energy planning, water stewardship, and early engagement as forms of local upside. Household efficiency adds another mechanism. Money becomes insulation, equipment, lower consumption, and a contractor invoice that a resident can see.

Local support is not a megawatt. It is still a delivery condition.

### 5. Allocate the risk before launch

The funder, utility, contractor, resident, and program operator should know who carries each failure.

Who pays for an upgrade that fails inspection. Who owns savings risk. Who handles complaints. Who can change a measure rule. Who approves a quote. Who confirms completion. Who moves the money. Who can stop the program.

[FERC's current large-load interconnection proceeding](https://www.ferc.gov/rm26-4) asks parallel questions for data centers. It is examining whether flexible loads could move through studies faster, whether curtailment commitments are credible, and whether large loads should fund the grid upgrades required for their connection. It is an early rulemaking step, not a final rule. The direction is still useful. Flexibility and cost allocation need to become contract terms.

### 6. Use a portfolio, then preserve optionality

[DOE treats data-center demand](https://www.energy.gov/oe/clean-energy-resources-meet-data-center-electricity-demand) as a portfolio problem across generation, storage, grid infrastructure, efficiency, demand resources, planning, tariffs, and financing. [LBNL's 2026 large-load framework](https://datacenters.lbl.gov/publications/speed-power-solutions-accelerating) adds load forecasting, interconnection, procurement, markets and operations, and cost allocation.

Permanent demand reduction should enter that portfolio as an option with a gate. If it cannot show locationally relevant savings, credible delivery, and a measurement path, it stays a community program. If it can, it becomes part of the capacity stack.

## Where WattShed fits

WattShed is a working version of the program operating layer. Its national public designer lets a funder test geography, budget, measures, payment terms, and location-appropriate methodology offerings. The wider product implements evidence review, deterministic qualification and payout caps, quote approval, completion clearance, and payment-instruction records. Milam County is the case study used to demonstrate the resident workflow.

The current build does not prove a capacity resource. The nationwide designer is a simulation and the Milam case study keeps settlement simulated. WattShed has no payment processor, does not custody funds, and moves no money.

That boundary is the point of the next decision. Do not scale a claim. Scale a test.

## Recommended next step

Run a utility-reviewed pilot beside a real large-load planning process. Pick one constrained geography and one target period. Compare the residential portfolio against the marginal supply, storage, grid-upgrade, and flexible-load alternatives. Publish the assumptions before enrollment. Measure delivery against them afterward. Keep community outcomes and capacity outcomes visible on the same page without combining them.

If the household portfolio cannot produce useful capacity, the pilot will show it. If it can, the project gains a resource that the normal supply stack misses and a local benefit that ordinary infrastructure spending rarely leaves behind.

## Primary sources

- [OpenAI, Building the compute infrastructure for the Intelligence Age](https://openai.com/index/building-the-compute-infrastructure-for-the-intelligence-age/), April 2026
- [U.S. Department of Energy, The Future of Resource Adequacy](https://www.energy.gov/sites/default/files/2024-04/2024%20The%20Future%20of%20Resource%20Adequacy%20Report.pdf), April 2024
- [U.S. Department of Energy, Clean Energy Resources to Meet Data Center Electricity Demand](https://www.energy.gov/oe/clean-energy-resources-meet-data-center-electricity-demand), August 2024
- [Lawrence Berkeley National Laboratory, Speed to Power](https://datacenters.lbl.gov/publications/speed-power-solutions-accelerating), June 2026
- [Lawrence Berkeley National Laboratory, Valuing Residential Energy Efficiency](https://eta.lbl.gov/publications/valuing-residential-energy-efficiency), July 2022
- [Federal Energy Regulatory Commission, Interconnection of Large Loads, Docket RM26-4-000](https://www.ferc.gov/rm26-4), current proceeding
- [Federal Energy Regulatory Commission, Demand Response](https://www.ferc.gov/power-sales-and-markets/demand-response)
- [U.S. Department of Energy, Virtual Power Plants Projects](https://www.energy.gov/edf/virtual-power-plants-projects)

## Rights

Copyright © 2026 Omer Bese / Bonjuur, Inc. All rights reserved.
