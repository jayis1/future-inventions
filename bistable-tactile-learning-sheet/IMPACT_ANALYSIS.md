# Impact Analysis — Bistable Tactile Learning Sheet

**Author:** jayis1

**Status:** Illustrative scenario model. No integrated BTLS impact has been measured; every result below depends on stated assumptions and must be replaced with pilot data.

## Scope and Baseline

The model covers operation at steady-state deployment, not a forecast of demand. The baseline is a mix of embossed tactile pages, one-line refreshable Braille displays, audio, and staff-mediated graphics. BTLS supplements that mix; it does not assume every learner with vision impairment needs or prefers a tactile sheet.

External context is limited to the WHO estimate that at least 2.2 billion people have near or distance vision impairment.[1] This is not the addressable market. Adoption scenarios below are explicit program choices rather than percentages of that population.

## Modeling Assumptions

| Input | Modeled value | Basis and uncertainty |
|---|---:|---|
| Delivered device price | US$325 | Midpoint of the US$250–400 design target; early units will cost more. |
| Service life | 8 years | Below the 10-year design target to allow field attrition. |
| Cassette price / interval | US$27.50 / 4 years | Midpoints of the US$20–35 and 3–5 year targets. |
| Other annual operating/service cost | US$10 per device | Design ceiling; excludes optional content services and staff time. |
| Typical use | 150 updates/day, 200 days/year | Classroom duty-cycle target. |
| Energy per update | 15 J | Midpoint of the 10–20 J engineering target. |
| Awake electronics | 0.1 W for 8 h/day, 200 days/year | Conservative use of the latched-page ceiling. |
| Electricity per device-year | 0.3 kWh | 0.125 kWh updates + 0.160 kWh awake, rounded upward. |
| Avoided embossed sheet mass | 10 g/page | Illustrative thick-paper assumption; procurement data must replace it. |
| Learners sharing each sheet | 4 / 3 / 2.5 | Conservative / base / ambitious utilization assumptions. |
| Avoided printed pages per device-year | 1,000 / 2,000 / 3,000 | Scenario assumptions, not measured substitution. |

The model excludes unmeasured learning gains, caregiver time, shipping, educator authoring time, and carbon credits. Those may be material but are not assigned a monetary value without pilot evidence.

## Steady-State Scenarios

| Scenario | Deployed sheets | Learners served | Avoided embossed pages/year | Avoided paper mass/year | Device electricity/year |
|---|---:|---:|---:|---:|---:|
| Conservative | 100,000 | 400,000 | 100 million | 1,000 tonnes | 30 MWh |
| Base | 1 million | 3 million | 2 billion | 20,000 tonnes | 300 MWh |
| Ambitious | 5 million | 12.5 million | 15 billion | 150,000 tonnes | 1,500 MWh |

Formulas:

- learners served = deployed sheets × learners sharing each sheet;
- avoided paper mass = sheets × avoided pages × 0.010 kg;
- update electricity = 15 J × 150 × 200 ÷ 3.6 million J/kWh = 0.125 kWh/device-year;
- awake electricity = 0.1 kW ÷ 1,000 × 8 h × 200 = 0.160 kWh/device-year;
- rounded device electricity = 0.3 kWh/year.

Avoided pages represent production capacity displaced, not guaranteed net savings. Schools may retain embossed masters, consumables, and alternative formats for resilience and user choice.

## Cost per Learner-Year

Annualized device cost is modeled as:

US$325 ÷ 8 years + US$27.50 ÷ 4 years + US$10 = **US$57.50 per device-year**.

That equals approximately **US$14.38**, **US$19.17**, and **US$23.00 per learner-year** at 4, 3, and 2.5 learners per sheet, respectively. These figures exclude training, content conversion, charging infrastructure, taxes, financing, and program administration; a pilot must compare the full cost with actual embossing and line-display budgets.

## Manufacturing and End of Life

Operational energy is small, but manufacturing may dominate lifecycle impact. Until a bill of materials and supplier-specific lifecycle assessment exist, the model uses no invented carbon total. Reporting must separately measure the silicone/TPU cassette, PET and printed conductors, recycled-polycarbonate fluidics, ABS/PC enclosure, electronics, pump, and 60 Wh LiFePO4 battery.

At one cassette replacement every four years, steady-state annual cassette demand is approximately 25,000, 250,000, or 1.25 million modules across the three scenarios. Procurement must report module mass, recovery rate, actual recycled yield, and disposal route. “Replaceable” reduces whole-device waste only if spares, repair labor, and take-back remain available.

## Social and Educational Outcomes

The defensible near-term outcome is access capacity: one reusable surface can present changing Braille and spatial content offline. Learning benefit remains a hypothesis. Pilots should preregister and report Braille accuracy, diagram comprehension, task time, fatigue, attendance, device uptime, content-authoring time, and repair time against validated embossed and line-display controls.

Privacy impact is bounded by design: no account, camera, microphone, mandatory radio, advertising identifier, or required telemetry. Audits must still test document parsers, verified boot, retention controls, removable storage handling, and administrator practices.

## Sensitivity and Breakpoints

- **Service life:** reducing life from 8 to 4 years raises annualized hardware cost from US$40.63 to US$81.25 per device before service and cassettes; durability is the largest direct cost lever.
- **Sharing:** moving from four to one learner per sheet raises modeled cost from US$14.38 to US$57.50 per learner-year.
- **Cassette interval:** replacement every 2 instead of 4 years adds US$6.88 per device-year at the modeled midpoint price.
- **Paper substitution:** halving avoided pages halves the paper-mass result; no learning result changes automatically.
- **Electricity mix:** device use is only about 0.3 kWh/year, so manufacturing, logistics, and module replacement likely dominate climate impact; this must be verified by lifecycle assessment.
- **Yield and defects:** if sheet yield prevents the US$325 delivered midpoint or field defects exceed the <0.1% post-retry pixel target, smaller tiled products may produce better access per dollar.

## Decision Gates

Scale is justified only if pilots show readable pages, safe thermal behavior, repairable faults, competitive five-year cost, and user preference in at least some workflows. Claims about paper, learning, carbon, or equity must be reported as measured ranges with study design and attrition—not promoted from these scenarios into facts.

## Source

[1] https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment — WHO: Blindness and vision impairment
