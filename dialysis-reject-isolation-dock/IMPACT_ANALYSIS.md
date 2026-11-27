# Dialysis Reject Isolation Dock — Impact Analysis

**Author: jayis1** · Scenario model, not measured dock performance or a reuse permit.

## Boundary and baseline

The input is dialysis-plant **RO reject only**, not spent dialysate, patient-contact water or disinfectant flush. An 11-machine US hospital estimated 927,000 L of RO reject in 2023; that is a single-site published estimate, not a per-clinic default.[1] Its documented baseline had water going to drain; other facilities may already reclaim qualified reject. Compare with the actual maintained site baseline and its approved nonpotable reuse, not with a fictional zero-reuse world. No recovered stream becomes potable or suitable for dialysis by passing the dock.

For this model only, an eligible clinic has 1–5 m³/day of reject on **300 operating days/year**, an existing full-flow permitted drain, approved toilet demand and accepted site assays. These are planning assumptions, not population statistics. Days without valid qualifications, sufficient tank space or approved use remain drain-only. Capture means entering the tank; displacement means metered nonpotable water actually delivered instead of mains makeup. The dock does not remove dissolved salts; toilet effluent still enters the approved sewer.

## Transparent annual scenarios per qualifying site

`Displacement (m³/year) = daily reject (m³/day) × operating days × eligible share × captured share of eligible reject × delivered share of tank admission`.

| Model input or output | Low | Base | High |
|---|---:|---:|---:|
| Reject, m³/operating day | 1 | 3 | 5 |
| Eligible share after cleaning/quality exclusions | 60% | 80% | 90% |
| Captured share of eligible reject | 40% | 50% | 70% |
| Delivered share after overflow, downtime and demand limits | 50% | 75% | 90% |
| Annual gross reject, m³ | 300 | 900 | 1,500 |
| Annual tank admission, m³ | 72 | 360 | 945 |
| Annual mains displacement, m³ | **36** | **270** | **850.5** |

The base 270 m³/year is **3 × 300 × 0.80 × 0.50 × 0.75**; 90 m³ admitted but not delivered is not counted as saved mains water. The low case misses the proposed ≥50% eligible-capture pilot gate and is a downside sensitivity, not a passing pilot. The high case assumes adequate local toilet demand and validated water quality; otherwise it collapses to the actual metered delivery. The cited hospital's 927 m³/year is a useful scale comparison, not an input to any modeled row.[1]

## Costs, power and adoption sensitivity

At an **illustrative** US$2/m³ avoided mains charge, the base gross water credit is **270 × $2 = $540/site-year** before wastewater tariffs, fees or taxes. Against the README's unquoted ≤US$5,000 installed target and unvalidated US$300/year seals/calibration/cleaning allowance, the arithmetic leaves **$240/year before** laboratory assays, plumber time, dedicated nonpotable plumbing, pump power, permits, depreciation and outages. It is **not** a payback or net-savings claim. An assumed incremental pump intensity of **0.2 kWh/m³ delivered** gives **54 kWh/site-year** at base output, excluding controls, treatment and embodied energy; measure these instead of assigning avoided emissions without a site-specific grid and mains-water factor.

If—and only if—ten comparable sites pass the pilot gates and attain the base case for a full year, their combined modeled displacement is **2,700 m³/year**. At the low and high inputs the same ten eligible sites would span **360–8,505 m³/year**, not a forecast of adoption. No global extrapolation, patient-health benefit or carbon saving is claimed. Sites with no approved endpoint or failed assays have **0 m³/year** displacement and still incur assessment costs; successful RO-efficiency upgrades can shrink reject availability.

## What the pilot must measure

Log RO inlet/product/reject, cleaning and drain volumes, tank admission/overflow, endpoint delivery and matched mains makeup; reconcile meter error and account for downtime. Test laboratory microbiology, salts/metals and cleaning agents to each site's approved nonpotable criteria, with independent backflow and drainage inspection. Report extra cleaning water, kWh, consumables, labor, false alarms, leaks and quarantined batches. Only measured delivery and actual mains displacement—after review of quality, plumbing and site rules—support an impact claim. See [SPECIFICATION.md](./SPECIFICATION.md) for go/no-go tests and [ROADMAP.md](./ROADMAP.md) for progression gates.

## Source

[1] Haddad, Kittner and Flythe, [“Thinking Globally, Acting Locally: Water Use in a Hospital Hemodialysis Unit”](https://pmc.ncbi.nlm.nih.gov/articles/PMC12282630/), *Kidney360*, online 2024. The 2023 figures are estimated for UNC Hospitals' 11-machine unit; the article cautions that equipment and operating conditions vary.
