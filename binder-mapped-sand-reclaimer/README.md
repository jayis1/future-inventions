# Binder-Mapped Sand Reclaimer

**Author: jayis1**

**Status: Research concept (TRL 2)**
**Category: Sustainable materials / foundry sand circularity**

## Problem

Foundries discard or downcycle spent casting sand when residual binders, fines and metal fragments make it unsuitable for another mould. Mining replacement sand and moving both streams burden ecosystems and local communities. Sand and gravel extraction is a large global environmental pressure [1]; that global figure is **not** a measure of foundry-sand demand. Existing mechanical and thermal reclamation already work, but the latter can consume substantially more energy, while aggressive abrasion destroys reusable grains [2].

## Solution

A shared, container-sized reclaimer accepts **segregated silica sand with identified organic binders** from small foundries. A screened hopper and magnet remove lumps and ferrous fragments. A low-abrasion attrition stage removes loose binder; a weighed, representative sample is tested for loss-on-ignition and grain-size distribution. Only lots failing the foundry's specified reuse criteria enter an electrically heated, insulated moving bed. The operator selects a laboratory-qualified temperature/time recipe for the documented binder family; the unit does not infer chemical safety from color or temperature. An enclosed oxidizing exhaust treatment train, particulate filter and monitored stack handle volatilized organics. Counterflow clean-air heat exchange preheats incoming air from hot **clean-side** product sand without mixing dusty exhaust into the feed. The cooled sand is classified and sampled for grain size, residual binder and casting performance before reuse.

Material balance at an illustrative 1,000 kg/h feed: a **design goal**, not measured performance, is at least 900 kg/h qualified reclaimed grains, with up to 100 kg/h of screened metals, fines and rejected material accounted for by scale; actual fractions depend on the feed. Rejected solids and filter dust require characterization and permitted disposal or recovery, not dispersal. No treated sand is automatically declared safe for unrestricted construction or soil use.

## Key Innovation

The proposed advance is **binder-specific, test-gated treatment**: primary attrition first, thermal processing only for qualified binder/lot combinations that need it, and repeat testing of the output. Heat recovery and exhaust treatment are designed and metered as parts of the same material-and-energy boundary. Thermal reclamation itself, mechanical attrition and afterburning are established art [2]; the unproven question is whether this integrated small-foundry workflow reduces *whole-system* fresh-sand demand and cost without shifting harm to electricity, air emissions or hazardous residues.

For an eligible silica/organic-binder feed, proposed pilot acceptance targets are: ≥90% of input mass returned as **foundry-qualified sand**; ≤180 kWh of purchased electricity per metric tonne of input including fans, heating and exhaust controls; and no more than 10% of operating hours lost to planned cleaning over a 500-hour pilot. The cited comparator study uses approximately 242 kWh/t for one thermal process and 11 kWh/t for one mechanical process [2]; these are study-specific examples, not universal baselines. Compare each pilot lot with a maintained conventional reclaimer on the *same feed*, using calibrated meters, scales, laboratory binder/particle tests and foundry casting rejects. Publish the measured emissions and material fate alongside energy use; failing a quality or exhaust limit diverts the lot from reuse and stops the heater.

**Failure and safety boundary:** Unknown binders, chromite or mixed mineral sand, coatings, heavy metals and fluorinated residues are excluded until independently characterized; heating them could create toxic emissions. A fan or oxidizer fault interlocks feed and heat and routes exhaust to a safe shutdown, never an unfiltered bypass. Bag-filter differential pressure and stack temperature/oxygen are logged locally for operators, not worker surveillance. Burn and combustible-dust hazards require guarded hot surfaces, explosion-risk assessment, local permits and independent emissions testing before operation. There is no deployment claim yet.

## Target Cost

**Unquoted engineering goal:** US$250,000 ex-works for a nominal 1 tonne/hour module at 10 units/year by 2038, including the enclosed heater, classifier, heat exchanger, filter and interlocks. Installation, power connection, site-specific emissions control, laboratory testing, transport, maintenance and residue disposal are **additional**. At a hypothetical 2,000 operating hours/year, capital alone is US$12.50/t on straight-line ten-year allocation (US$250,000 ÷ 20,000 t); financing, energy and labor are not included. At US$0.12/kWh, the ≤180 kWh/t electricity goal implies **up to US$21.60/t** before demand charges; neither figure is an observed price. Shared ownership must beat local delivered fresh-sand plus disposal costs on a full lifecycle basis, otherwise use conventional reclamation.

## Impact

A ten-unit pilot running 2,000 hours/year at 1 t/h and meeting the 90% reuse goal would provide up to **18,000 t/year of qualified reused sand**, not 18,000 t of proven avoided extraction: displacement depends on actual substitution, transport and rejects. Evaluate avoided virgin-sand purchases and landfill shipments with invoices, and net CO₂e with the actual grid mix and transport routes. No population or climate benefit is asserted before that comparison. Development path: 2027–2030 binder and emissions characterization; 2031–2035 independently monitored 500-hour pilot; 2036–2040 multi-foundry replication and permitting where measured benefit is positive.

## How It Works

The “map” is a **lot-level process record**, not an unproven real-time chemical scanner: the foundry declares the silica sand and organic binder formulation, and the operator attaches a traceable sample ID, feed mass, moisture, loss-on-ignition (LOI), sieve distribution and laboratory binder characterization. A recipe is enabled only for that documented binder family. Unknown or mixed feed is quarantined for analysis, not assigned a guessed thermal setting.

A metered hopper feeds screening, magnetic separation and gentle mechanical attrition. A representative post-attrition sample is compared with the receiving foundry's pre-agreed limits; qualifying material can bypass heating. Otherwise an eligible lot enters the enclosed electric moving bed on a laboratory-qualified temperature/residence-time recipe. Insulated heat exchange recovers sensible heat from clean-side product while keeping contaminated exhaust separate. After cooling, classification removes fines; a final composite sample must pass LOI, sieve and trial-casting tests before release. Product and each residual stream are weighed to close the mass balance. Treatment does not repair cracked grains or make an excluded binder safe.

## Technical Architecture

**Material path:** identified lots → screened/metal-removed feed → attrition → sampled bypass or thermal bed → cooling/heat recovery → classifier → quarantined product bin → laboratory release. Separate sealed bins hold scrap, fines and filter dust for characterization. **Control path:** lot record and lab results select an approved recipe; scales, thermocouples, power meters, fan status, filter pressure drop and stack oxygen/temperature write a time-stamped batch record. The controller cannot authorize product reuse by itself: the foundry's independent acceptance test is the release gate. Calibrations and chain of custody must be documented at pilot scale.

The heater and oxidizer use a permissive interlock: loss of draft, failed exhaust treatment, overtemperature or an out-of-limit stack reading halts feed and heat, isolates the lot and initiates a controlled shutdown under the site's engineered safety case. A contained local exhaust path, dust-rated filtration and occupational silica monitoring are essential; the exact air-pollution-control design and permit limits depend on binder chemistry and jurisdiction. Power and emissions reporting include fans and abatement, not just the hot bed.

## Performance Benchmarks

All project figures below are **proposed pilot gates, not measured results**. A same-feed comparison is required because binder, grain size, moisture and product acceptance criteria change the answer.

| Metric and boundary | Proposed gate | Published context / validation |
| --- | --- | --- |
| Nominal eligible feed throughput | 1 metric tonne/hour while running | Design capacity; weigh inlet and record uptime during a 500-hour pilot. |
| Foundry-qualified output / inlet mass | ≥90% for eligible silica/organic-binder lots | Unverified target; weigh *accepted* output, not all recovered solids; trial castings and lab tests determine acceptance. |
| Purchased electricity / inlet mass, full module and exhaust controls | ≤180 kWh/t | One study's equipment-specific examples are ~11 kWh/t mechanical and ~242 kWh/t thermal [2]. They are **not** equivalent quality or feed baselines; meter both alternatives on identical lots and record thermal-bypass share. |
| Planned cleaning downtime / scheduled pilot hours | ≤10% over 500 scheduled hours | Design goal; log start/stop causes. Unplanned stoppages reported separately, not hidden in this metric. |
| Product and emissions quality | Foundry-set LOI, sieve and trial-casting limits; permit-set stack limits | No universal threshold asserted. Establish numerical site-specific limits *before* a pilot, then independently sample every lot and test the stack. |

Record consumables (filter replacements), captured dust, metals, rejected sand and any wastewater per tonne. A thermal route is not “better” merely because it beats the cited thermal energy example: it must meet equal casting quality and show a favorable full-system material, cost and emissions balance.

## Deployment Scenarios

1. **Shared small-foundry service:** nearby foundries segregate and label compatible organic-binder silica lots; a permitted hub returns tested sand to its originating foundry. Rejected or unknown lots stay segregated, and transport is included in the business case.
2. **On-site closed-loop line:** a foundry with one stable binder recipe places the module between shakeout and mould preparation, with an independent lab sampling point and quarantine bin. Operators can bypass heating only after the attrition sample passes the local reuse specification.
3. **Regional pilot consortium:** several foundries compare matched lots with an existing mechanical/thermal reclaimer and jointly fund independent air monitoring and casting-reject audits. This is a research deployment, not a claim of commercial readiness.

## Risks & Mitigations

- **Binder error or contaminated feed:** paperwork and samples can disagree. Require supplier declaration plus periodic laboratory confirmation; lock out unknown, mixed-mineral, metal-contaminated or previously unqualified binder lots.
- **Weak sand or excess fines:** abrasion and heat may damage grain surfaces. Compare sieve distribution, LOI and casting defects with virgin and conventionally reclaimed controls; quarantine failed output rather than blending it away.
- **Silica exposure, dust/fire and hot equipment:** enclose transfers, use local exhaust and appropriate filtration, monitor respirable crystalline silica, guard moving/hot parts and evaluate combustible-dust hazards before commissioning. Stop on ventilation or filter failure.
- **Off-gas and secondary waste:** binder decomposition can generate hazardous compounds; test recipe-specific exhaust, independently measure emissions, and characterize dust and rejected solids for permitted disposal. Never bypass abatement to maintain throughput.
- **Economics and carbon rebound:** drying, abatement, testing, transport and grid electricity may erase savings. Meter the complete boundary, price residues and compare matched-site alternatives before scaling.

## Vision for 2050

**Scenario, not forecast:** if binder traceability, clean energy and independently verified quality become routine, a foundry could treat spent sand as a graded local feedstock rather than a default waste. Shared hubs might exchange *tested* sand under material passports while casting rejects, dust exposure and stack emissions remain visible on every batch. Where those gates cannot be met, conventional treatment or safe disposal remains the right choice; circularity is earned by measurement, not a label.

## Sources

[1] UNEP, *Sand and Sustainability: 10 Strategic Recommendations to Avert a Crisis* (2022), https://unepgrid.ch/storage/app/media/Publications/2022sandandsustainabilityreportfinal.pdf .

[2] *Economic and Environmental Aspects of Applying the Regeneration of Spent Moulding Sand*, Sustainability 16(19), 8462 (2024), https://doi.org/10.3390/su16198462 . Its comparison is feed- and equipment-specific; the figures above are not performance guarantees.
