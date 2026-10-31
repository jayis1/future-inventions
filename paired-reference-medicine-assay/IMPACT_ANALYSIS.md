# Paired-Reference Medicine Assay — Impact Analysis

**Author: jayis1**

**Status:** illustrative capacity and expenditure model; no measured clinical benefit, validated assay performance or procurement quotation.

## Scope and assumptions

One supervised screening opportunity consumes one tablet and one card from one lot of a single validated immediate-release formulation. A suspect or inconclusive reading is referred to a qualified laboratory; neither result proves medicine quality. This model does not extrapolate the WHO population-level substandard/falsified estimate to any individual site or infer lives saved.[1]

| Input | Illustrative planning value | Basis / exclusion |
| --- | ---: | --- |
| Sites × lots screened/site/year | Limited: 250 × 50; planning: 1,000 × 100 | Scenario choices, not forecast adoption. |
| Suspect + inconclusive referral share | Limited 2%; planning 5%; stress 10% | Scenario choices, not prevalence or measured error rates. |
| Disposable cost | US$1.20/screen | Unquoted 2038 volume target from README; excludes overhead. |
| Reader purchase | US$180/site, assumed one/site | Unquoted 2038 volume target; first year only, assumed zero salvage. |
| Reader servicing | US$30/site/year | Placeholder from README. |
| Referral | At least US$5/referral | Placeholder floor from README, **not** a real HPLC quote. |
| Training, sampling labor, shipping, reference QA, waste, certification, full laboratory cost | Not priced | Must be measured locally before an investment decision. |

## Transparent scenarios (annual)

Screens = sites × lots/site. Referrals = screens × referral share. First-year *modeled floor* = (screens × US$1.20) + (sites × US$180) + (sites × US$30) + (referrals × US$5). Recurring floor excludes reader purchase and assumes readers remain serviceable; all figures are US dollars, before excluded costs.

| Scenario | Screens | Referrals | Card spend | Reader purchase | Service | Referral floor | First-year modeled floor | Later-year modeled floor |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Limited: 250 sites × 50; 2% referred | 12,500 | 250 | $15,000 | $45,000 | $7,500 | $1,250 | $68,750 | $23,750 |
| Planning: 1,000 sites × 100; 5% referred | 100,000 | 5,000 | $120,000 | $180,000 | $30,000 | $25,000 | $355,000 | $175,000 |
| Referral stress: 1,000 sites × 100; 10% referred | 100,000 | 10,000 | $120,000 | $180,000 | $30,000 | $50,000 | $380,000 | $200,000 |

At planning volume, doubling the referral share from 5% to 10% adds **$25,000** to this placeholder floor and **5,000** laboratory referrals, before any actual HPLC charges or follow-up costs. Capacity for those referrals must be contracted in advance. The 100,000 cards also imply 100,000 disposable card waste items plus consumed solvent vessels per year; mass, solvent volume and disposal cost are unknown until the prototype bill of materials is measured.

## What this cannot claim

The published literature notes that portable screening for reduced-dose products is harder than screening for absent/wrong API.[2] The README's ≥90% sensitivity, ≥95% specificity and ≤5% invalid-control goals are proposed gates, **not** inputs to a projected count of substandard products caught. Referral share mixes true defects, false alarms and invalid tests, and is not a prevalence estimate. Sampling one tablet per lot cannot establish batch uniformity; errors could cause missed hazards or unnecessary stock disruption. Report HPLC-confirmed true/false alerts, cost per valid screen, follow-up times, environmental waste and medicine-access effects in a prospective pilot before estimating health or economic benefit. GPHF Minilab TLC remains a relevant field comparator, not an interchangeable laboratory truth standard.[3]

## Sources

[1] https://www.who.int/news-room/fact-sheets/detail/substandard-and-falsified-medical-products — WHO estimate, not a local prevalence assumption.
[2] https://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0009360 — evaluation of portable screening devices.
[3] https://www.gphf.org/en/minilab/factsheet.htm — Minilab fact sheet.
