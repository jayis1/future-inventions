# Engineering Specification — Laundry Microfiber Capture Cassette

**Author:** jayis1
**Status:** proposed test plan, not certified plumbing or appliance hardware

## System boundary and feasibility

- Install downstream of the washer's original discharge hose without defeating the maker's specified hose height, air gap or standpipe. A licensed local installer decides whether a particular machine/drain pair is eligible. No drinking-water contact or reuse of filtered laundry water.
- Proposed 500 µm pre-screen and 60 µm fine woven stainless mesh, nominal fine-screen area 0.12 m², polypropylene housing, EPDM seals. At the provisional 20 L/min flow target (0.000333 m³/s), the average gross surface flux is **0.00278 m/s** (flow divided by unfolded mesh area). This is a geometric estimate, not a prediction of pressure drop: pleat blockage, open-area fraction, detergent and fiber mats must be measured.
- Nominal 5 kPa pressure drop corresponds to about **0.51 m water head** (using water density 1000 kg/m³ and g = 9.81 m/s²). That allowance may exceed a given washer's permissible external head; *manufacturer limits override this provisional target*. Qualify a pump by measured pressure, discharge time and thermal cycling before any home trial.
- Capture target ≥70% of discharged synthetic-fiber **mass ≥100 µm length** in predeclared mixed loads, including beginning and end of cleaning interval; separately report counts by polymer and fiber-length band (100–500 µm, 0.5–2 mm, >2 mm), plus smaller detected fibers. Nominal mesh pores do not predict capture of long, thin or deformable fibers.

## Hazards and controls

| Failure | Detection | Required response / test |
|---|---|---|
| Fine screen clogs | Mechanical head flag; longer discharge time | Stop and clean into lidded tray; relief-path activation latches red and counts as untreated discharge |
| Relief also clogs or drain backs up | Standpipe overflow, pump alarm or delayed discharge | Stop washer and isolate water; reject model pairing if safe drainage cannot be demonstrated under injected worst-case lint |
| Seal mis-seated or housing cracks | Visible leak at first rinse and post-service check | Stop washing, repair or replace; no unattended deployment until validated leak-containment protocol |
| User rinses lint into sink | Handling observation / waste audit | Retest tray and pouch usability; no credited capture for fibers returned to wastewater |
| Screen tears or seals age | Inspection and downstream fiber sampling | Replace damaged module; test life with detergent, bleach and repeated cleaning |
| Collected waste mishandled | Sealed-pouch and municipal disposal audit | Do not claim destruction; assess local disposal rules and leakage risk |

## Stage gates (all targets, none demonstrated)

1. **Bench, 50 cycles per candidate washer type:** measure pressure, flow, leakage, discharge duration, pump temperature and relief activation with clean and staged lint-loaded screens. Include deliberate seal misassembly, partial drain blockage and maximum allowed water temperature. Reject if appliance limits, installation rules or flood-control requirements cannot be satisfied; never rely on the provisional 5 kPa value in place of maker limits.
2. **Laboratory capture, randomized paired washes:** at least 30 matched pairs across polyester, acrylic and blended garments with detergent and predeclared wash programs, including clean and end-of-interval screens. Measure polymer-identified mass and count in total discharge with a downstream reference capture method; report uncertainty and contamination blanks. Reject if intention-to-treat ≥100 µm synthetic-fiber mass reduction is below 70% or relief activates in ≥1% of prescribed-service washes.
3. **Home pilot, 100 households for 12 months:** compare with both no filter and a contemporary external filter, predeclare assignment and losses to follow-up. Record actual service hours, leaks, bypasses and residual waste; independent observers audit whether users rinse fibers into drains. Stop trial for attributable pump damage or significant flooding; independently assess lifecycle burden before broader deployment.

Existing filters make the science of basic interception plausible within a 10–15-year product development horizon. The difficult hypothesis is **safe, sustained real-world retention at accessible total cost**, not an unobserved new particle-binding physics.
