# Passive Flood Door Sill — Impact Analysis

**Author: jayis1.** Illustrative US-dollar scenario arithmetic for a *hypothetical cohort of 1,000 engineer-screened, above-grade doorways*, not a forecast, measured efficacy, insurance claim or offer of flood protection. The counterfactual is the same eligible buildings using their existing warnings and property-level flood measures **without this panel**, not buildings with no resilience. One doorway is not a building.

## Model and assumptions

- Time horizon: one year of expected avoided damage; also a simple undiscounted 10-year comparison with constant annual rates. Geography: no specific market claimed; figures are generic US-dollar planning inputs, not local loss data.
- 1,000 candidate doors are **assumed** to pass structural, site, regulatory and egress screening; actual eligibility is unknown. Adoption ranges from 10% to 90% of this selected cohort, not of all flood-prone homes.
- Annual event probability per installed site is an illustrative 5% / 10% / 20%. Events are treated as independent *for expected-value arithmetic only*; severity and repeated damage may be correlated.
- Conditional avoided damage per successfully protected event is an **assumption** of US$2,000 / $5,000 / $10,000 versus that site's counterfactual. It excludes fatalities, injuries, displaced residents, business interruption and environmental benefits.
- Effective-protection share of events is 20% / 40% / 60%. This explicitly discounts for missed manual fitting, heads above 0.6 m, relief opening, leakage, failure and alternate paths such as walls, vents and drains. This share is unmeasured and may be zero; deliberate pressure relief admits water and can reduce avoided damage while protecting the structure.
- Installed cost **assumed** at $500 per door, including panel and labor; $30 per installed door per year for inspection/seal reserve. These are not supplier quotes. The README's US$90–140 is a separate unverified *factory* target and must not be mistaken for installed cost. Structural reinforcement, certification, insurance, taxes, flood cleanup and disposal are excluded and could dominate.

## Conditional annual outcomes

`Expected avoided damage = 1,000 eligible doors × adoption × event probability × effective-protection share × avoided damage per successful event.` Results are cohort expectations, not literal fractional floods at one site.

| Scenario | Adoption | Installed doors | Event probability/year | Effective share | Avoided damage/success | Modeled avoided damage/year | One-time install | Annual upkeep |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Low | 10% | 100 | 5% | 20% | $2,000 | $2,000 | $50,000 | $3,000 |
| Base | 50% | 500 | 10% | 40% | $5,000 | $100,000 | $250,000 | $15,000 |
| High | 90% | 900 | 20% | 60% | $10,000 | $1,080,000 | $450,000 | $27,000 |

Base worked example: 500 installed doors × 0.10 events/year = 50 expected affected doors/year; × 0.40 effective protection = 20 successful events/year; × $5,000 conditional loss avoided = $100,000/year. This does **not** mean 20 homes are kept dry. The low case allows negative value; if benefit is zero, the entire cost remains.

A naive, undiscounted 10-year net (`10 × annual modeled avoided damage − installation − 10 × annual upkeep`) is **−$60,000 / +$600,000 / +$10,080,000** in low/base/high. These are not net-present values: no discounting, inflation, financing, catastrophic tail risk, insurance effects, substrate repair, recertification or changes in hazards are included. At the base parameters, reducing the effective-protection share from 40% to 20% halves modeled annual avoided damage to $50,000 while installed and upkeep costs remain unchanged.

## Evidence and stop conditions

No field efficacy, deployment reliability, local loss distribution or lifecycle footprint has been measured. A pilot must record warning availability, fitting rates, matched-event depth/velocity, leakage, hatch activation and flow, other ingress routes, damage against comparable untreated sites, structural and egress outcomes, maintenance and embodied/recycled material mass. Independently check whether installed costs, hatch failures or low effective protection reverse the economics before scaling. Never use these modeled numbers to justify a panel where engineered flood openings, evacuation or other safer floodproofing methods are required; building-level guidance explains why pressure equalization and alternate pathways matter.[2]

[2] https://basc.pnnl.gov/information/design-and-retrofit-flood-protection
