# Post-Fire Runoff Cassette — Impact Analysis

**Author: jayis1** · Scenario model, not a field result. No ecological, health or avoided-damage benefit has been measured.

## Boundary and baseline

Compare one year of permitted, accessible post-fire outfalls with the same outlets without a cassette, including a maintained settling basin as a separate field comparator. Count pollutant mass retained by this side-cell, not watershed-wide cleanup, drinking-water improvement or avoided floods. The original culvert remains the untreated bypass. The assumed concentrations below are illustrative inputs, **not measured local values or literature baselines**; field values could differ substantially. Relevant prior art is iron-enhanced-sand phosphorus filtration in other drainage contexts, not a validated post-fire analogue (see README [3]).

## Transparent assumptions

| Variable | Illustrative value | Qualification |
| --- | --- | --- |
| Event duration at rated intake | 4 h × 1 L/s = 14.4 m³ potential per unit/event | A simplifying rectangular hydrograph; storms may be shorter, larger or obstructed. |
| Mixed influent TSS | 200 mg/L = 0.2 kg/m³ | Scenario input, not an observed catchment concentration. |
| Mixed influent soluble reactive P (SRP) | 0.5 mg/L = 0.0005 kg/m³ | Scenario input; chemistry and speciation vary. |
| Treated-flow retention | 80% TSS and 50% SRP | Existing README's **unvalidated proposed gates**, not performance data. |
| Pollutant split into diversion | Equal to diverted water fraction | Artificial equal-concentration simplification; first-flush enrichment may violate it. |
| Replacement and materials | One full replacement set after each modeled event at target US$400/set; module US$5,000 | Conservative service example; targets are unquoted, ex-workshop and exclude installation, testing, freight and disposal. |

For N sites, E modeled events/site/year and treated water fraction f, treated volume = N × E × 14.4 × f m³/year. Retained TSS = volume × 0.2 kg/m³ × 0.8; retained SRP = volume × 0.0005 kg/m³ × 0.5. This assumes no remobilization or leaching and no overlap between TSS and dissolved SRP accounting; mass retention is **not** an ecological outcome. Untreated bypass volume is N × E × 14.4 × (1 − f) m³, under the same rectangular-event simplification. A blockage makes f = 0 for that period.

## One-year conditional projections

| Case | Sites × events × f | Treated volume | TSS retained | SRP retained | Modules + replacement media target |
| --- | --- | --- | --- | --- | --- |
| Low | 10 × 3 × 0.50 | 216 m³ | 34.56 kg | 0.054 kg | US$50,000 + US$12,000 |
| Base | 100 × 6 × 0.75 | 6,480 m³ | 1,036.8 kg | 1.62 kg | US$500,000 + US$240,000 |
| High | 1,000 × 10 × 0.90 | 129,600 m³ | 20,736 kg | 32.4 kg | US$5,000,000 + US$4,000,000 |

The high case is deployment arithmetic, **not a forecast**. Module purchase is a one-time cost, not an annual recurring charge; replacement sets are modeled annually and count one set per site-event, regardless of actual breakthrough. Full annualized cost additionally needs useful life, installation, crew travel, road safety, assays, cleaning, waste transport and disposal. These excluded costs could dominate. Do not divide ex-workshop spend by treated volume and call it lifecycle cost.

## Sensitivity, evidence and stop rules

At fixed volume and concentration, halving actual treated-flow retention halves modeled retained mass; halving the diverted pollutant-load fraction does the same. A bypass enriched in ash or phosphorus can make whole-event retention much worse than volume fractions suggest. If performance is zero, all modeled retention is zero despite the capital and waste costs; if media releases phosphorus or iron, net benefit can be negative. Quantify uncertainty with paired flow-weighted samples and error bounds rather than these point estimates.

Before any benefit claim, measure time-resolved upstream, treated-return and bypass flow and analytes across storm seasons; compare with controls at comparable rainfall and severity. Verify design-storm head–flow capacity during total side-cell blockage, detect first-flush breakthrough, characterize hazardous waste and report whole-event retained mass and lifecycle US$/m³. Reject scaling if crossing safety is reduced, pollutant release occurs or maintained conventional controls perform as well at lower full cost.
