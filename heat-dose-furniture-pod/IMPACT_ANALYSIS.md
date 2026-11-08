# Heat-Dose Furniture Pod — Impact Analysis

**Author: jayis1**

**Status:** scenario model, not measured impact or a claim of treatment efficacy. Reference design and safety exclusions: [README](README.md). Horizon: one operating year in 2050, conditional on successful independent validation and approvals.

## Model and assumptions

A pod treats one screened eligible article per cycle. Annual cycles = deployed pods × cycles/pod/year. Completed cycles = cycles × verified completion fraction; *avoided disposals* = completed cycles × fraction of completed articles that would otherwise have been discarded. That last fraction is an **assumption** requiring a counterfactual reuse-center audit; it is not synonymous with insects killed or infestations prevented. Excluded, failed or damaged items yield no avoidance credit. No avoided pesticide, furniture-manufacturing emissions, landfill impacts, health benefits or market revenue are counted without measured counterfactuals.

Electricity = cycles × metered kWh/cycle; gross operational emissions = electricity × assumed grid intensity. Electricity rate is an illustrative US$0.20/kWh; grid intensities below are scenario inputs (kg CO2e/kWh), **not** claims about any specific jurisdiction in 2050. Hardware cost uses the unquoted US$900 ex-workshop planning target per pod, excludes installation and replacements, and is *not* an annual cost. Design cap: ≤1.5 kW × ≤6 h = ≤9 kWh per cycle only for eligible loads meeting both caps; none of the scenario energy values are measured.

| 2050 scenario (assumed) | Low | Central | High |
| --- | ---: | ---: | ---: |
| Deployed pods | 20 | 100 | 500 |
| Cycles/pod/year | 100 | 200 | 250 |
| Verified-complete fraction | 70% | 80% | 90% |
| Counterfactual disposal fraction of completed articles | 10% | 25% | 40% |
| Metered electricity target, kWh/cycle | 8 | 6 | 4 |
| Assumed grid intensity, kg CO2e/kWh | 0.60 | 0.40 | 0.15 |
| Annual attempted loads | 2,000 | 20,000 | 125,000 |
| Annual verified-complete loads | 1,400 | 16,000 | 112,500 |
| **Potential avoided disposals, articles/year** | **140** | **4,000** | **45,000** |
| Annual electricity, kWh | 16,000 | 120,000 | 500,000 |
| Gross operating emissions, t CO2e/year | 9.6 | 48 | 75 |
| Electricity expense at US$0.20/kWh, US$/year | 3,200 | 24,000 | 100,000 |
| Hardware purchase at US$900/pod, US$ one-time | 18,000 | 90,000 | 450,000 |

## Net impact and sensitivity

For the central case, 100 × 200 × 0.80 × 0.25 = 4,000 *potential* avoided disposals/year; 20,000 × 6 = 120,000 kWh and 120,000 × 0.40 / 1,000 = 48 t CO2e/year gross electricity emissions. Without a measured emissions factor for the *actual* item displaced (including transport, alternate treatment, durability and end-of-life), net CO2e cannot be calculated responsibly. A break-even test would require more than 48,000 kg CO2e of **measured** net counterfactual savings in the central case, or >12 kg CO2e per credited item, before maintenance and transport emissions. This is a threshold, not an assertion of savings.

Per attempted load in the central case, electricity is US$1.20; add operator labor, sorting, transport, rent, calibration, repairs, failed cycles and amortized installed hardware before comparing with disposal or another heat chamber. If completion falls, attempted-cycle energy remains while credited reuse declines. If electricity exceeds 9 kWh for some loads, the rated-power/time design goal failed and those loads require a new eligibility or energy budget—not an extrapolated claim. A failed egg-survival trial or unresolved fire hazard stops deployment regardless of apparent waste savings.

## Evidence to collect

Meter wall energy and operator time for each eligible and rejected load; independently log cold spots, sentinel survival and damage; audit whether each item would truly have been discarded; record replacement parts and transport; use local time-specific grid intensities. Publish uncertainty intervals and compare matched workload and treatment endpoints to existing portable chambers rather than claiming that a pod inherently saves energy. EPA describes article heat treatment and portable units, but not this design's economic or environmental superiority.[1] Heat has no residual effect, so building-level infestation outcomes require separate follow-up.[2]

## Sources

[1] https://www.epa.gov/bedbugs/controlling-bed-bugs-using-integrated-pest-management-ipm — US EPA, article heat and IPM guidance.
[2] https://www.epa.gov/bedbugs/safety-issues-controlling-bed-bugs — US EPA, heat treatment safety and reinfestation.
