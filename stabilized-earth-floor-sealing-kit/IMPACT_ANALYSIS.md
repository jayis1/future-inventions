# Impact Analysis — Stabilized Earth Floor Sealing Kit

**Author: jayis1**
**Status:** Scenario arithmetic, not measured impact or a sales forecast. USD values are hypothetical 2035 nominal material budgets with no inflation adjustment. Geography is unspecified: adoption is among suitable dry-site rooms only, not a share of all global earth-floor households.

## Assumptions and boundaries

| Input | Assumption / source | Boundary |
|---|---|---|
| Cumulative rooms installed by end-2035 | Low 1,000; central 10,000; high 100,000 (illustrative adoption scenarios) | One 12 m² room per installation; no automatic assumption of one new healthy household |
| Area per room | 12 m² (project [README](./README.md)) | Excludes other rooms and drainage work |
| Topping and binder | 32 kg dry mix/m²; 2.4 kg each hydrated lime and calcined clay/m² ([SPECIFICATION.md](./SPECIFICATION.md)) | Target dry density 1,600 kg/m³ at 20 mm; no measured yield |
| Material budget | US$5–8/m² design target at 10,000 kits/year in 2035 | Scenario endpoints use the same target even at lower volume; this may be optimistic. Excludes labor, transport, screening, drainage, taxes and finance |
| Repairs / lifetime | US$1/m² patching over a proposed ten-year service period | Both are unverified hypotheses; excludes labor and replacement |
| People using each room | 4, illustrative, not observed | Counts possible room users, not health beneficiaries or distinct households |
| Carbon reference only | Illustrative 50 mm concrete layer and GSA concrete EPD limit band 228–277 kg CO₂e/m³ for ≤2,499 psi concrete[3] | U.S. *procurement limits*, not measured local slabs, whole assemblies or a claim of functional equivalence |
| Kit carbon | Unknown pending local cradle-to-grave LCA, including lime process CO₂, clay calcination, transport, patching and disposal | No net avoided-emissions figure can responsibly be stated |

## Quantitative scenarios (all projections, cumulative through 2035)

Formula: rooms × 12 m²/room = area; area × 32 kg/m² = topping mass; area × 2.4 kg/m² = mass of **each** binder; area × US$5–8/m² = material-budget range. These figures are *inputs and spending*, not benefits.

| Scenario | Rooms / area | Dry mix; each binder | Material budget (US$) | Ten-year patch materials (US$1/m² hypothesis) |
|---|---:|---:|---:|---:|
| Low | 1,000 / 12,000 m² | 384,000 kg; 28,800 kg | 60,000–96,000 | 12,000 |
| Central | 10,000 / 120,000 m² | 3,840,000 kg; 288,000 kg | 600,000–960,000 | 120,000 |
| High | 100,000 / 1,200,000 m² | 38,400,000 kg; 2,880,000 kg | 6,000,000–9,600,000 | 1,200,000 |

### Health and equity — exposure reach, not disease effects

| Scenario | Possible room users (rooms × 4) | Projected infections, diarrhea cases or DALYs averted |
|---|---:|---|
| Low | 4,000 | Not estimable |
| Central | 40,000 | Not estimable |
| High | 400,000 | Not estimable |

Piso Firme found improved child health after replacing dirt with **cement**, not this limewash/earth assembly.[2] Even the assumed room-user counts may overlap across installations. A voluntary controlled comparison must establish this kit's own dust and health effects; don't apply the cement study's percentages to these people. Residents on damp, contaminated or unstable sites need another solution rather than inclusion in the rollout denominator.

### Cost comparison — unknown until local quotes

The table above projects **gross material spending**, not household savings. Ten-year target material-and-patch spend is US$6–9/m², or US$72–108 for one 12 m² room, before labor, drainage, inspections, distribution or discounting. EarthEnable says it charges about US$4/m² for its *different, installed oil-sealed floor* in its operating area; that self-reported selling price is not a valid universal comparator or a price this kit beats.[1] Net savings = installed and maintained cost of a functionally suitable *local alternative* minus installed and maintained kit cost; both must be quoted at the same site and service horizon. A negative result means the kit costs more.

### Carbon — reference volume, not emissions saved

For perspective only, a hypothetical 50 mm concrete layer has volume `area × 0.05 m`. Multiplying that volume by GSA's **limit** band of 228–277 kg CO₂e/m³[3] yields the following reference-stage figures. A 50 mm layer is not necessarily a code-compliant slab and cannot be assumed to serve the same function as this 20 mm topping.

| Scenario | Hypothetical concrete volume | Reference production GWP at the cited limits, not avoided emissions |
|---|---:|---:|
| Low | 600 m³ | 136,800–166,200 kg CO₂e |
| Central | 6,000 m³ | 1,368,000–1,662,000 kg CO₂e |
| High | 60,000 m³ | 13,680,000–16,620,000 kg CO₂e |

Net climate impact would be `locally suitable baseline's full life-cycle GWP − kit's full life-cycle GWP`, normalized per serviced m²-year and including base preparation, binder manufacture, freight, repair and replacement. Baseline might instead be bare earth or an already low-carbon improved-earth floor; in either case the hypothetical concrete figure must **not** be counted as avoided carbon.

## Sensitivity and decision gates

Adoption changes all aggregate volumes linearly; doubling suitable rooms doubles materials, costs and possible room users but proves no health gain. A US$1/m² increase in material price adds US$12 per modeled room; a service life below ten years increases annualized cost and replacement impacts. Local calcined-clay energy and failed moisture screens could dominate the carbon and access case. Pilot measurements should establish site rejection rates, full installed prices, wet slip, dust, abrasion and actual service life before any ROI, DALY, avoided-emissions or global-benefit claim is made. Stop deployment on persistent damp, unsafe dust or excessive repair demand.

## Sources

[1] https://earthenable.org/faqs — EarthEnable FAQs
[2] https://mdcattaneo.github.io/papers/Cattaneo-Galiani-Gertler-Martinez-Titiunik_2009_AEJ-Policy.pdf — Housing, Health, and Happiness (2009)
[3] https://www.gsa.gov/real-estate/for-businesses-seeking-opportunities/ira-lec-material-requirements — GSA low embodied carbon concrete limits
