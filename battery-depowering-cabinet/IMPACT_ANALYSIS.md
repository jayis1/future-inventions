# Battery Depowering Cabinet — Impact Analysis

**Author: jayis1** · Illustrative annual scenarios, not observed performance or a forecast. Scope: ten staffed sites, one cabinet and one pack per bay at a time. See the [research specification](SPECIFICATION.md) and [README](README.md). No recovered materials or avoided fires are credited to the cabinet; those depend on downstream recycling and a comparable control.

## Model and assumptions

- Accepted only: manufacturer-labelled, intact rechargeable Li-ion packs with approved external contacts, nominal 3.6–14.8 V and rated ≤50 Wh. Rejected/unknown packs require a separate route. Feed figures below are *eligible packs after screening*; rejected counts and total incoming feed are unknown.
- Capacity per site/month = floor(operating days × available bay hours/day ÷ mean occupied bay hours/pack × uptime). Processed = min(eligible monthly feed, capacity). Annual site and network totals multiply the monthly result by 12 and 10 respectively. The mean occupied time includes loading, discharge, cooldown, checks and handoff; these values are assumptions, not tested cycle times.
- Illustrative extractable energy is 10, 25 or 50 Wh/processed pack (all at or below the 50 Wh rated-energy ceiling). Resistor heat estimate = processed packs × assumed extractable Wh; real charge state, electrical losses and pack electronics change the result. Ancillary electricity, thermal-event loads and building ventilation are *not* included or claimed offset by this energy.
- Annual fixed cabinet allowance = US$1,500 purchase ÷ five years + US$350 service = US$650/site/year, using the README's unvalidated design example; excludes installation premium, financing, staff, packaging, site protection, insurance, shipping and recycler fees. Incremental economics relative to collection-only cannot be determined without measured costs for both routes.

| Case | Eligible feed/site/mo | Days × bay hours/day | Mean occupied hours | Uptime | Capacity/site/mo | Processed/site/mo | Processed/10 sites/year | Assumed Wh/pack | Heat/site/year |
|---|---:|---|---:|---:|---:|---:|---:|---:|---:|
| Low | 25 | 20 × 8 | 3.0 | 80% | 42 | 25 | 3,000 | 10 | 3 kWh |
| Base | 100 | 26 × 10 | 2.5 | 95% | 98 | 98 | 11,760 | 25 | 29.4 kWh |
| High | 150 | 26 × 12 | 2.0 | 95% | 148 | 148 | 17,760 | 50 | 88.8 kWh |

The base case falls slightly short of the README's 100/site/month pilot aspiration because 260 nominal bay-hours at 95% uptime support only 98 cycles of 2.5 hours. Ten-site resistor heat is 30, 294 or 888 kWh/year in these scenarios, released locally rather than recovered as electricity. A single full 50 Wh pack corresponds to 180 kJ; a 25 W mean resistive discharge alone would require at least two hours in the ideal case. Actual cycle lengths and heat profiles need instrumented testing; a cell failure could release energy well beyond normal discharge heat.

At the modeled US$650 annual fixed allowance, cost per processed pack is US$2.17 (low), US$0.55 (base) or US$0.37 (high), **before** all excluded costs. No saving is implied: the collection-only comparator avoids cabinet purchase and can still require trained labor, isolation, compliant transport and recycler fees. If rejection rates or feedstock reduce eligible supply, utilization and cost/pack worsen; if discharge time increases or downtime rises, capacity drops. Measure incoming, rejected, accepted and successfully handed-off packs separately.

## What a pilot must prove

Compare matched eligible-pack cohorts at staffed collection-only and cabinet sites: operator minutes/pack; mis-sort and false-release counts; electrical/thermal faults and near misses; verified recycler acceptance; and total cost including staff, installation, power, packaging, transport, service and insurance. Predefine incident reporting and stop rules with independent reviewers. A zero-incident pilot cannot establish a reliable fire-prevention rate; environmental gains require auditable *additional* collection and actual authorized recycling, not merely heating batteries onsite. No battery mass, emissions, recovered metals, avoided incidents or lives-saved projection is justified by the present data.
