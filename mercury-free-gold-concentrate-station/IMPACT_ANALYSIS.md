# Mercury-Free Gold Concentrate Station — Impact Analysis

**Author: jayis1. Status: scenario arithmetic, not measured benefit or adoption forecast.** Process boundary: characterized, gravity-recoverable *dry ore* accepted into the wet table, with concentrate, middlings, tailings, filter solids and any purge kept in custody. Crushing, refining, gold sale and final disposal are outside the equipment boundary but must be costed and tracked in a real pilot. Geography is deliberately unspecified; baselines must come from participating sites. All numbers below are illustrative inputs except the existing README's unverified design targets. A case is a steady **one-year** run after deployment, not a cumulative ten-year estimate.

## Functional unit and model

One station at target duty processes 25 kg dry feed/hour × 4 hours/day × 200 days/year = 20,000 kg = 20 t/year. A station uses no mercury *in its own circuit*, but avoids mercury input only for a documented batch that actually displaces a mercury-using local workflow. The model assumes eligible ore and a licensed downstream route; neither is established by installing hardware.

Let N = stations, U = realized fraction of design capacity, S = fraction of processed tonnes that verifiably replace local mercury use, H = baseline mercury introduced in that local workflow (kg/t dry ore), and D = **incremental gold returned to miners relative to that same workflow** (g/t of displaced ore). Then:

- Processed ore (t/year) = N × 20 × U; displaced ore (t/year) = processed ore × S.
- Potential avoided **mercury introduced** (kg/year) = displaced ore × H, *only if* no equivalent mercury use moves downstream. This is not avoided emissions, contamination, exposure or health burden.
- Illustrative incremental gold (kg/year) = displaced ore × D / 1,000; illustrative gross value (US$/year) = displaced ore × D × assumed US$80/g. The price is a sensitivity placeholder, not a current quote. If recovery is worse, D is negative and the model's upside disappears.
- Equipment and service allocation (US$/year) = N × (US$3,800/5 years + US$600/year) = N × US$1,360. This excludes installation, labor, sampling/assay, power, transport, financing, permits, water, downtime and safe residues. It is **not net benefit**.

## Input assumptions (not observations)

| Case | N | U | S | H (kg/t displaced) | D (g/t displaced) |
| --- | ---: | ---: | ---: | ---: | ---: |
| Conservative | 10 | 0.50 | 0.25 | 0.01 | 0.0 |
| Illustrative base | 100 | 0.75 | 0.50 | 0.03 | 0.1 |
| Stretch | 1,000 | 1.00 | 0.75 | 0.05 | 0.2 |

The H and D values are **hypothetical sensitivity inputs**, not published averages, ore-grade claims, or measured results. H must be measured as mercury introduced per dry tonne for the *specific practice actually displaced*. D must come from paired assays, documented actual gold returned and miner payment records, correcting for grade, liberation, losses and assay uncertainty. No 70% gravity-recoverable-gold target implies a positive D against the baseline; do not use this table to claim it does. Only verified mercury-using displacement enters S; setting S = 0 makes avoidance zero regardless of N.

## Derived one-year outputs

| Case | Ore processed (t) | Mercury-using ore displaced (t) | Potential Hg input avoided (kg) | Incremental gold (kg) | Gross gold value (US$) | Equipment + service allocation (US$) |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Conservative | 100 | 25 | 0.25 | 0 | 0 | 13,600 |
| Illustrative base | 1,500 | 750 | 22.5 | 0.075 | 6,000 | 136,000 |
| Stretch | 20,000 | 15,000 | 750 | 3.0 | 240,000 | 1,360,000 |

These deliberately exposed assumptions make clear that even the optimistic *gross incremental gold value* is smaller than equipment/service allocation in this model, before the excluded costs. The cooperative might value harm reduction or a different local economic outcome, but no positive payback or viable miner fee is evidenced. A lower utilization raises the equipment/service allocation per tonne processed from US$68 at U = 1 to US$136 at U = 0.5; benchmark full cost and net take-home against the real local process before expanding.

## Other flows and decision gates

At the README's **unverified ceiling** of 50 L fresh-water makeup per 100 kg dry ore (0.5 m³/t), a full-capacity station would require up to 10 m³/year of makeup; 1,000 at full duty would require up to 10,000 m³/year. This is a design ceiling, **not a measured saving** versus any local practice; initial fill, purge and contaminated sludge still need separate accounting. Record metered makeup, purge volume and quality, dry solids in every output, and legal custody to final destination. A ≥90% accounted-solids prototype gate is a test threshold, not evidence that the missing fraction is safe to discharge.

No numerical health-benefit or emission-avoidance projection is defensible from mercury input alone. Legacy mercury in feed, downstream re-amalgamation, exposure during transfer and regional differences could erase the assumed benefit. Measure workers' exposure and local environmental contamination with qualified partners, with consent and controls against false attribution. Do not extrapolate from one cooperative to a country.

**Minimum evidence for publication of impact:** a contemporaneous matched local baseline with H and ore grade; independently assayed split-feed comparisons and actual miner payments for D; documented S without displacement of harm downstream; logged throughput, uptime, full cost, water/residues and worker exposure across a season. Reject the modeled benefits if any core baseline is missing. Technology context and limitations are described in the README sources, especially planetGOLD's gravimetric-plant guide [2] and Torkaman et al. [3]; neither supplies the scenario inputs above.
