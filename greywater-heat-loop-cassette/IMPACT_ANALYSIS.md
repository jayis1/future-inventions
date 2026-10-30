# Greywater Heat-Loop Cassette — Impact Analysis

**Author: jayis1. Status: scenario model, not measured performance or a deployment forecast.** Scope: shower drain → cold feed to an electric water heater, with no storage, pump or wastewater reuse. The existing README's 0.209 kWh example is five minutes at 4°C cooling; the central scenario below is eight minutes at the same cooling. Existing DWHR and no-exchanger controls must be measured before claims of superior performance.

## Inputs and boundaries

| Parameter | Low | Central | High | Basis |
| --- | ---: | ---: | ---: | --- |
| Simultaneous nominal water flow (L/min) | 9 | 9 | 9 | Design test condition, not a measured site mean |
| Shower duration (min) | 5 | 8 | 10 | Assumed active flow |
| Showers per unit per day | 1 | 2 | 3 | Assumed occupancy/use |
| Drain cooling across exchanger (°C) | 3 | 4 | 5 | Unverified target/sensitivity, not measurements |
| Flow coincidence factor | 0.60 | 0.80 | 0.90 | Assumed usable overlap, including mismatch |
| Availability after bypass/fouling | 0.90 | 0.95 | 0.98 | Assumed performance-equivalent uptime |

Common assumptions: 365 days/year; density 1 kg/L; specific heat 4.18 kJ/kg/K; 35°C drain, 15°C cold supply (20°C inlet gap). The 3–5°C cooling cases correspond to 15–25% of that gap at matched flows, **not** certified exchanger ratings. In warmer mains water, at lower flow or with a fouled exchanger, the assumed cooling may be unattainable. Theoretical thermal upper bound for the central 72 L shower is `72 × 4.18 × 20 / 3600 = 1.672 kWh`; the central modeled 0.334 kWh is below it. No auxiliary electrical demand is assumed because the concept is passive; any measured controls, pumping or additional distribution loss must be deducted.

## Reproducible calculation

`Gross recovered thermal kWh/shower = 9 L/min × duration min × 1 kg/L × 4.18 kJ/kg/K × drain cooling K ÷ 3600 kJ/kWh`.

`Annual useful heat kWh/unit = gross kWh/shower × showers/day × 365 × coincidence × availability`. The factors are assumptions, not field-observed reliability. To avoid counting non-overlapping showers twice, flow coincidence applies **once**, after active shower duration. For comparison with a simple electric heater, assume 90% delivered-heat-per-metered-kWh including heater losses; `avoided billed kWh = useful heat ÷ 0.90`, before any downstream distribution loss. At US$0.20/billed kWh and grid factors of 0.2 or 0.6 kg CO2e/billed kWh, savings are:

| Scenario | Gross heat/shower (kWh) | Useful heat/unit-year (kWh) | Avoided billed/unit-year (kWh) | Bill/unit-year (US$) | Avoided CO2e/unit-year (kg, low/high grid factor) |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 0.157 | 30.9 | 34.3 | 6.9 | 6.9 / 20.6 |
| Central | 0.334 | 185.5 | 206.1 | 41.2 | 41.2 / 123.7 |
| High | 0.522 | 504.6 | 560.7 | 112.1 | 112.1 / 336.4 |

For **one million eligible, functioning units** under the same assumed usage: 30.9 / 185.5 / 504.6 GWh/year useful heat (low/central/high); 34.3 / 206.1 / 560.7 GWh/year avoided billed electricity; US$6.9 / $41.2 / $112.1 million/year gross bill savings. At 0.2 kg CO2e/kWh, avoided operational emissions are 6.9 / 41.2 / 112.1 thousand tonnes CO2e/year; at 0.6 they are 20.6 / 123.7 / 336.4 thousand tonnes. This is a scale illustration, **not** a prediction that one million suitable sites exist or adopt the unit. Electrically powered heat pumps or gas heaters require different savings and emissions factors; do not apply these electric-resistance estimates to them.

## Economics and missing evidence

The README's unvalidated production goal of US$180 plus US$150–500 qualified installation implies US$330–680 upfront **before** unusually difficult retrofits. Illustrative US$15/unit-year cleaning/replacement allowance (not a quote) leaves central net operating savings of about US$26/year at this tariff; simple payback could exceed 12 years and reach roughly 26 years even before financing, failure and future replacement. In the low case the allowance exceeds modeled bill savings. Service labor, seal life, embodied manufacturing emissions and disposal are unmeasured; therefore **net lifecycle carbon savings and actual payback are unknown**. No claim of product superiority or universal retrofit economics follows from this model.

Prioritize 30 matched, metered 12-month pilot sites with approved vertical DWHR and no-recovery controls. Measure inlet/outlet temperatures and flows, heater input, pressure loss, drain head, blockage/bypass events, visible leakage, cleaning time and component failures. Vary mains temperature and occupancy; terminate or redesign on cross-connection, flooding or negative net value. The dominant uncertainties are achieved cooling after fouling, overlap, site eligibility, installation cost, tariff and displaced heater type. References for the existing DWHR/plumbing context are [2] and [3] in the invention README; every numerical outcome above is an explicit arithmetic scenario rather than a sourced product result.
