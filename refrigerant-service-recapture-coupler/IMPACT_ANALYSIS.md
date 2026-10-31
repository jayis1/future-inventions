# Refrigerant Service Recapture Coupler — Impact Analysis

**Author: jayis1**
**Status:** Illustrative scenarios, not measured outcomes or a market forecast. The initial concept is unapproved pressure equipment for one future, specifically qualified nonflammable stationary-system refrigerant/port family. No prototype or field measurements exist.

## Boundary and method

The counterfactual is **the same service job with a maintained conventional low-loss fitting and normal certified recovery equipment**, not an open hose vented to air. Count only the *additional* mass prevented from reaching the atmosphere by the coupler during eligible connection/disconnection cycles, net of any recovery-path leakage or subsequent disposal. Recovered mass is not automatically avoided emissions. No bulk charge recovery, avoided installation leaks, adoption outside the qualified refrigerant family, or benefits claimed by the [Refrigerant Reclamation Microcart](../refrigerant-reclamation-microcart/) are counted here.

Annual avoided refrigerant (kg) = active pairs × eligible cycles per pair-year × independently measured net incremental avoidance (g/cycle) ÷ 1,000. For a single known gas, conditional 100-year climate equivalent (tonnes CO₂e) = avoided kg × GWP100 ÷ 1,000. Replace the illustrative avoidance input with a statistically supported matched-test estimate before using any figure as an impact claim.

## Inputs and scenarios

| Input | Low | Base | High | Status |
| --- | ---: | ---: | ---: | --- |
| Active matched pairs | 10,000 | 100,000 | 500,000 | Hypothetical deployments, not addressable-market estimates |
| Eligible cycles/pair-year | 50 | 100 | 200 | Hypothetical usage; excludes incompatible or skipped jobs |
| Net incremental avoidance versus low-loss fitting (g/cycle) | 0.05 | 0.20 | 0.40 | Unverified; can be zero or negative in reality |
| Annual incremental avoided mass (kg) | 25 | 2,000 | 40,000 | Derived product of rows above ÷ 1,000 |
| Conditional R-410A-only climate equivalent (t CO₂e/year) | 52.2 | 4,176 | 83,520 | Derived using EPA GWP100 = 2,088 [3] |

The last row is a **counterfactual sensitivity illustration**, not a claim that R-410A is the chosen first variant or that all deployed units handle it. Actual climate accounting must use each verified refrigerant's GWP, eligible event mix and measured losses; do not apply 2,088 to other gases. The base case reproduces the README's 100,000 × 100 × 0.2 g = 2,000 kg (2 tonnes) of *conditional* additional avoidance per year. An observed improvement of zero yields zero benefit regardless of deployment.

## Per-pair economics and resource cost

At the base usage assumption, 100 cycles × 0.2 g = 20 g/pair-year avoided. At an **illustrative, unsourced** US$20/kg replacement value, that is US$0.40/pair-year in refrigerant alone. The README's **unquoted planning targets** are US$45 ex-factory per matched pair at 100,000 pairs/year and US$4/year for seals/inspection, excluding rated recovery equipment, certification, installation, calibration and technician time. Refrigerant savings alone do not cover even the annual seal allowance. At 10 years and no discounting, the planning hardware-plus-seal allowance is US$85/pair before recovery gear and labor, versus US$4 in illustrative avoided refrigerant purchases; this is not a payback claim. Additional recovery time or cylinder logistics may make the device uneconomic. The project must measure these costs, durability and operational benefits rather than assume a business case from climate mass alone.

Machined brass/stainless and replaceable polymer seals require raw material, machining energy, pressure testing and eventual recycling/disposal; their lifecycle emissions are **not estimated**. A net climate benefit requires subtracting production/maintenance emissions and any extra service-energy or transport emissions from the conditional avoided CO₂e. Sensor power, cylinder handling and safe fluid disposition also belong in the boundary.

## Evidence gates and uncertainty

- Measure at least 500 matched cycles per arm using the same approved refrigerant, connection, hose, charge state, pressure and ambient temperature, with randomized order and qualified operators. Track complete-cycle atmospheric release by independent gravimetry, not solely chamber pressure or recovered-cylinder weight. Report uncertainty intervals and failure/rework rates.
- Repeat at temperature/pressure extremes, with liquid-filled dead spaces, aged seals, blocked recovery and power loss; confirm pressure-safe fault handling under qualified laboratory supervision. A ≤0.5 g total-release target and ≥5,000-cycle durability gate are **design goals**, not evidence of superiority.
- Sample actual eligible job counts and refrigerant mix before extrapolating; missing or incompatible jobs reduce coverage. A2L/A3, R-744, ammonia, unknown mixtures and motor-vehicle systems are excluded from the initial concept. Cylinder contamination, repeat transfers and later leakage can erase a nominal captured-mass benefit.
- Compare ongoing low-loss fittings as they improve; avoid double-counting charge recovery already required by law or already attributed to a different device. If trials find no incremental advantage or unsafe handling, retire the impact projection.

## References

[1] US EPA, stationary refrigeration service practice requirements: https://www.epa.gov/section608/stationary-refrigeration-service-practice-requirements
[2] US EPA, Section 608 technician certification requirements: https://www.epa.gov/section608/section-608-technician-certification-requirements
[3] US EPA, Technology Transitions GWP Reference Table (R-410A = 2,088, calculated from 100-year constituent factors): https://www.epa.gov/hfcs/technology-transitions-gwp-reference-table
