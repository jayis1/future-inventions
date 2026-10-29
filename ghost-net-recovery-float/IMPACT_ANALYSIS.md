# Ghost-Net Recovery Float — Impact Analysis

**Author: jayis1. Status: scenario arithmetic, not field measurements or a forecast.** This is a visual backup marker for fixed nets at ≤20 m; it neither lifts nets nor locates them remotely. Sources [1] and [2] explain marking/recovery context but do not validate the scenario rates below. Compare with standard legally marked nets, not with doing nothing.

## Unit and assumptions

One hypothetical cooperative fits **10,000 eligible nets** with one reusable module each for one year. A lost-net incident means a net cannot be recovered on its intended haul; a net counts as recovered only when the **whole net** reaches port. Rates are deliberately illustrative and require a paired field study. Net mass is weighed at port after documenting water and fouling; this simplified model treats assumed mass as the mass of recovered gear, not avoided new ocean input.

| Variable | Low | Base | High | Provenance |
| --- | ---: | ---: | ---: | --- |
| Fitted nets | 10,000 | 10,000 | 10,000 | Illustrative fleet assumption |
| Annual lost-net incident fraction | 1% | 3% | 5% | Scenario assumption, not a global loss estimate |
| Baseline fraction of incidents fully recovered with legal marks | 20% | 20% | 20% | Scenario assumption; must be measured locally |
| Fraction fully recovered with backup module, *including failures to surface, sight or retrieve* | 30% | 50% | 70% | Hypothetical outcome, not a module performance claim |
| Recovered net mass | 10 kg | 20 kg | 30 kg | Scenario assumption; actual wet/dry mass varies |
| Unit purchase / service life / annual service | US$45 / 5 yr / US$10 | Same | Same | Unvalidated README target; excludes inflation, finance and failures |

## Derived annual outcomes

Equations: incidents = fitted nets × incident fraction; baseline nets = incidents × baseline recovery fraction; tagged nets = incidents × tagged recovery fraction; **additional nets** = tagged − baseline; **additional mass** = additional nets × kg per net ÷ 1,000. These are incremental to conventional marking, so the baseline recovery is not credited twice.

| Outcome | Low | Base | High |
| --- | ---: | ---: | ---: |
| Lost-net incidents | 100 | 300 | 500 |
| Fully recovered with standard legal marking | 20 | 60 | 100 |
| Fully recovered with module (not merely sighted) | 30 | 150 | 350 |
| Additional complete nets recovered | 10 | 90 | 250 |
| Additional gear mass landed | 0.1 t | 1.8 t | 7.5 t |
| Annualized module purchase + service: 10,000 × (US$45/5 + US$10) | US$190,000 | US$190,000 | US$190,000 |
| Module-only cost per extra complete net | US$19,000 | ~US$2,111 | US$760 |
| Module-only cost per additional tonne | US$1,900,000/t | ~US$105,556/t | ~US$25,333/t |

These **module-only** costs omit installation, vessel/search time, permits, replacement, disposal and opportunity cost; real full costs are higher. A positive mass estimate does not prove economic or ecological value, especially at low incident rates. A 100-net paired pilot from the README is a feasibility study, not evidence sufficient to extrapolate these rates to 10,000 nets.

## Failure, lifecycle and decision boundary

A timed release is not evidence of a lost net. Pilot logs must separately count releases, surfaced markers, sightings, correctly identified nets, full retrievals, false alarms, missing floats and gear left on the seabed. Every module has an owner/serial, pre-set inspection and return or documented loss. If a module becomes litter, its polymer/metal mass and any device-caused wildlife harm must be charged against the benefit; neither is estimated here. Recovered net mass must be logged by waste disposition (reuse, recycling or controlled disposal), not automatically called recycled plastic.

Sensitivity is dominated by incident frequency and **incremental** retrieval fraction, not by the release-timer pass rate alone: if module-equipped nets recover no more often than ordinary marked nets, additional nets and mass are zero and cost per additional tonne is undefined. Measure crew and vessel fuel/hours, failed searches and module recovery rate before claiming a net benefit. No defensible conversion from mass landed to animals saved, ghost-fishing mortality avoided or CO₂e avoided is available from this model.

## Sources

[1] FAO, *Voluntary Guidelines on the Marking of Fishing Gear* and risk-assessment background: https://openknowledge.fao.org/server/api/core/bitstreams/8e458922-9ebd-40c1-9e3d-6ced70700768/content — context on gear marking and recovery; no assumed scenario rate is attributed to it.

[2] IOTC, *Operationalisation of FAO Voluntary Guidelines for the Marking of Fishing Gears*, §3.2.4: https://iotc.org/sites/default/files/documents/2022/02/IOTC-2022-WPICMM05-13_Add1_-_Scheme_to_operationalise_FAO_VGMFG.pdf — alternative locating approaches, not evidence of this module's performance.
