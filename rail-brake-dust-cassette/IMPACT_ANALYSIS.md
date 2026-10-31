# Rail Brake Dust Cassette — Impact Analysis

**Author: jayis1**

**Status:** Illustrative scenario, not measured emissions, certified performance or a health forecast. Scope is PM10 mass originating at eligible *disc brakes*, not all railway PM10, wheel–rail wear or all friction materials. See the [README](README.md) for design gates and sources [1]–[4].

## Reproducible fleet scenario

Hold the **installed fleet at 10,000 compatible brake assemblies for one full year**; this is a scenario, not an adoption forecast. The emission-factor placeholders below already include each assembly's assumed annual friction-braking activity and regenerative-braking share. Do not multiply by train-km, stops or bogies again. The factor must ultimately come from representative measured brake-origin PM10 mass per assembly-year, with background and wheel–rail contributions separated. All figures in the table are **assumptions or derived results**, not observations from this invention.

| Variable / outcome | Low | Base | High |
| --- | ---: | ---: | ---: |
| Baseline brake-origin PM10, kg/assembly-year (assumed) | 0.2 | 1 | 3 |
| Whole-system PM10 capture at matched boundary, fraction (assumed) | 0.30 | 0.50 | 0.70 |
| Operational uptime with qualified cartridge, fraction (assumed) | 0.80 | 0.90 | 0.95 |
| Uncontained service release, fraction of collected mass (assumed) | 0.02 | 0.02 | 0.02 |
| Fleet baseline, tonnes/year (derived) | 2 | 10 | 30 |
| Gross retained PM10, tonnes/year (derived) | 0.48 | 4.5 | 19.95 |
| Net source PM10 retained after service release, tonnes/year (derived) | 0.4704 | 4.41 | 19.551 |

Equation (units explicit): `net tonnes/year = 10,000 assemblies × kg PM10/(assembly·year) × whole-system capture fraction × uptime × (1 − service-release fraction) ÷ 1,000 kg/tonne`. Base case: `10,000 × 1 × 0.50 × 0.90 × 0.98 ÷ 1,000 = 4.41 tonnes/year`. Low and high inputs are intentionally broad sensitivity bounds, not confidence intervals. Zero installation, failed safety qualification or negligible eligible friction-braking duty yields zero credited benefit. The README's ≥50% PM10 and ≥30% PM2.5 values are **prototype targets**, not measured capture; the low/high capture assumptions explore outcomes that could fail or exceed the PM10 gate. Do not apply PM10 fractions to PM2.5 or particle number.

## Cost and material boundary

At the README's **unquoted planning targets** ($180 housing, five-year life; $35 cartridge, two annual changes), hardware and media = `10,000 × ($180/5 + 2 × $35) = $1,060,000/year`, with 20,000 cartridge changes/year. In the base scenario this is approximately **$240 per net kg PM10 retained** (`$1,060,000 ÷ 4,410 kg`), before labor, downtime, capital financing, qualification, fan electricity, collection, transport and waste treatment; this is **not** cost per passenger exposure avoided. Two changes per year is an accounting assumption, not an established safe service interval. Recycled iron or copper revenue is set to **$0** until dust chemistry, yield and a licensed buyer are verified. Net lifecycle emissions and manufacturing impacts are unquantified.

## Exposure and evidence gates

No numerical platform PM reduction, avoided disease burden, passenger-hours or net climate benefit is claimed. Platform air mixes braking with wheel–rail and electrical wear, outside air, ventilation and resuspension; source reduction is not an exposure conversion factor. Before projecting exposure, measure controlled brake-origin mass over realistic normal/emergency cycles (fresh and loaded), actual annual braking duty, cartridge release during exchange, and operator uptime. Then run matched platform and worker-zone PM monitoring with ventilation, timetable and season recorded. Publish uncertainty and any negative results; reject deployment if stopping, cooling, retention or maintenance safety fails, even if collection is high.
