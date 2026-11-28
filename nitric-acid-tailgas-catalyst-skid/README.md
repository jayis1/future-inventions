# Nitric-Acid Tailgas Catalyst Skid

**Author: jayis1**
**Category:** Climate & Sustainable Manufacturing / Industrial Nitrous-Oxide Abatement
**Maturity:** Research concept; not an approved plant retrofit.

## Problem

Nitrous oxide (N₂O) formed during nitric-acid manufacture is a persistent greenhouse gas and ozone-depleting emission, with low-cost industrial abatement still underused.[4] Industrial sources are a smaller share of total anthropogenic N₂O than agriculture, but existing abatement is not universally installed; the UNEP/FAO assessment identifies industrial controls as a near-term opportunity.[1] This concept is for otherwise un-abated, compatible nitric-acid production lines—not for medical anesthetic exhaust (the repository's `scavenge-exhaust-catalyst-pod`) or agricultural drainage (`electrogenic-denitrification-drainage-array`). It does not claim to solve all industrial or agricultural N₂O emissions.

## Solution

A plant-engineered, removable tail-gas skid places an iron-exchanged zeolite catalyst in the hot, post-absorber gas train, with an independently sampled inlet/outlet N₂O measurement pair, differential-pressure taps and a sealed sample-return line. Fe-exchanged zeolites have been studied for N₂O and NOₓ removal in a nitric-acid plant at 350–380 °C; catalytic conversion itself is established prior art, not this proposal's invention.[2] Intended net reaction: 2 N₂O → 2 N₂ + O₂. Each site needs a licensed pressure-vessel and process-safety design; cold or wet gas, incompatible NOₓ concentrations, or inadequate heat balance are grounds to reject installation, not reasons to extrapolate performance.

The proposed distinction is a standard replaceable, low-pressure-drop catalyst module coupled to a site-specific thermal/pressure qualification envelope and independent mass-flow-weighted abatement accounting. It aims to make maintenance and verification less dependent on a bespoke whole-train rebuild. Whether such packaging actually lowers retrofit cost or outage time relative to existing industrial abators is **unproven** and must be tested against a commercial baseline.

## Key Innovation

- **Materials and flow path:** Fe-exchanged ferrierite or beta-zeolite on an alumina-bound ceramic monolith, corrosion-compatible steel housing and gaskets selected by a plant corrosion review; two removable, keyed catalyst blocks with upstream particulate screening. No scarce noble-metal catalyst is assumed. Zeolite framework, binder, gas composition, water loading and temperature must be qualified together rather than treated as interchangeable.
- **Operating target, not a result:** At a suitable 350–400 °C tail-gas location, target ≥90% sustained N₂O mass removal over a year, added skid pressure drop ≤300 Pa at design flow and no increase above permit limits for NOₓ, ammonia slip or other measured emissions. This lower bound is a development target, not a guarantee; a field study reports >90% N₂O conversion with Fe/BEA under its own 350–380 °C conditions.[2]
- **Sanity-check mass balance:** For an illustrative 10,000 Nm³/h dry stream at 500 ppmv N₂O (normal volume at 0 °C, 1 atm), feed ≈10,000 × 0.0005 × 44 / 22.414 = 9.8 kg N₂O/h. At 90% removal and 8,760 operating hours, avoided discharge ≈77 tonnes N₂O/year, *before* downtime and measurement uncertainty; this is a scenario, not a measured plant or global projection. At 300 Pa added drop, **if actual operating flow were 10,000 m³/h** and blower efficiency were 60%, incremental shaft load ≈(10,000/3,600 m³/s) × 300 Pa / 0.60 = 1.39 kW, or ≈12 MWh/year at continuous operation. Actual hot-gas volumetric flow generally differs from the 10,000 Nm³/h used in the N₂O mass calculation; site pressure, temperature, pre-existing expander recovery and flow-control behavior can change the electrical estimate materially.
- **Safe failure:** Loss of temperature, sensor agreement, sample flow, catalyst activity or acceptable pressure drop triggers an alarm and a controlled production-rate reduction or plant shutdown under an approved operating procedure. No automatic vent bypass is represented as abatement. A plant must retain its independent NOₓ controls and log periods with invalid N₂O measurement as unverified emissions; EPA's nitric-acid guidance requires site-specific monitoring/accounting for abatement performance.[3]

## Target Cost

**Unquoted engineering target:** US$0.5–1.5 million ex-works per skid at 100 units/year by 2040 for a compatible 10,000 Nm³/h-class line. This is a design ceiling hypothesis, **not** a vendor quote or validated installed cost. It excludes site piping, pressure-vessel certification, shutdown time, heat integration, instrumentation calibration, regulatory testing, taxes and installation. Target catalyst replacement every 3–5 years only if measured activity and materials aging support it; spent media is returned to a licensed recycler or industrial-waste handler after composition testing, never dispersed. Incremental electricity is estimated above; supplemental heating could dominate the energy budget and disqualify a site.

## Impact

A single illustrative qualified line could prevent roughly 77 tonnes N₂O/year under the stated assumptions. This is not a claim about the average nitric-acid plant, and verified net benefit must subtract additional power/heating emissions and account for any production or NOₓ changes. The 10–20-year development path is bench exposure to representative wet/NOₓ gas, pilot skid on a consenting industrial site, independently calibrated inlet/outlet and stack measurements through seasonal operation, then pressure-vessel certification and site-specific permits. The core claim fails if a 12-month pilot cannot maintain ≥90% mass-weighted destruction without breaching NOₓ limits or pressure/energy constraints, or if installed cost and outage time are not competitive with existing abatement. Avoiding harm depends on trained plant operators and regulated installation—not consumer deployment. No military, surveillance or coercive use is proposed.

## Sources

[1] https://ozone.unep.org/sites/default/files/2025-04/Global%20Nitrous%20Oxide%20Assessment.pdf
[2] https://aiche.onlinelibrary.wiley.com/doi/10.1002/ep.12979
[3] https://www.epa.gov/system/files/documents/2024-04/v_nitricacid_infosheet_2024.pdf
[4] https://doi.org/10.1038/s41558-023-01723-3
