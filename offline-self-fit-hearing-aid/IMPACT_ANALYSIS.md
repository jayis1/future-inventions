# Offline Self-Fit Hearing Aid — Impact Analysis

**Author: jayis1. Illustrative scenario model, not clinical evidence or a sales forecast.**

## Baseline and scope

WHO reported in 2024 that **over 400 million people** could benefit from hearing devices and **fewer than 20%** of those needs were fulfilled.[1] This is a global context figure, **not** the number eligible for this adult mild-to-moderate air-conduction design. One unit equips one ear, not necessarily one person; age, diagnosis, preferences, bilateral fitting and local regulation shrink the actual eligible market. The intervention must not displace clinical care, captions or sign language.

Model horizon: one distribution year, with six-month retained-use observation for each year's cohort. No clinical effect size or health-economic savings are assumed. All rates and budgets below are **scenario assumptions** or unverified README targets, not measurements.

## Explicit scenario assumptions and arithmetic

| Scenario | Aids issued/year (assumption) | Valid fit fraction (assumption) | Six-month continued use among valid fits (assumption) | Valid fits = issued × fraction | Active aid-ears at six months = valid fits × use |
| --- | ---: | ---: | ---: | ---: | ---: |
| Low | 50,000 | 60% | 60% | 30,000 | 18,000 |
| Base | 100,000 (README deployment scenario) | 80% | 80% (README test target) | 80,000 | 64,000 |
| High | 150,000 | 90% | 80% | 135,000 | 108,000 |

An invalid fit is not counted as use; a wearer who stops using the aid at six months is not counted as active. These are **aid-ears**, not distinct people or proven communication gains. The base 100,000 issued aid-ears would represent at most 0.025% of WHO's >400 million-person context (100,000 ÷ 400 million); the 64,000 active aid-ears are at most 0.016% on that deliberately generous, mismatched comparison. Neither ratio is a true coverage-rate change because the numerator counts ears and the denominator people, and many users are outside the intended category.

**Cost envelope, US dollars per issued aid (planning assumptions):** $65 ex-factory + $8 lower-bound charger allocation + $5/year × 3 years for domes, cleaning and cell replacement = **$88 over three years**. This assumes one full $8 charger allocation per aid even though the charger could be shared; it excludes distribution, training, clinical referrals, taxes, repairs, electricity and trial costs. The original README's approximately $27/aid-year excludes this charger and other omitted costs. Three-year scenario commitments if all issued aids are supported for three years: low 50,000 × $88 = **$4.4 million**; base 100,000 × $88 = **$8.8 million**; high 150,000 × $88 = **$13.2 million**. These are illustrative procurement and consumable budgets, not savings or prices paid by users.

**Abandonment sensitivity at base issuance and valid-fit assumptions:** if six-month continued use falls from 80% to 60% (40% stop using), active aid-ears fall from 80,000 × 80% = **64,000** to 80,000 × 60% = **48,000**; the $8.8 million modeled commitment is unchanged. A fit may also be valid yet fail to improve speech in noise; do not count an active aid as a demonstrated clinical benefit without matched outcome measurement.

## Measurement needed to replace assumptions

Record eligibility and referral exclusions; ear-level issuance, fitting attempts and failures; one- and six-month use; acoustic faults and adverse events; real-ear response; speech recognition in noise; and wearer-reported communication, stratified by language, age and dexterity. Compare with locally available care under appropriate authorization and report both costs and losses to follow-up. Field invoices and returns must test the $65 factory and $5 annual consumable assumptions before any affordability claim. The broader access case depends on affordable ear care, ongoing parts supply and real sustained benefit, not shipments alone.

[1] WHO (2024), [hearing-aid service delivery guidance](https://www.who.int/news/item/01-03-2024-who-issues-guidance-to-improve-access-to-hearing-care-in-low--and-middle-income-settings). Device constraints and targets: [README.md](README.md). US adult OTC indication: [FDA OTC hearing aid guidance](https://www.fda.gov/medical-devices/hearing-aids/otc-hearing-aids-what-you-should-know).
