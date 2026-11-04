# Barn Urine Ammonia Recovery Panel — Impact Analysis

**Author: jayis1**

**Status: illustrative scenario model; no panel measurements or avoided-emission results**

## Boundary and method

One eligible, already source-separated urine channel; one calendar year of 365 days. The panel acts before the existing storage route and does not capture all barn ammonia. All N quantities below are **elemental nitrogen**, not NH₃ or fertilizer mass. Published pig-slurry membrane work establishes the transfer principle but does not validate these channel-specific recovery assumptions.[1] The README's 30 g N/day pilot target assumes 100 L/day × 1 g TAN/L × 30% receiver capture on active days. Other-N forms and changes in channel inventory require a separate total-N balance.

Annual receiver N (kg) = daily urine (L) × feed TAN (g N/L) × capture fraction × availability × 365 / 1,000. This is bounded above by incoming TAN at the stated feed, and remains hypothetical. Ten-channel figures multiply one eligible unit by ten; they are **not** extrapolations to all barns. Availability includes downtime, fouling and cartridge logistics; no further uptime factor is applied.

| Case | TAN (g N/L) | Capture of incoming TAN on active days | Availability | Receiver N (kg/unit-year) | Receiver N (kg/10 unit-years) |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 0.5 | 10% | 60% | 1.095 | 10.95 |
| Base | 1.0 | 30% | 80% | 8.76 | 87.6 |
| High | 1.5 | 40% | 90% | 19.71 | 197.1 |

All cases assume 100 L/day on active days; feed TAN, recovery and availability are **scenario inputs, not observed distributions**. For perspective, the README's continuous base-design calculation (100% availability) gives 10.95 kg N/unit-year, or 109.5 kg for ten; at 80% availability it becomes 8.76 and 87.6 kg. No population adoption rate is inferred.

## Reagents, outputs and costs

Stoichiometry: 2 mol NH₃-N need 1 mol H₂SO₄ and yield 1 mol (NH₄)₂SO₄. Using molar masses 14.007, 98.079 and 132.14 g/mol, the **theoretical minimum** is 3.50 kg pure H₂SO₄-equivalent/kg receiver N and 4.72 kg dry ammonium-sulfate-equivalent/kg N. For low/base/high units respectively this implies about 3.83/30.67/69.01 kg acid-equivalent/year and at most 5.17/41.32/92.97 kg dry-salt-equivalent/year. Acid excess, residual free acid, dilution and impurities alter actual shipped mass and marketability. A 20 L, initially 1 N receiver holds at most 0.280 kg N by acid equivalents before reserve; seven-day exchange at base active-day recovery consumes about 0.210 kg of that capacity. Chemical compatibility and required pH must be tested.

The US$450 ex-workshop per-panel 2038 target is unquoted and **excludes** US$150–400/site provisional installation, cartridges, membrane replacement, acid delivery, assays, electricity, technician time and waste handling. A base-case calculation of $450 / 8.76 = **$51.37 per first-year recovered kg N** is *capital-only* and assumes a full unit paid for in one year; it is neither an operating cost nor an economic case. Determine levelized $/kg with verified lifetime, replacement schedule, installed capital and actual labor/reagent invoices. Do not transfer pig-slurry laboratory €/kg results directly to a barn-channel business case.[1]

## Emissions and decision gates

Avoided channel NH₃-N = measured time-integrated NH₃-N from matched **covered-only** controls minus that from covered-plus-panel channels, normalized to the same throughput and season. An uncovered arm measures the separate benefit of the cover. Receiver N is **not** substituted for measured emissions: some recovered N might otherwise have stayed dissolved, and changes downstream of the channel remain outside this boundary. Conversion from a measured NH₃-N saving to NH₃ mass uses 17.031/14.007; no avoided-mass estimate is defensible without a control flux. No climate, health or fertilizer-displacement credit is claimed before a consequential life-cycle study accounts for acid manufacture, pumping, transport, cleaning, material replacement, product use and possible downstream losses.

Advance only with ≥30% lower paired channel NH₃-N emissions than covered-only controls, independent total-N balance with stated uncertainty, safe drainage and worker exposure, and compliant product or disposal pathways. TAN and pH, season, membrane wetting, availability and service cost dominate uncertainty; measure these before projecting beyond the ten-channel pilot. A reduced nutrient purchase is possible only if tested material legally displaces purchased fertilizer in a documented nutrient plan; do not count the same captured N twice as both avoided emissions and avoided production.

## Source

[1] https://pmc.ncbi.nlm.nih.gov/articles/PMC9699080 — Soto-Herranz et al., *Membranes* 12 (2022), 1104; controlled pig-slurry ePTFE configurations, not source-separated urine channels.
