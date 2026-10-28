# Soil Extract Validity Kit — Impact Analysis

**Author: jayis1.** Scenario arithmetic, not measured impact or a forecast. Functional unit: one three-channel field encounter on a composite soil sample from one management zone. Scope: an illustrative cooperative network in one operating year after validation; no geography-specific population or nutrient-loss estimate is assumed. The test addresses nitrate in a specified water extract, not broad soil safety or a fertilizer prescription.

## Inputs and limits

| Input | Low / base / high assumptions | Status |
| --- | --- | --- |
| Reusable kits operated | 1,000 / 5,000 / 10,000 | Hypothetical adoption, not a market estimate |
| Encounters per kit per year | 20 in every case | README capacity assumption; includes invalid tests |
| Invalid fraction | 25% / 15% / 5% | Sensitivity assumption, **not** a measured failure rate or proof the gate detects all failures |
| Laboratory referral completion among invalids | 50% in every case | Hypothetical; monitor the actual fraction and cost |
| Ex-factory cost | $12 per reusable kit, $0.55 per packaged test | Unvalidated 2038 volume targets: 10,000 kits/year and 1,000,000 tests/year respectively; smaller scenarios cannot assume these prices are attainable |
| Shared-visit contacts | Up to five per encounter | Capacity ceiling from README; contacts are not independently tested farms |

The pilot must separately measure **false-valid** results (bad procedures that pass controls), **false-invalid** results, lab agreement and sampling quality. The invalid fractions here model workload, not test sensitivity. A post-filtration spike cannot detect poor extraction of native nitrate, and neither a valid reading nor a contact is an established agronomic or environmental benefit.

## Annual illustrative volumes

| Scenario | Encounters: kits × 20 | Invalid: encounters × fraction | Apparently valid: encounters − invalid | Completed referrals: invalid × 50% | Target hardware + consumables: kits × $12 + encounters × $0.55 |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 20,000 | 5,000 | 15,000 | 2,500 | $23,000 |
| Base | 100,000 | 15,000 | 85,000 | 7,500 | $115,000 |
| High | 200,000 | 10,000 | 190,000 | 5,000 | $230,000 |

These are *apparently* valid encounters: false-valids remain unknown until blind challenge studies. At most 100,000 / 500,000 / 1,000,000 shared-visit farm contacts result from encounters × five; no scenario demonstrates that those contacts changed fertilizer use. Nominal hardware-plus-consumables cost per apparently valid encounter is $23,000/15,000 ≈ $1.53 (low), $115,000/85,000 ≈ $1.35 (base), or $230,000/190,000 ≈ $1.21 (high). These ratios are **not** delivered cost per trustworthy decision: they omit labor, training, logistics, repeats, storage, disposal, referrals and potentially higher prices below production scale. A repeat for every invalid encounter would add invalid × $0.55 in consumables before any additional labor; not all repeats will resolve a failed soil matrix.

## Decision value and accounting boundaries

Do not monetize avoided fertilizer, yield, nitrate runoff, health or laboratory testing from these volumes alone. Compare a randomized or matched extension program with existing advice, recording actual fertilizer applied, yields, referral costs and downstream outcomes over multiple seasons. Some field encounters add information without displacing a laboratory analysis; some failures require one. Disclose how many reported bands were later overturned by a matched-extract laboratory result and how many invalids could not access confirmation. Procurement should use **total cost per independently confirmed usable decision**, not just the $0.55 material target.

Environmental accounting must include polymer hardware life, pad chemistry, cellulose filters, packaging, transport and disposal against the *actual* displaced process; no net emissions or water-quality benefit is claimed. For roadmap gates, see [ROADMAP.md](ROADMAP.md); the assay and its limitations are specified in [README.md](README.md).
