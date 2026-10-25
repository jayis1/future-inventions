# Receive-Only Disaster Bulletin — Impact Analysis

**Author: jayis1** · Scenario model, not observed impact or a claim of lives saved. All costs are 2038 planning dollars from the [README](README.md), without inflation adjustment. The tile is a supplement to existing official warnings.

## Scope and model

A five-year deployment cohort of fixed public tiles. “Potential regular readers” are distinct people regularly passing a sign, not people who saw a particular alert; the model assumes no overlap across signs. For **one relevant drill bulletin**, define:

- Potential readers = installed tiles × distinct regular readers per tile.
- Estimated readers encountering a *verified* notice = potential readers × site/event reception-and-opportunity fraction.
- Estimated correct recall = estimated readers encountering notice × comprehension/recall fraction. **Recall is not evacuation, timely action or prevented harm.** Neither fraction has been field-measured.
- Upfront tile + installation cost = tiles × US$120; annualized device/installation/maintenance cost = tiles × (US$120 / 5 years + US$6/year) = tiles × US$30/year. This excludes network and authority costs.

| Input | Low | Base | High | Provenance |
| --- | ---: | ---: | ---: | --- |
| Tiles installed | 10,000 | 100,000 | 250,000 | Hypothetical deployment sizes; base matches README planning example. |
| Distinct regular readers/tile | 25 | 50 | 75 | Hypotheses; require de-duplicated site surveys. |
| Reception × opportunity for a relevant drill | 50% | 70% | 85% | Hypotheses combining RF availability and human encounter; **not** RF test results. |
| Correct recall given encounter | 40% | 60% | 75% | Hypotheses; must be tested in local languages and accessible formats. |
| Factory + installation / tile | US$85 + US$35 | same | same | Unverified volume target in README; actual prices may differ. |
| Service life / annual maintenance | 5 years / US$6 | same | same | Planning assumptions; aging and vandalism may shorten life. |

## Derived scenarios (same five-year cohort; per-bulletin reach is a single-drill estimate)

| Output | Low | Base | High |
| --- | ---: | ---: | ---: |
| Potential regular readers | 250,000 | 5,000,000 | 18,750,000 |
| Estimated encounter with verified notice, per relevant drill | 125,000 | 3,500,000 | 15,937,500 |
| Estimated correct recall, per relevant drill | 50,000 | 2,100,000 | 11,953,125 |
| Upfront purchase + installation | US$1.2m | US$12m | US$30m |
| Annualized device + upkeep | US$0.3m/year | US$3m/year | US$7.5m/year |

The base case's 5 million is **capacity only**. Even its modeled 2.1 million correct recalls are conditional on one relevant, encountered, authenticated alert; they are not 2.1 million new people reached beyond existing channels. To estimate incremental benefit, randomize comparable sites or use matched controls and subtract baseline recall/action from radio, siren, SMS and outreach. Record issue time, reception, comprehension, action and verified evacuation separately, with uncertainty intervals. Do not multiply an arbitrary hazard count by recall to claim lives saved.

## Sensitivities and exclusions

At fixed base-case tiles and readers, halving the encounter fraction halves modeled recall; doubling readers does not help if they are the same people counted at multiple entrances. A power or transmitter outage can drive local reception to zero. A sign can be read but misunderstood, and a correct remembered instruction can arrive too late. The RF and comprehension fractions are correlated with weather, disability, language and siting; treating them as independent would overstate certainty.

Excluded from the US$30/tile-year device-only figure: regional transmitters, backup power and backhaul, CAP gateway and authority staff, key custody and revocation, translations, spectrum/regulatory work, drills, taxes, vandalism, replacement before five years and independent evaluation. A site-level total-cost audit may reverse the apparent advantage. UNDRR's general early-warning benefits and coverage gap[6] motivate a test; they cannot be attributed to this tile or used as its casualty-reduction coefficient.

## Falsification gates

Stop or redesign if the signed feed cannot be operated by an authorized local issuer, stale state is misread, cold-weather autonomy fails, covered-site 60-second delivery falls below the proposed ≥95% target, false alerts rise, or controlled trials show no improvement in correct action over existing channels. Publish negative findings. Safety decisions must continue to use official warnings and local responders.

## Sources

[6] https://www.undrr.org/implementing-sendai-framework/sendai-framework-action/early-warnings-for-all
