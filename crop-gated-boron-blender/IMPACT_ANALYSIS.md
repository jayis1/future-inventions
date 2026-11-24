# Crop-Gated Boron Blender — Impact Analysis

**Author: jayis1** · Scenario arithmetic, not measured benefit or a deployment forecast.

## Basis and boundaries

The README proposes a 1 m³/day unit operating 200 days/year and an illustrative feed of 1.5 mg elemental B/L, treated stream of 0.6 mg-B/L and 1.0 mg-B/L *locally authorized* mixed-water ceiling. FAO's boron interpretation is general, not a field approval; EC/SAR and soil conditions are independent constraints.[1] NMDG adsorption and regeneration are known methods, but breakthrough and waste yields are feed- and operation-dependent.[2] No prototype, yield response, delivered price or environmental advantage has been measured.

Let N be installed units, u the fraction of nameplate volume passing all release criteria, f the treated volume fraction, and V = N × 1 m³/day × 200 days/year × u. For the example concentrations, `(1.5 − 1.0) / (1.5 − 0.6) = 0.556` is the *minimum planning* treated fraction; use `f = 0.60` as a conservative illustrative valve setting, subject to measured mixed-batch release. The ideal mixed concentration is `0.60 × 0.6 + 0.40 × 1.5 = 0.96 mg-B/L`. This 0.04 mg/L margin may be smaller than assay and mixing uncertainty, so passing cannot be inferred from the setting alone.

## Scenarios (illustrative, not predictions)

| Case | Units N | Qualified fraction u | Qualified delivery V | Resin-stream throughput at f = 0.60 |
| --- | ---: | ---: | ---: | ---: |
| Contained trial | 1 | 50% | 100 m³/year | 60 m³/year |
| Cooperative network | 100 | 75% | 15,000 m³/year | 9,000 m³/year |
| Broad conditional rollout | 1,000 | 80% | 160,000 m³/year | 96,000 m³/year |

The 1,000-unit nameplate ceiling is 200,000 m³/year; rejection, outage and unsuitable feed lower actual qualified volume. At 0.96 mg-B/L, each cubic metre carries 0.96 g B into irrigation; the entire 160,000 m³ broad scenario would deliver 154 kg B/year to fields if all batches matched the ideal setting. That is *loading*, not avoided pollution: soil retention, drainage, crop uptake and leaching require site-specific measurements. At 0.60 treated fraction, theoretical adsorption is `(1.5 − 0.6) mg/L × 0.60 m³ × 1,000 L/m³ = 540 mg B` removed per qualified cubic metre, before startup losses and cartridge breakthrough. The broad case would therefore transfer an illustrative 86.4 kg B/year into resin/regenerant streams *for qualified output alone* under these exact assumptions; processing rejected batches adds further waste. A compliant disposal route is essential, not optional.

## Cost and decision thresholds

The US$850 per unit figure is an **unquoted 2038 ex-workshop target**, not a current market price.[README](README.md) At 1,000 units the simple hardware-only multiplication is US$850,000, excluding installation, testing, labor, energy, cartridges, transport, regenerant treatment and disposal. For an illustrative five-year straight-line allocation with no financing or salvage, one unit incurs US$170/year in hardware alone: US$0.85/m³ at 200 m³/year or US$1.70/m³ at 100 m³/year *before any operating cost*. These are scenario inputs, not prices. Full delivered cost must include all released and rejected batches and compare with maintained full-flow resin treatment on the same source, crop specification and season. If daily laboratory testing or licensed disposal makes qualified water more costly, the proposed advantage disappears.

## Uncertainty and adverse effects

V scales directly with qualified fraction u: halving u halves delivery while fixed hardware cost per qualified cubic metre doubles. Required f rises when resin outlet boron rises; if it exceeds the crop limit, no blend of that outlet and higher-boron feed can pass. Other contaminants, EC/SAR failures, soil accumulation, or a crop rotation to a more sensitive variety can reduce u to zero. Wrong batch identity or physical bypass creates harmful releases even if arithmetic and assays are correct. Regeneration moves boron into concentrated waste rather than destroying it; chemical use, transport, energy and leakage must be inventoried in pilot life-cycle accounting. No yield gain, saved hectares, net water saving or emissions reduction is credited until matched field evidence exists.

## Sources

[1] https://www.fao.org/4/x5871e/x5871e07.htm — FAO, water quality and crop production.
[2] https://pmc.ncbi.nlm.nih.gov/articles/PMC9517912/ — Liu et al. (2022), boron-removal technologies.
