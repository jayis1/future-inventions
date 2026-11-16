# Intermittent-Pressure Joint Seal — Impact Analysis

**Author: jayis1**

**Status:** Scenario arithmetic, not measured performance, forecast, public-health claim or approval for drinking-water use. Time horizon: one operating year after repair; USD hardware goals are for 2038 at 10,000 kits/year.

## Boundary and baseline

Count only treated water no longer lost at *verified eligible joints* while the pipe is pressurized. The baseline is a metered 20 L/hour leak at each intact joint for eight pressurized hours/day, 365 days/year. These inputs are assumptions from the invention README, **not representative field averages**. Intermittent low-pressure intrusion is a separate safety outcome and is not valued in water-volume arithmetic; the product must not be used in drinking-water service without certification and utility approval. Comparison is with both no repair and a compliant conventional clamp, not an imaginary zero-cost alternative.

## Calculation

- Baseline per joint: 20 L/hour × 8 hours/day × 365 days/year ÷ 1,000 L/m³ = **58.4 m³/year**.
- Potential retention = eligible repairs × 58.4 m³/year × measured fraction of baseline leak eliminated × operating fraction of the year. Do not count leaks that recur; shorten operating fraction accordingly.
- **Upper bound in README:** 1,000 repairs × 58.4 × 1.0 × 1.0 = **58,400 m³/year**. This is a no-recurrence upper bound against *no repair*, not an incremental benefit over another successful fitting.

| Illustrative case | Eligible installed joints | Leak elimination | Effective operating fraction | Retained vs unrepaired (m³/year) |
| --- | ---: | ---: | ---: | ---: |
| Conservative | 100 | 50% | 75% | 2,190 |
| Central | 1,000 | 80% | 90% | 42,048 |
| Optimistic/upper bound | 1,000 | 100% | 100% | 58,400 |

The effective fraction captures partial-year service or re-leakage, not extra pressurized hours; eight hours/day is already in the baseline. Scale linearly only if measured baseline leaks and hours match. At 10 L/hour, each volume halves; at 40 L/hour, it doubles, assuming pressure and duty hours are unchanged. A real pilot must measure pre/post flow under matched pressure and demand, account for background/unrepaired leaks and analyze the certified-clamp control arm separately. If a conventional clamp retains the same volume, the cassette's **incremental water-volume benefit is zero**; only demonstrated safety, labor or lifecycle differences could justify it.

## Cost and material sensitivity

The README's **unquoted** hardware goal is US$95 per new kit (US$30 reusable 316L shell, US$20 initial EPDM sleeve, US$15 stops/bolts/test port and US$30 assembly/QA). A replacement sleeve is budgeted at US$15, with a proposed five-year inspection interval that is *not* established service life. For 1,000 new kits the hypothetical first-purchase hardware total is **US$95,000**, excluding excavation, isolation, labor, water testing, disinfection, approvals, shipping, tax and disposal. It is not a net saving. If 1,000 sleeves were replaced once, add US$15,000 in sleeve purchases before labor and disposal. No claim of reduced material waste is quantified until shell reuse, manufacturing yield and displaced conventional repair/replacement materials are measured.

At an illustrative *avoidable production cost* of US$0.25–1.00 per m³ (an explicit sensitivity assumption, not a sourced local tariff), central-case gross avoided production cost would be **US$10,512–42,048/year**; this is neither utility revenue nor net benefit. For 1,000 joints, the US$95,000 hardware goal alone would equal about **US$2.26/m³ in the first central-case year** (95,000 ÷ 42,048); financing, useful life and other costs change that figure. Never add this gross avoidance to customer bill savings as if they were distinct benefits.

## Evidence required before claiming impact

The 100-joint paired pilot must log installation and rejection rates, leak rate by pressure, bidirectional tracer assay limit and recovery, microbial results, recurrence and maintenance, water-quality incidents, installed lifecycle cost and pipe replacements avoided. Publish denominators and uncertainty intervals. Avoid extrapolating to population served, infections prevented or global non-revenue water: billing and metering losses are outside this joint-repair mechanism. Stop deployment on contamination signals or structural failures pending utility investigation.[1]

## Source

[1] U.S. EPA, *New or Repaired Water Mains* (2002): https://www.epa.gov/sites/default/files/2015-09/documents/neworrepairedwatermains.pdf
