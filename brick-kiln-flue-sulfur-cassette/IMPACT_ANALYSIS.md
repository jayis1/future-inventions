# Brick-Kiln Flue Sulfur Cassette — Impact Analysis

**Author: jayis1 · Scenario arithmetic, not a forecast or measured performance.** No brick-kiln SO₂ inlet rate or adoption fraction is established here. The local alternative is a maintained existing scrubber or cleaner fuel, not uncontrolled firing; incremental benefit must be demonstrated against that alternative.

## Boundary and equation

One 12-month operating year. For eligible sites only, avoided stack SO₂ (t/year) = eligible kilns × adoption fraction × baseline inlet SO₂ (kg per firing hour) × firing hours/year × on-stream capture fraction × fraction of firing hours actually treated ÷ 1,000. This simplified constant-rate model assumes no capture during bypass; it does **not** correct for changes in fuel, flow or emissions outside firing hours. Field estimates instead integrate paired inlet/outlet mass-flow measurements through firing and bypass, including startups and maintenance.[2]

| Illustrative scenario (all inputs assumed, not surveyed) | Low | Base | High |
|---|---:|---:|---:|
| Eligible kilns | 100 | 1,000 | 3,000 |
| Adopting fraction | 10% | 20% | 40% |
| Baseline inlet SO₂ (kg/firing h per kiln) | 0.2 | 0.4 | 0.8 |
| Firing hours/year | 1,200 | 2,000 | 3,000 |
| Treated-stream capture | 50% | 60% | 70% |
| Fraction of firing hours treated (remainder bypass/uncontrolled) | 90% | 95% | 98% |
| Avoided stack SO₂ (t/year; illustrative) | 1.08 | 91.2 | 1,975.68 |

At the base inputs, one adopting kiln would emit 0.8 t SO₂/year without this cassette and *could* capture 0.456 t/year if the assumed inlet and performance hold. Across 200 adopting kilns that is 91.2 t/year; this is **not** an additional benefit if existing controls already remove the same sulfur. The five-kiln pilot would correspond to 2.28 t/year only under the same assumptions; the real result must be measured.

## Materials and energy cross-check

Net reaction CaCO₃ + SO₂ → CaSO₃ + CO₂, with optional oxidation and hydration of the solid.[2] Molar masses approximately 100.09 g/mol CaCO₃, 64.06 g/mol SO₂ and 172.17 g/mol CaSO₄·2H₂O imply a *minimum* 1.56 t pure limestone consumed and, **only if fully oxidized/hydrated**, 2.69 t pure gypsum formed per tonne SO₂ captured. At the base 91.2 t/year scenario, theoretical minimum limestone is ~142.5 t/year; theoretical pure gypsum equivalent ~245 t/year. Real purchases and waste mass can be higher because of excess reagent, ash, dust and moisture; sulfate fraction, leaching, water purge and disposal costs require assays. No byproduct sale is assumed.

At 2,000 actual m³/h, 400 Pa *clean* pressure drop and assumed fan efficiency 60%, incremental fan shaft power is Δp × Q / η = 400 × (2,000/3,600) / 0.60 ≈ 0.37 kW, or ~0.74 MWh over 2,000 treated hours. This is an illustrative upper-clean-pressure-drop calculation, **not** installed electrical demand: dirty pressure drop, motor losses, pump power, cooling, wastewater treatment and any fan upgrade are additional unknowns. Meter them rather than translating SO₂ capture into a carbon claim.

## Measurement and decision rule

Measure SO₂ concentration on a declared dry/wet, normal-temperature/pressure and O₂-reference basis, gas mass flow, bypass duration and whole-season emitted mass for the retrofit and a matched maintained-control comparator. Independently measure CO, PM, worker CO, fuel per saleable brick, water makeup, effluent contaminants, residue mass and total service costs. Report uncertainty and missing-data hours; a treatment-only efficiency is insufficient. No avoided deaths, exposure reduction, net climate benefit, payback, legal compliance or safe residue reuse follows from this arithmetic.[1][2]

## Sources

[1] https://documents1.worldbank.org/curated/en/770271468212375012/pdf/601550ESW0P1110e00201100Color0FINAL.pdf — World Bank, *Introducing Energy-efficient Clean Technologies in the Brick Sector of Bangladesh*.
[2] https://www.epa.gov/sites/default/files/2021-05/documents/wet_and_dry_scrubbers_section_5_chapter_1_control_cost_manual_7th_edition.pdf — US EPA, *Wet and Dry Scrubbers for Acid Gas Control* (2021).
