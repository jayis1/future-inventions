# Impact Analysis — Offline Care Consent Card

**Author: jayis1**

**Status:** Scenario arithmetic, not observed clinical impact or a cost-effectiveness finding. One-year steady-state model in US dollars; compare with actual local paper and offline-app workflows before procurement.

## Inputs and formulas

All figures below are **illustrative assumptions**, except the card/reader prices, which repeat the unquoted planning targets in the README. No clinical outcome improvement is assumed.

| Input | Model value | Status and limitation |
| --- | ---: | --- |
| Cardholders (low / base / high) | 10,000 / 100,000 / 1,000,000 | Hypothetical enrolment, not adoption forecast; low matches proposed pilot target |
| Visits with an attempted history read | 2 per cardholder-year | Assumption; count only actual opportunities, not card issuance |
| Card price and life | $10 / 5 years | Midpoint of README's $8–12 target; lifetime untested |
| Replacement and card service allowance | $2 per cardholder-year | README planning allowance; actual loss rate unknown |
| Reader price and life | $55 / 5 years | Midpoint of README's $40–70 target; reader can serve 500 cardholders (assumption) |
| Provisioning, training, translation, support and take-back | $2 per cardholder-year | Simplifying assumption, not a quote; may be materially higher |
| Existing paper workflow cost | $1 per cardholder-year | Hypothetical comparator, not a published benchmark; excludes clinician time |
| Minutes saved per attempted read (low / base / high) | 0.5 / 1 / 2 minutes | Conditional illustration, **not** a measured speed advantage; negative values are possible |

Annual card-pathway modeled cost per cardholder = $10/5 + $2 + ($55/5)/500 + $2 = **$6.022**. This is $5.022 more than the illustrative $1 paper comparator, before unmodeled certification, clinical review, security incidents and integration. This is amortized annual cost, **not first-year cash expenditure**. Readers required = cardholders / 500. Time difference in hours/year = cardholders × 2 attempts × assumed minutes saved / 60; this is clinician time capacity, not a cash saving. For a total fully loaded comparison, measure and add staffing, device failure, clinical workflow changes and actual comparator costs in each site.

| Scenario | Cardholders | Readers | Modeled annual card cost | Increment above assumed paper cost | Conditional staff hours freed/year |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 10,000 | 20 | $60,220 | $50,220 | 167 |
| Base | 100,000 | 200 | $602,200 | $502,200 | 3,333 |
| High | 1,000,000 | 2,000 | $6,022,000 | $5,022,000 | 66,667 |

The time values are rounded to whole hours. **No avoided-dose, error, dispute, illness or life-saved count is projected**: such effects would need a controlled comparator, measured baseline incidence and a credible causal link. The card may cost more *and* take longer than paper; if so, the modeled time benefit reverses. A reader procurement fee, card replacement spike, weak NFC coupling, exclusion of people unable to use the switch, coercion, or delayed key-revocation updates could erase any benefit or cause harm. Measure results by language and disability group, report privacy incidents and wrongful record associations, and stop deployment if clinical safety or voluntary choice deteriorates.
