# Flood-Isolating DC Spur — Impact Analysis

**Author: jayis1** · Scenario model, not measured impact or a safety claim. The 1.81 billion flood-exposed people cited in [README.md](README.md) are not an addressable-market estimate.

## Boundary and baseline

One site has two nonessential, isolated 24 V DC spurs (≤4 A each) on an elevated supply. Compare (A) ordinary elevated distribution with coordinated branch protection and sealed low wiring with (B) the same plus two dry-side latched disconnects and two witness cartridges. No medical, evacuation or mains loads; no injury/death or uptime benefit is assumed. Horizon: 10 years, undiscounted US dollars; one module/site. Prices and event rates below are **illustrative assumptions**, not quotations or observed rates. Flood survey, supply, cable, approvals, installation beyond the stated allowance, damaged outlets and disposal charges are excluded from both cases; verify these before investment.

## Explicit cost assumptions

| Item per site | A: baseline | B: proposal | Basis |
| --- | ---: | ---: | --- |
| Initial installed incremental assembly allowance | $120 | $110 ex-workshop module + $90 installation = $200 | Hypothetical; $110 is README target for two-spur module, not a quote |
| Annual inspection | $10 | $20 | Assumed qualified-service allowance, excludes travel |
| Cartridge replacement following event | n/a | 0.1 events/year × ($8 cartridge + $40 labor) = $4.80/year | Assumed event rate and labor; 0.1 is not a flood forecast |
| Ten-year total before repairs | $220 | $448 | $120 + 10×$10; $200 + 10×($20+$4.80) |

Thus **incremental cost = $228/site over 10 years** ($80 upfront + $14.80/year × 10). A 50-site pilot would cost an illustrative $11,400 more than baseline; 10,000 sites would cost $2.28 million more, before qualification, training, financing and excluded work. At $300 avoided *incremental repair expense* per effectively prevented event (assumption), break-even is $228/$300 = **0.76 effective events/site over ten years**, or **0.076/year**; 10,000 sites require 7,600 such events to break even. Count a damaged branch's avoided repair only once, not again as an outage or safety saving. Restoration still requires inspection and perhaps cable/outlet replacement, so $300 may greatly overstate avoidable cost.

## Sensitivity, not prediction

Let `p` be baseline qualifying wet-damage events per site-year, `e` the fraction whose $300 repair is actually avoided by B, and `n` additional nuisance-trip cost per site-year. Then ten-year incremental net cost = `$228 − 10 × p × e × $300 + 10 × n`. At illustrative `p = 0.1` and `e = 0.5`, avoided repair is $150, leaving **$78 net extra cost** with `n = 0`; at `e = 0`, all $228 remains. Even `p = 0.1, e = 1` yields only $72 net savings before nuisance trips. At `n = $10/year`, the break-even effective-event rate rises to ($228+$100)/($300×10) = **0.1093/year**. These are assumed bounds, not confidence intervals; pilot evidence must estimate event frequency, detection effectiveness, false trips and labor independently.

Additional material: a module uses two DC-rated disconnects, enclosure, controller and two disposable cartridges; exact mass, embodied emissions, recycling yield and life are unknown, so no carbon benefit is estimated. Collect actual steel/copper/electronics mass and qualified waste-disposal costs in the pilot. A false trip may remove essential service if misapplied; this design is explicitly excluded from those circuits. Independent electrical testing, certification where applicable, and flood-response procedures remain prerequisites, not monetized benefits.
