# Spectral-Guard Air Disinfector — Impact Analysis

**Author: jayis1** · Scenario model, not a measurement or health-benefit forecast. Concept status: no prototype efficacy, exposure or ozone result. See [README.md](./README.md) and [SPECIFICATION.md](./SPECIFICATION.md).

## Boundary and assumptions

The unit of comparison is one independently qualified fixture in one **50 m³** eligible room. Existing ventilation, filtration, diagnosis and respiratory protection stay in place. The scenarios below describe a hypothetical mature year of operation, not a dated adoption prediction. All installation counts and eACH values are assumptions; the ≥5 additional eACH base case is an **unverified research target**, not a measured value. Negative chemistry or exposure results mean zero permissible occupied-mode output, regardless of modeled benefit.

| Input | Conservative | Base | Stretch | Basis |
|---|---:|---:|---:|---|
| Eligible installed rooms / fixtures | 1,000 | 10,000 | 50,000 | Illustrative adoption; one per room, no double counting |
| Additional viable-surrogate eACH while operating | 2 | 5 | 8 | Assumptions under documented room mixing; base matches specification target |
| Availability while rooms are scheduled for use | 50% | 80% | 90% | Assumed uptime; sensor expiry and safety shutdown count as off |
| Scheduled use | 2,000 h/year | 2,000 h/year | 2,000 h/year | Assumed 8 h/day × 250 days; no benefit outside this window |
| Input power while on | 60 W | 60 W | 60 W | Specification ceiling; conservative energy estimate, not measured draw |
| Fixture plus installation | US$600–750 | US$600–750 | US$600–750 | US$450 ex-factory *target* + US$150–300 installation estimate; excludes survey, taxes, certification and electrical retrofit |
| Annual service per installed room | US$80–150 | US$80–150 | US$80–150 | Existing research estimate, excludes ventilation, lab retests and disposal |

## Arithmetic and scenario outputs

For a well-mixed surrogate, incremental equivalent clean airflow while operating = `50 m³ × additional eACH` (m³/h). Annual equivalent treated-air volume = airflow × `2,000 h × uptime` × installed rooms. This is a *comparison metric for viable airborne surrogate decay*, not a physical intake flow, certified particle CADR or guaranteed exposure reduction. Aggregate instantaneous equivalent airflow below is time-averaged across scheduled hours; an off fixture supplies zero incremental eACH.

| Output | Conservative | Base | Stretch |
|---|---:|---:|---:|
| Additional equivalent airflow per operating room | 100 m³/h | 250 m³/h | 400 m³/h |
| Average fleet equivalent airflow during scheduled hours | 50,000 m³/h | 2,000,000 m³/h | 18,000,000 m³/h |
| Annual modeled equivalent treated-air volume | 100 million m³ | 4 billion m³ | 36 billion m³ |
| Operating electricity per room/year at 60 W ceiling | 60 kWh | 96 kWh | 108 kWh |
| Fleet operating electricity/year at 60 W ceiling | 60 MWh | 960 MWh | 5,400 MWh |
| Initial fixture + installation | US$0.60–0.75m | US$6.0–7.5m | US$30–37.5m |
| Recurring service/year | US$0.08–0.15m | US$0.8–1.5m | US$4.0–7.5m |

At the base assumption, dropping realized eACH from 5 to 2.5 halves equivalent airflow and annual modeled volume (250 → 125 m³/h per operating room; 4 → 2 billion m³/year fleet) while electricity and maintenance stay unchanged. If mixing or aged lamps reduce the measured rate below the acceptance gate, report the observed result, not the target; if exposure or air-quality limits fail, use zero occupied-mode contribution. Operating electricity excludes manufacturing, external battery conversion losses, ventilation and catalyst service.

## What this does not project

No number of infections, TB cases, deaths or carbon emissions avoided can be defensibly inferred from equivalent airflow alone. A room's infective source strength, occupancy, near-field exposures, aerosol spectrum, baseline ventilation, contact patterns and health outcomes are not specified. Published room-sized far-UVC chamber work found substantial *S. aureus* reductions with five filtered sources at 3 ACH ventilation, but its lamp count, test organism and mixing cannot be transferred to this design.[3] EPA distinguishes particle-cleaner CADR and other pollutant controls; UV inactivation alone does not remove CO₂ or particles.[4] ASHRAE 241's equivalent-clean-airflow framework includes installation, performance and safety requirements, not a shortcut to certification.[6]

An occupied pilot needs independent spectrally weighted exposure mapping at the worst accessible position; viable-aerosol on/off decay with multi-position sampling and confidence intervals; and ozone, aldehyde and secondary-particle testing under low approved ventilation and representative VOCs. A reported 2024 restroom study measured a mean 5 ppb ozone increment from 222 nm GUV under 1–2 h⁻¹ ventilation; this is a reason to measure site chemistry, not this fixture's predicted increment.[7] Track failed assessments, lamp-off time, energy, service costs and replacement/disposal. Only separate, appropriately controlled epidemiological studies could support an infection-outcome claim.

## Sources

[3] https://www.nature.com/articles/s41598-022-08462-z
[4] https://www.epa.gov/indoor-air-quality-iaq/guide-air-cleaners-home
[6] https://www.ashrae.org/about/news/2023/ashrae-publishes-standard-241-control-of-infectious-aerosols
[7] https://pubs.rsc.org/en/content/articlelanding/2024/em/d4em00144c
