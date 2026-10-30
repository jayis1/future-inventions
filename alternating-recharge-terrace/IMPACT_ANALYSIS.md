# Alternating Recharge Terrace — Impact Analysis

**Author: jayis1.** Scenario arithmetic, not field measurements or a forecast. See [README.md](README.md) for the proposed mechanism, targets and MAR prior-art sources [2][3]. No aquifer-recovery or potable-water benefit has been established.

## Boundary and assumptions

| Input | Planning assumption | Qualification |
| --- | ---: | --- |
| Total bed footprint | 50 m²/site | Two 25 m² beds; only one active at a time |
| Active-bed sustained flux | 0.03 m/h | Unverified target on suitable native soil for six hours |
| Eligible event duration | 6 h | Excludes first flush and unapproved runoff |
| Inlet limit | 0.25 L/s | At most 5.4 m³ in six hours; volume must be measured |
| Event frequency, low/base/high | 8 / 15 / 20 per year | Illustrative eligible events, not a rainfall prediction |
| Installed goal | US$1,300/site | Unquoted 2038 goal at 1,000 sites/year, excludes land, survey, permits and testing |
| Annual operating budget | US$100–200/site-year | Preliminary allowance; actual lab and disposal bills may exceed it |
| Illustrative life | 20 years | Accounting assumption, not proven equipment life; no discounting |

At target flux, maximum surface entry per eligible event is `min(25 m² × 0.03 m/h × 6 h, 0.25 L/s × 3,600 s/h × 6 h ÷ 1,000 L/m³) = min(4.5, 5.4) = 4.5 m³`. This assumes enough lawful, clean-enough water and no interruption; actual volume can be zero. The 1 m³ forebay is a settling volume, **not** additive storage or treatment credit. The 0.15 m maximum operating depth is a safety target, not an additional water-yield term.

## Annual surface-infiltration ceilings

| Scenario | Eligible events/site-year | Per site (m³/year) | 1,000 sites (m³/year) | 10,000 sites (m³/year) |
| --- | ---: | ---: | ---: | ---: |
| Low | 8 | 36 | 36,000 | 360,000 |
| Base | 15 | 67.5 | 67,500 | 675,000 |
| High | 20 | 90 | 90,000 | 900,000 |

Each cell is `4.5 m³/event × events × sites`, an **upper bound on surface infiltration**, not a net change in aquifer storage. Ten thousand sites occupy 500,000 m² (50 ha) of bed footprint before access, spacing, forebays and buffer land; suitability and available qualifying flows at that scale are untested. No double counting of diverted stream water as new water: a counterfactual equal-footprint single basin, prevailing runoff route and downstream allocation must be measured. The README's incremental pilot criterion is ≥20% more *cumulative qualified infiltration per total bed footprint* than a matched control, not a demonstrated 20% increase in regional groundwater.

## Cost and uncertainty

For an optimistic 20-year undiscounted accounting exercise, annualized installed goal is `US$1,300 ÷ 20 = US$65/year`. Adding US$100–200/year preliminary operations gives US$165–265/site-year, or **US$2.44–3.93 per m³ of upper-bound surface infiltration** at 67.5 m³/year. At 36 m³/year the same ratio is US$4.58–7.36/m³; at 90 m³/year it is US$1.83–2.94/m³ (rounded). These are *not* delivered-water costs: omitted land, surveys, permits, water testing, finance, discounting, downtime, recovery wells and distribution can dominate, while actual aquifer recharge could be zero. Do not infer payback or compare to water tariffs without an independently measured recoverable yield and like-for-like alternatives.

Net aquifer storage requires a water balance: measured eligible diversion minus bypass, evaporation, root-zone use, vadose-zone storage and other losses, adjusted for displaced natural recharge and downstream effects. Observation-well levels and chemistry, paired controls and a hydrogeological model are needed before assigning even an approximate recharge fraction. Sand alone does not ensure pathogen or chemical removal; a contaminated aquifer or impaired downstream right is a negative impact, not a tradeable yield. Stop or bypass on site-specific permit exceedances, shallow mounding, slope or overflow damage, or unavailable monitoring. The pilot must report paid maintenance hours, waste disposal, quality results and missed events alongside inlet and infiltrated volumes.
