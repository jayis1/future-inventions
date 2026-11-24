# Scavenge-Exhaust Catalyst Pod — Impact Analysis

**Author: jayis1.** Illustrative annual scenarios for an *eligible N₂O-only scavenging outlet*, not forecast or measured site results. Compare with supply repair and approved scavenging first; never count upstream savings again as pod benefit. See [the concept](README.md).

## Basis and assumptions

- Input is kilograms of N₂O **already collected in dedicated exhaust** per site per year, after supply repairs; it excludes uncollected gas and upstream losses. Illustrative 10/25/50 kg per site are assumptions, not prevalence data.
- Bypass/warm-up/availability leave 50%/80%/90% of collected mass actually entering the hot reactor in low/base/high cases; assumed conversion is 90% of that entering mass. These fractions are unverified and must be separately metered.
- Assumed electricity is 25 kWh per kg destroyed, including idle, warm-up and auxiliaries: the design target, **not a measurement**. Real load could be worse; the published large Swedish unit reported 30–45 kWh/kg split.[1]
- Illustrative electricity emissions factor is 0.4 kg CO₂e/kWh, **a scenario input**, not a universal or measured local grid factor. Use an audited location/time-specific factor in a real assessment. For illustration use N₂O GWP100 = 273 kg CO₂e/kg from the US EPA's presentation of IPCC AR6; reporting regimes may prescribe another factor.[2]
- No avoided emissions are attributed to treatment where a commercial destruction system would otherwise have destroyed the same gas. The table compares with a counterfactual *outdoor vent of the already collected stream*, after upstream repairs; an incumbent comparison must subtract its avoided emissions and burdens.

## Transparent calculation

`Destroyed N₂O (kg/site-year) = collected mass × fraction entering hot reactor × conversion`.
`Metered electricity (kWh/site-year) = destroyed mass × 25` (assumed target).
`Illustrative operational climate benefit (kg CO₂e/site-year) = destroyed mass × 273 − electricity × 0.4`.
This is **not net life-cycle benefit**: subtract manufacture, catalyst, shipping, replacements, disposal and any changed scavenging energy once measured. Do not count any uncollected or bypassed gas.

| Scenario | Collected kg/site-year | Hot-path fraction | Destroyed kg/site-year | Electricity kWh/site-year | Operational t CO₂e/site-year | Ten sites: kg destroyed; operational t CO₂e/year |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 10 | 0.50 | 4.5 | 112.5 | 1.1835 | 45; 11.835 |
| Base | 25 | 0.80 | 18 | 450 | 4.734 | 180; 47.34 |
| High | 50 | 0.90 | 40.5 | 1,012.5 | 10.6515 | 405; 106.515 |

Ten sites assume ten identical eligible installations over 12 months, not market adoption. Ten-site base electricity is 4,500 kWh/year; low/high are 1,125/10,125 kWh/year. Gross avoided N₂O climate mass in the base case is 4.914 t CO₂e/site-year before the 0.180 t electricity burden. Costs: a US$5,000 ex-factory target per unit plus US$600/year target service implies US$50,000 hardware and US$6,000 annual service for ten sites, **excluding** installation, permitting, electricity, equipment amortization and catalyst recycling. No payback is claimed.

## Sensitivities and decision gate

At fixed 25 kWh/kg and 0.4 kg CO₂e/kWh, electricity consumes 10 kg CO₂e per kilogram destroyed versus 273 kg avoided before life-cycle burdens. If actual electricity is 45 kWh/kg (the top of the *different* published installation's range), the modeled electricity burden becomes 18 kg CO₂e/kg; this does not validate either pod operating point.[1] Availability and capture can drive destroyed mass to zero even with a high reactor conversion. Measure actual duty-cycle electricity, capture and bypass; determine the site-specific climate-factor and grid-intensity sensitivity, full life-cycle burdens and alternative destruction baseline before procurement. Do not infer occupational health gains from exhaust conversion; separately monitor room exposure and retain approved safeguards.[3]

## Sources

[1] Ek and Tjus, “Decreased emission of nitrous oxide from delivery wards—case study in Sweden” (2008): https://link.springer.com/article/10.1007/s11027-008-9142-9
[2] US EPA, “Understanding Global Warming Potentials” (AR6 N₂O GWP100 273): https://www.epa.gov/ghgemissions/understanding-global-warming-potentials
[3] UK Health and Safety Executive, “Using nitrous oxide (gas and air) safely in maternity units”: https://www.hse.gov.uk/healthservices/using-nitrous-oxide-safely.htm
