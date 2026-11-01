# Locally Repairable Terrain Wheelchair

**Author: jayis1**

**Status:** Research concept (TRL 2); no certified chair or clinical benefit claimed.

## Problem

WHO estimates that 80 million people need a wheelchair and warns that access to an *appropriate* chair and trained fitting is uneven.[1] Imported chairs can be difficult to repair where roads are rough and replacement components are scarce. A cheap frame alone does not solve seating, postural support, fitting, or follow-up; WHO explicitly requires a person-centred provision process.[1]

## Solution

A workshop-buildable, manually propelled wheelchair family uses a common, published mechanical interface for the seat rails, rear axle carriers, front fork mounts, and push handles. A trained wheelchair service chooses a configuration, fits the user and cushion, teaches safe propulsion and transfer, and schedules follow-up. The standard interface lets regional workshops substitute locally sourced bicycle-compatible wheel and bearing sizes without improvising the safety-critical frame joints. The chair is not a universal one-size-fits-all model.

The candidate adult frame uses welded 25 mm outside-diameter mild-steel tube with gusseted axle mounts; replaceable bolted forks, a mechanically indexed rear-axle position, 24-inch spoked pneumatic rear wheels with hand rims, and wider serviceable front wheels selected for local ground conditions. An adjustable textile sling supports a separately fitted pressure-distribution cushion; the cushion is not a substitute for individual pressure-injury assessment. Drain holes, replaceable stainless fasteners, and paint/powder-coat protection support wet-weather servicing. No electronics, accounts, telemetry, or motors are required.

## Key Innovation

Local manufacture and rugged indoor-outdoor wheelchairs are *existing* art: Whirlwind's RoughRider has been manufactured and repaired in Georgia with seating services and user training.[2] This proposal tests a **cross-workshop interchange standard**, rather than claiming to invent rough-terrain wheelchairs: published go/no-go gauges and common replaceable interfaces could permit independently manufactured forks, seat frames, and axle carriers to fit a qualified frame without matched factory tooling. Gauge interoperability and retained strength are unproven. The closest repository items are the neural-adaptive-prosthetic (limb interface) and pressure-witness-insole (diabetic foot); neither provides wheelchair mobility or a repairable frame platform.

## Target Cost

Unquoted 2038 planning target at 10,000 adult chairs/year across regional workshops, in US dollars: steel frame and finish $38; rear wheels/hand rims $34; front wheels/forks/bearings $23; seating textile and fitted cushion allowance $18; brakes/footrests/handles $22; welding, quality checks, packaging $25; workshop overhead and contingency $20. **Ex-workshop total target $180**, with **$220 delivered hardware** target after a separate $40 allowance for distribution and margin. These are hypothetical allocations, not supplier quotations; the $18 cushion allocation may be insufficient for complex seating and must not cap clinical fitting. At $18/year in expected tire, bearing, brake, and upholstery service, the simple five-year hardware-plus-service estimate is **$310** ($220 + 5 × $18), excluding fitting, clinician time, training, user travel, site-specific freight above the distribution allowance, taxes, finance, and replacement after failure. Pilot procurement must quote each item and report total delivered and user-paid cost separately.

## Impact

Planning capacity, *not* measured benefit: 10,000 qualified chairs/year could equip at most 10,000 people/year if every chair is individually appropriate, fitted, accepted, and retained in service. Measure independent use, repair time, abandonment, user-reported participation, pressure injuries, and falls against a locally available appropriate chair plus the same trained fitting and follow-up. No population-wide benefit is inferred from WHO's 80-million-person need estimate.[1]

## Engineering and validation gates

- **Configuration envelope (design hypotheses):** adult user mass up to 100 kg; individually selected seat width 380–500 mm and seat depth 400–500 mm. These are *not* clinical fitting limits or verified safe loads. Child and complex-posture configurations require separate engineering and provision pathways.
- **Mechanical tests:** test every interchangeable interface at its worst-case axle and seat positions for static stability, braking, impact, and fatigue under applicable ISO 7176 parts and local standards before human use. WHO's design guidance identifies strength, durability, stability, brake effectiveness, and context-specific rough-ground use as essential checks.[3] An interface gauge passing does not prove a complete assembled chair is safe.
- **Pilot:** users and trained services co-design a range of sizes and terrain options; compare at least 50 fitted candidates with 50 appropriately fitted existing chairs over 12 months, reporting failures and maintenance as well as benefits. Obtain ethics and local device approval where required. Zero unresolved brake, weld, tip, or retention failures is a release gate, not a prediction.
- **Failure modes:** a loose axle mount can cause a fall; a seized front wheel can pitch a rider; an unsuitable cushion can cause skin damage; a soft tire or worn brake can impair stopping. Require captive locking fasteners, torque marks and periodic inspection, a brake function check before every trip, tire/bearing service instructions, and trained seating review. Remove a damaged chair from service and provide an alternative mobility plan rather than telling a user to keep riding.
- **Horizon:** TRL 2 concept now; aim for interface and destructive-test prototypes within 2–5 years, supervised multi-site service trials within 5–10 years, and only then a qualified interoperable production family (TRL 8 target by 2042). Materials and manufacturing already exist; interoperability, durability, and affordability remain hypotheses.

## Sources

[1] https://www.who.int/news/item/05-06-2023-who-releases-new-wheelchair-provision-guidelines
[2] https://whirlwindwheelchair.org/programs/the-georgia-project
[3] https://www.ncbi.nlm.nih.gov/books/NBK143784

## How It Works

The design is a manually propelled chair, not a motorized climbing device. A fitted rider drives 24-inch rear hand rims; pneumatic tires deform over small irregularities while a selected wide front wheel reduces sinkage on compacted dirt. Neither tire size nor tread makes deep mud, loose sand, stairs, or steep slopes safe. A trained service positions the indexed rear axle to balance reach to the hand rim against rear-tip risk, verifies brake engagement with the actual tires, and fits seat, foot supports, and cushion to the person. Every axle setting is a separate stability test configuration, not an unrestricted adjustment.

The distinctive element is a *published, gauged interface*: a workshop makes a fork or axle carrier to controlled hole-spacing, face-flatness, and retention geometry on a drawing still to be engineered. A second workshop checks it with independent go/no-go gauges; only qualified modules and specified fastener grades enter service. Standard bicycle tires and spokes can be sourced locally where dimensions match, but a bicycle hub is **not** automatically a safe wheelchair axle or hand-rim mount. The frame's welded load path and any damaged safety-critical joint require a trained technician and requalification, never an improvised roadside weld.

A proposed field workflow is: isolate the chair and supply alternative mobility if a brake, axle, fork, or frame is suspect; identify the approved module by its stamped drawing revision; inspect fit with the gauge and mating faces; install with documented torque/retention checks; then perform an unoccupied functional check and a service sign-off before use. A puncture or upholstery tear may be serviced with ordinary tire or sewing tools, but it still triggers inspection for secondary damage. The illustrated repair-time targets below include diagnosis and re-check, not user fitting or travel to a shop.

## Technical Architecture

| Subsystem | Candidate construction and interface | Verification boundary |
| --- | --- | --- |
| Primary structure | Welded 25 mm OD mild-steel tube, gusseted carrier mounts, protective coating and drain holes; wall thickness and weld procedure remain to be specified | Coupon and assembled-frame fatigue, weld inspection, corrosion exposure |
| Running gear | 24-inch spoked pneumatic rear wheels with hand rims; locally selected wider replaceable front wheels and bolted forks | Wheel retention, spoke tension, caster clearance, rolling effort on defined surfaces |
| Adjustment and restraint | Mechanically indexed axle carriers, bolted foot supports, tire-contact parking brakes, captive retention hardware | Worst-case tip angles, brake holding with worn and wet tires, foot/hand clearance |
| Human interface | Adjustable sling plus independently prescribed cushion and posture supports | Individual assessment, pressure-injury prevention plan, transfer and follow-up |
| Repair information | Printed, offline drawing revision; module IDs, material/fastener specification, gauge dimensions and inspection record | Independent workshops produce interchangeable modules that pass whole-chair tests |

The energy path is human effort → hand rim → spoked wheel → tire/ground; the opposing ground reaction passes through hub, axle carrier, frame, and fitted seating. There is no electronics or data collection. Service information instead flows from a revision-controlled paper drawing and parts list to a shop's inspection log and back to the wheelchair service for follow-up. A gauge proves geometry only: destructive tests and full-assembly tests must qualify each supplier/material combination. Steel is chosen for ordinary workshop fabrication, at a likely weight and corrosion penalty versus optimized aluminum; neither penalty has yet been measured. Passenger vehicle restraint, powered assistance, and stair travel are outside this concept's validated scope.

## Performance Benchmarks

**No prototype measurements exist.** The published state of the art already includes locally manufactured rough-terrain chairs such as the RoughRider.[2] The proposed advance is *cross-workshop compatibility*, not an unsubstantiated speed or safety advantage. ISO 7176-1:2014 specifies static-stability measurement, ISO 7176-3:2012 brake-effectiveness measurement, and ISO 7176-8:2014 static, impact and fatigue strength requirements.[4][5][6] Those tests do not alone establish rough-ground safety or clinical appropriateness.

| Metric | Current/reference state | Engineering target (unverified) | Test condition |
| --- | --- | --- | --- |
| Interchangeability | RoughRider demonstrates local production and repair; independent cross-shop fit not established here[2] | Modules from 3 independent shops pass the same gauges **and** full-chair strength/stability tests | Same drawing revision; worst-case axle/seat setting and approved load dummy |
| Static stability and braking | No matched numerical baseline available | Report all measured tip angles and brake results under ISO 7176-1/-3; meet applicable requirements before user trials | 100 kg design-hypothesis user represented by an appropriate test dummy, empty and loaded accessory configurations; dry and wet tire checks |
| Strength and service life | No independently comparable results gathered | Pass applicable ISO 7176-8 tests after module swaps, with no critical failure | Qualified frame and each fork/carrier supplier combination; document failures and cycles under the standard |
| Field service | No observed repair-time distribution yet | Median tire/spoke service ≤2 hours; qualified bolt-on fork exchange ≤4 hours after part arrival | Trained technician, documented tools and spare in hand; record diagnosis through sign-off |
| Total hardware cost | No like-for-like quoted competitor baseline | $220 delivered hardware and $310 five-year hardware plus routine service, per hypothetical allocation above | 10,000 units/year planning case; report fitting and transport separately |

Before claiming superiority, test an appropriately fitted locally available chair with the same rider-mass dummy, tire inflation, rough-ground course, maintenance regime, and service support. Measure propulsion effort, tip events, repair downtime, mass, and total cost; report confidence intervals and adverse events rather than selecting only favorable outcomes.

## Deployment Scenarios

1. **Rural district rehabilitation service:** on compacted tracks and seasonal ruts, a trained provider fits the chair and teaches transfers; a bicycle workshop stocks matched tires/spokes while a qualified wheelchair shop holds gauged forks. The user needs an alternative route or chair when mud makes a trip unsafe. Follow-up checks skin, tire wear, and repairs, not merely whether the chair was delivered.
2. **Post-disaster repair network:** a clinic and local metalworking cooperative inventory drawing revisions and certified replacement modules for already-fitted users. A bent fork can be exchanged at a staffed service point; an unverified welded frame is retired. The main bottlenecks are individual fitting, reliable spares, and continued service after the initial donation.
3. **Peri-urban mobility programme:** broken pavement, curb cuts, and rain test caster wear and brake contamination. A wheelchair technician assesses fit and hand-rim reach; participating workshops perform documented tire and upholstery service. An accessible route assessment remains necessary: the chair is not a substitute for usable infrastructure.

## Risks & Mitigations

| Risk | Mitigation and stop condition |
| --- | --- |
| Rear or sideways tipping; transfers shift the centre of mass | Test every axle/seat/load combination for static stability and controlled obstacle/brake behavior without occupants first; train users; do not prescribe an untested setting. |
| Brake wear, wet tires, seized caster, or loose axle | Pre-trip function check, periodic torque/retention marks, wheel inspection and technician sign-off; remove from service on failed holding, steering, or retention checks. |
| Fatigue cracks, rust, variable steel or field welds | Specify steel and weld procedure, inspect coating and joints, fatigue-test supplier combinations; reject cracked or undocumented structural parts rather than patching in the field. |
| Poor fit, hard seating, hand strain or pressure injury | Individual assessment, appropriate cushion and propulsion training, scheduled follow-up and adverse-event reporting under WHO's person-centred provision guidance.[1][3] |
| Nominally matching but weak replacement modules | Revision-controlled drawings, material traceability, approved fasteners, gauges plus destructive qualification; a dimensional pass alone is never a safety certificate. |
| $18 cushion allowance and $220 hardware target underfund service | Quote seating, fitting, transport and follow-up separately; do not deploy where adequate clinical service cannot be financed. |
| Regulatory and procurement mismatch | Confirm local device classification, applicable standards, ethics review and incident reporting before pilot distribution; do not call a concept certified. |

## Vision for 2050

Imagine a region where wheelchair service teams can order a compatible fork from several qualified local workshops, while a neighborhood bicycle mechanic handles the ordinary tire and spoke work. Open drawings and low-cost gauges would make supply less dependent on one factory; a documented service record would help a chair be refurbished and refitted for another person only after inspection and individual assessment. This is a possible infrastructure outcome, not a 2050 adoption forecast. The measure of success is not how many frames were made but how many people retain an appropriate, safe mobility option with a reachable repair service.

### Additional sources

[4] ISO 7176-1:2014, static stability: https://www.iso.org/standard/56817.html
[5] ISO 7176-3:2012, effectiveness of brakes: https://www.iso.org/standard/53816.html
[6] ISO 7176-8:2014, static, impact and fatigue strengths: https://www.iso.org/standard/64902.html
