# Continuous-Load-Path Roof Tie — Impact Analysis

**Author: jayis1** · Conditional planning exercise, not a measured forecast. No storm-loss or life-safety benefit has been established. The 3 kN laboratory gate and witness tolerances in [README.md](README.md) are design targets, not as-installed ratings.

## Baseline and assumptions

- Cohort: 100 one-story timber-framed dwellings screened for a sound concrete foundation and an engineer-designed complete load path; this is a hypothetical cohort, not a market-size estimate.
- Baseline: conventional engineered, code-compliant roof-to-wall, wall and foundation strengthening with an equivalent site survey and inspection. Its installed cost and storm-loss rate must be measured locally; neither is assigned a fabricated value here. An unretrofitted house is not the comparator for claims of incremental performance.
- Horizon: ten years after installation. The low/base/high scenarios assume eligibility of 40/60/80 homes out of 100 screened, and uptake among eligible homes of 25%/50%/75%. These are scenario inputs, not empirical adoption rates.
- Paths per participating home: 20/24/30 respectively, assumed for illustration only; actual spacing, tributary area and engineering schedule are site-specific. Hardware target: US$85 per path ex-workshop at a *future* 50,000 sets/year production scale. Inspection/parts planning allowance: US$10 per path-year, excluding access labor. Neither figure is a supplier quote or a full retrofit bid.
- Costs excluded: foundation anchor chemistry, repairs, roof/sheathing work, engineer, permits, installation, finish restoration, tax, property disruption and any maintenance labor. Installed cost cannot be computed from these inputs.

## Reproducible scenario arithmetic

Eligible homes = 100 × eligibility rate; participating homes = eligible homes × uptake; path sets = participating homes × assumed paths/home. Hardware-only target = sets × US$85. Ten-year inspection/parts allowance = sets × US$10 × 10 years. Both costs are gross modeled outlays, not incremental costs versus the conventional comparator.

| Scenario | Eligible / participating homes | Assumed paths/home | Path sets | Hardware-only target | Ten-year parts allowance | Sum of those two limited items |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 40 / 10 | 20 | 200 | US$17,000 | US$20,000 | US$37,000 |
| Base | 60 / 30 | 24 | 720 | US$61,200 | US$72,000 | US$133,200 |
| High | 80 / 60 | 30 | 1,800 | US$153,000 | US$180,000 | US$333,000 |

These scenarios vary eligibility, adoption *and* path count together; they are not confidence intervals. Even the high scenario is below the assumed 50,000-set/year manufacturing scale underlying US$85/path, so its unit price is especially uncertain. A sensitivity check at twice the hardware price doubles only the hardware column; repair and labor could dominate regardless. Annual inspection/parts allowances are US$2,000 / US$7,200 / US$18,000 across the participating cohort, before labor.

## Benefits and validation boundary

The physically relevant outcome is verified continuity and resistance of *each* installed path under site-specific loads, not the number of clips sold. For a conditional example, an assumed 1.5 m² tributary roof area under an assumed 2 kPa net uplift gives 3 kN demand before local pressure zones, internal pressurization and code factors. Reaching a 3 kN *characteristic* lab target does not prove a 3 kN *allowable* site capacity. A qualified designer must assess every deck, timber, fastener, wall, bracing and anchor interface against governing loads.[1][2]

A permitted 100-building pilot should report: screened-out/repair counts; fraction of designed paths physically verified; matched conventional retrofit completeness; characteristic assembled-path load distributions and weak-link failures; witness false green/red rates; full installed cost; corrosion and follow-up repairs. Pre-register storm exposure and roof-detachment/water-intrusion definitions if comparing field outcomes. There is no defensible numerical estimate yet of avoided losses, deaths, insurance savings or emissions. Do not count roof-covering, opening or flood protection as benefits of this tie; do not multiply connection strength by building count to infer resilience.

## Sources

[1] https://www.fema.gov/sites/default/files/documents/fema_improving-windstorm-resilience-fact-sheet_022023.pdf — FEMA windstorm and tornado resilience fact sheet, cited in README.
[2] https://ibhs.org/wind/continuous-load-path-clp/ — IBHS continuous load path and full-house wind research. Neither source validates this proposed assembly or its cost targets.
