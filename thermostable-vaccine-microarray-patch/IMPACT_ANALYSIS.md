# Thermostable Vaccine Microarray Patch — Impact Analysis

- **Author:** jayis1
- **Status:** Illustrative annual scenario arithmetic, **not measured outcomes or a forecast**. Applies only after a named vaccine is licensed with the storage and immune-response claims required for its setting.
- **Scope:** One hypothetical vaccination programme; counts are administered doses, not additional immunized people. No deaths or DALYs are estimated.

## Inputs and provenance

| Input | Value | Type and interpretation |
|---|---:|---|
| Low / base / high annual administrations | 10 / 50 / 100 million | Scenario assumptions; same number of administrations in both arms, not incremental reach. |
| Conventional shipped-dose loss | 10% | Scenario assumption including all causes, not a WHO population estimate. |
| Patch shipped-dose loss | 5% | Aspirational scenario assumption including production-approved distribution failures; must be demonstrated locally. |
| Conventional temperature-controlled logistics | $0.40 per dose shipped | Scenario assumption, excludes antigen and injection labour. |
| Patch temperature-managed logistics | $0.10 per dose shipped | Scenario assumption; **not** zero-temperature control. |
| Incremental patch/pack/provision cost | $0.60 per dose administered | Scenario assumption **above** the conventional presentation, after matching included packaging/disposal categories; not the README's absolute $0.80–1.50 patch/pack price. Excludes antigen and any different production yield. |
| Worker time | 12 minutes conventional / 8 minutes patch per administration | Scenario assumptions including preparation, administration and record; neither clinically established. |
| Conventional exposed sharps | 1 per administration | Scenario accounting assumption; patch target is zero **exposed** needles, but backing remains clinical waste. |

README/SPECIFICATION engineering goals are **targets**, not field observations: 24 months at 25 °C/60% RH, 30 days at 40 °C with ≥90% release potency, ≥95% needle insertion and 90–110% label-claim content. No model input assumes clinical equivalence has been shown.

## Method

For `D` million administered doses, conventional shipments = `D / 0.90`, patch shipments = `D / 0.95`; thus fewer shipped units are a *wastage* result, not extra vaccinations. Temperature-logistics difference in $million = `0.40 × conventional shipments − 0.10 × patch shipments`. Net modeled budget difference = logistics difference − `0.60 × D` (negative means patch costs more). Worker hours freed in millions = `D × (12 − 8) / 60`. Sharps avoided in millions = `D`, conditional on successful substitution; used backing still needs regulated handling.

| Scenario | Administered (million/year) | Shipped conventional → patch (million/year) | Units not shipped (million/year) | Logistics difference ($million/year) | Net modeled budget difference ($million/year) | Worker hours freed (million/year) | Exposed sharps avoided (million/year) |
|---|---:|---:|---:|---:|---:|---:|---:|
| Low (20% of base uptake) | 10 | 11.11 → 10.53 | 0.58 | +3.39 | **−2.61** | 0.67 | 10 |
| Base | 50 | 55.56 → 52.63 | 2.92 | +16.96 | **−13.04** | 3.33 | 50 |
| High | 100 | 111.11 → 105.26 | 5.85 | +33.92 | **−26.08** | 6.67 | 100 |

Numbers rounded after calculation. At **50% of base adoption** (25 million/year), the same assumptions imply 27.78 → 26.32 million shipped, 1.46 million units not shipped, +$8.48 million logistics difference, **−$6.52 million net budget**, 1.67 million worker hours freed and 25 million exposed sharps avoided. These are gross time savings, not automatically redeployable paid hours.

## Limits and decision rule

A 5-percentage-point shipment-loss improvement does **not** imply a 5-point coverage increase; missed people, antigen shortage, late visits and refusal require separate evidence. Potency loss or incomplete delivery could erase all benefits despite a completed witness. At base assumptions the patch has a modeled $13.04 million annual *premium* before training, quality assurance, take-back, regulatory compliance, manufacturing yield and any improved health outcomes; those costs and outcomes need local measurement. The break-even incremental provision cost under this narrow model is approximately **$0.339 per administration** (`$16.96m / 50m`), lower than the assumed $0.60. Pilot procurement should compare **cost per successfully immunized person**, stratified by geography and age, and retain conventional injection if safety, immune response, supply reliability or economics fail. Carbon and lives-saved claims are omitted because no defensible transport-energy or epidemiological inputs are available.
