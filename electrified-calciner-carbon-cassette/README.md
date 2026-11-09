# Electrified Calciner Carbon Cassette

**Author: jayis1**
**Status: Concept (TRL 2)**
**Category: Climate & Sustainable Manufacturing / Cement Process Emissions**

## Problem

Heating limestone for Portland-cement clinker releases CO₂ from the mineral itself: CaCO₃ → CaO + CO₂. Replacing fossil heat with renewable electricity does not eliminate this process CO₂. At conventional plants it mixes with combustion exhaust, making separation harder. Cement demand serves billions of people; an emissions reduction must also preserve clinker chemistry, plant safety and affordable construction.

## Solution

A proposed **replaceable calciner-and-carbon-accounting cassette** for a *site-qualified preheater/precalciner cement line*. Metered raw meal passes through sealed, refractory-lined indirect-heating channels; electric resistance elements heat the outside of the channel without mixing air or combustion gas with the released process CO₂. A sealed outlet sends the CO₂-rich stream through a serviceable dust filter and dryer to a separately powered compressor and a permitted transport/storage connection. Calcined meal is metered back into the existing rotary-kiln feed, where clinker formation still occurs. Kiln combustion emissions are **not** captured by this cassette.

The distinctive proposed integration is a **swappable hot-face liner plus independently reconciled solids, electricity and CO₂ boundary**: damaged channels can be isolated and replaced during a planned stop, while a locally readable balance flags gas leakage or uncollected CO₂ rather than treating a concentrated outlet as proof of abatement. Indirect calcination and electrification are existing approaches, including Leilac's modular direct-separation technology [1]; this is a testable maintenance and verification configuration, **not** a claim to invent indirect calcination or to have demonstrated net-zero cement.

## Key Innovation

- **Mechanism and materials:** FeCrAl resistance elements outside replaceable high-alumina refractory hot-face liners; temperature-qualified steel shell on the cooled side, ceramic fiber only where contained against fiber release, and gasketed high-temperature mineral seals. Actual alloy/liner lifetime at local meal chemistry and temperature is unproven; hot-side metal must not be assumed to survive calciner conditions.
- **Separate capture boundary:** pressure-monitored meal feed/discharge locks, dust-resistant gas taps, replaceable ceramic particulate elements, condensation/drying, flow and CO₂-composition measurement, and compression metering. Process-gas inventory must include filter purge, bypass, leaks, startup and shutdown; no vented CO₂ is credited as captured. Dust is returned to the meal only after quality checks.
- **Design targets, not measured performance:** ≥90% collection of the *calcination CO₂ entering the qualified retrofit boundary* over a full operating cycle, and clinker meeting the same plant's chemical and strength specifications as its matched baseline. Capture fraction is collected CO₂ mass divided by inferred process CO₂ from measured carbonate input and residual carbonate in solids, cross-checked against the measured gas outlet. Report uncertainty and all exclusions.
- **Energy sanity check:** CaCO₃ decomposition is endothermic (roughly 178 kJ per mole of pure CaCO₃); this is a reaction-heat lower bound, not the required electrical input. Feed heating, losses, air ingress, kiln integration and CO₂ compression add energy; measure the total kWh per tonne of saleable clinker and compare with an otherwise comparable baseline. A carbon-intense grid can erase or reverse the benefit. No claim that the kiln's remaining fuel emissions vanish.

## Target Cost

**Unquoted engineering target in 2026 US dollars:** installed retrofit and capture equipment below US$150 per tonne/year of *qualified clinker capacity* at repeat deployment of ten plants by 2040, excluding transport/storage infrastructure, plant shutdown losses and grid upgrades. For illustration only, a 1 million tonne/year eligible line would therefore have a ceiling of US$150 million, not a supplier quote. Operating expenditure is **not yet estimated**: it depends on metered electricity price and kWh/t, liner/filter replacement, labor, CO₂ compression and independently contracted durable storage. Publish an itemized site estimate and uncertainty range before procurement; do not call captured CO₂ avoided until its fate and lifecycle emissions are verified. Sites without affordable low-carbon electricity and permitted durable storage are not candidates.

## Impact

A successful 10–20-year deployment could avoid part of the process-emissions burden of eligible existing cement lines while preserving material quality. The measurable benefit is **net lifecycle tonnes CO₂e avoided per tonne of saleable clinker** versus an independently measured baseline, including electricity, residual kiln fuel, compressor energy, material replacement, transport, storage losses and construction. Use only verified durable mineralization or geological storage; short-lived CO₂ utilization is not automatically permanent removal. No population-scale or global abatement total is claimed from an untested retrofit. Accessibility means publishing open measurement protocols, training local maintenance crews and assessing whether the added cost excludes lower-income builders; reduce clinker demand and use qualified low-clinker cements where possible instead of treating capture as a substitute.

## Validation and failure modes

1. Bench-test a representative meal and liner for conversion, deposit formation, seal leakage and thermal cycling against a conventional calciner control. Independently assay raw meal, discharge carbonate and recovered CO₂; stop if dust clogs the outlet or mass-balance uncertainty prevents a credible ≥90% collection test.
2. Pilot a bypassable slipstream under a qualified cement engineer's safety case. Compare electricity, throughput, clinker chemistry and strength, CO₂ purity, capture fraction, liner wear and downtime across ordinary and off-design meal compositions and startup/shutdown. Reconcile a third-party lifecycle inventory before any avoided-emissions claim.
3. On loss of power, failed feed lock, gas overpressure, blocked filter or failed compressor, isolate electric heat and solids feed, use a pressure-rated emergency route governed by plant permits, and record any venting as emissions. Do not route hot dusty gas into occupied spaces or promise safe continued operation. Existing kiln and hot-gas safety interlocks remain authoritative; qualified engineers must assess explosion/CO hazards from site-specific fuels and purge gases.
4. Replace worn elements, gaskets and refractory under lockout during cooldown; contain dust and spent ceramic fibers for regulated disposal or qualified recycling. If repairs, extra electricity or storage losses outweigh measured reductions, abandon the retrofit at that site.

## How It Works

A weighed, preheated raw-meal slipstream enters the isolated channel through a gas-tight solids lock. Resistance heaters transfer energy through a replaceable refractory hot face; carbonate decomposes into lime and CO₂ without exposing the process stream to combustion air. For an illustrative 1.00 t of clinker with 0.65 t of CaO derived entirely from limestone, the IPCC balance requires about 1.16 t CaCO₃ and releases about 0.51 t CO₂ before its separate kiln-dust correction; the actual feed also contains silica, alumina and iron-bearing minerals and must be assayed, not assumed.[2] The heated meal returns to the host kiln for clinker formation. The cassette is **not** a container for stored CO₂: it is the removable liner/heater/seal and instrumented process boundary. Its filtered CO₂ stream is dried, compressed and handed to a separately permitted durable-storage operator; custody meters and storage records close the chain. A failed seal or bypass is an emission, not captured carbon.

## Technical Architecture

**Material path:** preheater diversion → weighed feed lock → parallel indirectly heated channels → discharge lock → original kiln feed; entrained dust passes a serviceable ceramic filter and returns only if chemistry permits. **Gas path:** each channel's pressure tap → common insulated manifold → filter → water knock-out/dryer → composition and flow meters → compressor → custody-transfer meter and storage interface. **Power and data path:** protected electrical supply → zoned FeCrAl heaters and independently metered auxiliaries; temperature, pressure, differential-pressure and flow signals drive a safety PLC with hardwired heater/feed trips and a historian that reconciles inlet carbonate, outlet residual carbonate, dry CO₂ and all vent/bypass events. The host plant retains kiln interlocks; a pressure-rated permitted relief path cannot be replaced by software. Removable cassettes are cooled and isolated before replacement; **no CO₂ sorbent is claimed or regenerated**. Heat-transfer area, refractory thickness and channel residence time remain site-specific design problems.

## Performance Benchmarks

These are **proposed qualification targets, not measured prototype results**. A conventional direct-fired preheater/precalciner is the matched comparator; Leilac has already demonstrated indirect separation at pilot scale, so the proposed differentiator is maintainability plus auditable end-to-end carbon accounting, not a new capture chemistry.[1][3]

| Metric and boundary | Comparator / physical anchor | Proposed acceptance gate |
| --- | --- | --- |
| Carbonate process CO₂ per t saleable clinker | IPCC Tier-1 default **0.52 t CO₂/t clinker** including kiln-dust allowance; replace with site assays.[2] | Account for carbonate in all feeds and unreturned dust; report measured, uncertain baseline. |
| Capture of process CO₂ inside qualified cassette boundary, **full cycle** | Conventional uncaptured calciner: 0 t routed to storage; indirect separation itself is demonstrated by Leilac, not novel.[1][3] | ≥90% of CO₂ generated in cassette channels reaches custody meter; include startup, purge, leaks and downtime. This is **not** 90% of whole-plant emissions. |
| Energy per t saleable clinker | CaCO₃ reaction enthalpy ≈178 kJ/mol in original concept: ≈573 kWh/t clinker for 1.16 t CaCO₃, a reaction-only lower bound; recovered preheat and fuel displacement change the *incremental* electrical balance. | Illustrative **700 kWh/t clinker additional electricity** including compression; measure separately from displaced calciner fuel and reject if heat/mass balance or plant output fails. Not a promise of superior energy efficiency. |
| Product and reliability | Same line's pre-retrofit clinker chemistry/strength and operating schedule | Matched product qualification; ≥8,000 operating hours per year is an aspirational availability gate, contingent on liner wear, dust and seals. |

The 700 kWh/t assumption and ≥90% gate must be jointly tested at representative throughput; neither is a supplier guarantee. At 1 Mt/year saleable clinker the illustrative electric demand is 700 GWh/year, requiring grid and transformer studies; 0.52 × 0.8 eligible process fraction × 0.9 collection ≈0.374 t CO₂/t clinker before transport or storage losses (see [impact analysis](./IMPACT_ANALYSIS.md)).

## Deployment Scenarios

1. **Existing dry-process plant:** a cement operator diverts a bypassable fraction of preheated meal to a cassette bank, retains the kiln and checks clinker specification while a grid operator qualifies a new electrical connection. Storage contracts and a CO₂ pipeline or permitted truck/ship route precede commissioning.
2. **Industrial CO₂ hub:** several nearby lines share compression/export infrastructure but retain separate inlet, outlet and custody meters so each owner can audit its emissions. Planned outages exchange cooled liners; a hub outage diverts or stops the cassette, never silently vents credited CO₂.
3. **New-build low-carbon kiln line:** the process engineer sizes indirect channels, grid connection and heat recovery alongside the preheater from the start; a third party verifies storage and full-plant lifecycle performance. Where low-carbon power or storage is absent, use lower-clinker cement and other abatement rather than install a stranded cassette.

## Risks & Mitigations

- **Heat transfer and variable feed:** wet/coarse/high-alkali meal can reduce conversion or foul channels; assay each feed lot, test residence-time and thermal gradients at pilot scale, and bypass off-spec material.
- **Thermal cycling and dust:** liners, seals and filters can crack or plug; perform repeated hot/cold cycles and differential-pressure tests, hold replacement inventory, and require cooldown/lockout with dust containment.
- **Gas leakage, pressure and CO₂ exposure:** monitor channel pressure and indoor CO₂; trip feed/heaters on leakage or blocked outlet, route pressure relief only to a permitted safe location, and count relief as emitted.
- **Carbon-accounting and grid risk:** air ingress, compressor outages, fossil-heavy power or non-permanent CO₂ use can nullify benefits; independently reconcile meter uncertainty and storage custody, publish both gross collected and net lifecycle avoided CO₂e, and decline sites with negative net balance.
- **Cost and plant disruption:** the unquoted capital target excludes power upgrades and storage; require a plant-specific engineering estimate and a bypassable pilot before committing to a shutdown.

## Vision for 2050

In a plausible, **conditional** 2050 scenario, qualified cement corridors use modular calciner retrofits, low-carbon electricity and independently verified CO₂ storage while specifying less clinker wherever structural standards permit. An operator can replace a worn hot-face unit during a planned outage and hand an auditor reconciled feed, electricity, vent and storage records. The result is not zero-emissions cement by decree: remaining kiln fuel, construction, transport and storage losses stay on the ledger, and a retrofit is retired wherever its measured net benefit disappears.

## Source and prior art

[1] https://www.leilac.com/technology/ — Leilac's indirectly heated, modular direct-separation calciner (existing art; described as electrification-ready). This concept has not been built or independently validated.

## Sources

[1] https://www.leilac.com/technology
[2] https://www.ipcc-nggip.iges.or.jp/public/2006gl/pdf/3_Volume3/V3_2_Ch2_Mineral_Industry.pdf
[3] https://www.leilac.com/project-leilac-1
