# Battery Depowering Cabinet — Research Specification

**Author: jayis1** · **117** · Prototype study only; not an operating manual or safety certification.

## Scope and physical principle

A trained collector processes one eligible *intact, labelled, rechargeable lithium-ion pack* at a time. The electric circuit moves stored energy into a fused resistor (Joule heating, E ≈ ∫V I dt); a dedicated heat sink and engineered enclosure reject that heat to the environment. It never attempts metal recovery or claims to neutralize electrolyte. A recycler may not require discharge at all; compare the cabinet against terminal isolation and direct certified shipment before deployment.

```text
Staffed intake -> visual/label gate -> keyed removable carrier -> isolated bay
                 | fail/reject                            | fused DC load -> heat sink
                 v                                        | independent voltage/thermal monitors
     separate DDR pathway / trained response              v
                                            stop + operator review -> insulated terminals
                                                          -> approved recycler container
```

## Design envelope and quantitative feasibility

- Initial research envelope: labelled 3.6–14.8 V nominal, ≤50 Wh packs with safe external terminals and manufacturer/recycler approval. Unknown packs are rejected. At maximum stored energy, 50 Wh = 180 kJ; a nominal 25 W average load would need **at least 2 hours** in the ideal full-energy case, not including taper or review. This is a heat-management requirement, not a throughput guarantee.
- With 25 W continuous average heat over two hours, reject 180 kJ; the enclosure and ventilation must be qualified for that thermal load **plus fault conditions**. No promise that normal ventilation survives a cell thermal event. Cabinet fire strategy requires independent fire engineering and local authority sign-off.
- The planned throughput of 100 accepted packs/site/month assumes staffed time, repeatable carrier fit and recycler acceptance; it is an adoption scenario rather than measured performance.
- No fixed end-of-discharge voltage is published here: chemistries, cell count, pack electronics and recycler rules vary. A validated pack-specific profile must set current, time, voltage thresholds and an explicit reject outcome; open-circuit voltage alone cannot prove a pack is safe to transport.

## Independent barriers and safe states

| Fault | Detection | Required state / residual risk |
|---|---|---|
| Unlabelled, wrong chemistry, swollen, leaking, hot, recalled, or damaged pack | Trained intake examination plus label and terminal match | No electrical connection; isolate via approved DDR process. Internal defects may be invisible. |
| Overcurrent, short or reversed leads | Physical keyed adapter, polarity test, fuse and independent current monitor | Do not close contactor or open it; fuse is last electrical barrier. Arcing risk requires testing. |
| Overheating or sensor disagreement | Two separately powered thermal channels on carrier and bay, plausibility check | Open contactor, alert operator, keep bay controlled; cell runaway can continue with power removed. |
| Ventilation loss, mains failure or watchdog fault | Airflow proving and supervised control supply | Normally open contactor drops out; controlled emergency response. Lost ventilation may trap heat. |
| Contactor weld | Independent load-current measurement after stop, upstream manual isolation | Flag unsafe fault, prohibit access and call qualified responder; the contactor alone is not a sufficient barrier. |
| Wrong carrier or worn contact | Mechanical key, insertion check, scheduled resistance/contact inspection | No start, repair or replace carrier before use. |
| Apparently completed discharge | Independent post-run measurement and operator signoff | Insulate terminals and use compliant packaging; no safe/nonhazardous certificate. |

A prototype must be bench-tested with simulated electrical/thermal faults and instrumented surrogate loads **before any battery trial**. Trials with real packs require a fire-engineered site, trained staff, regulated shipment pathway, and written emergency plan. Reject states, near misses and false clearances must be logged without consumer-identifying information. The stop criterion for the research program is any uncontrolled heat event, false accepted damaged pack, or inability to demonstrate a risk advantage over collection-only controls.

## Material and lifecycle plan

Powder-coated steel outer shell, replaceable ceramic-fiber-free mineral insulation selected by a fire engineer, nonconductive polypropylene carrier, fused resistor assembly, field-replaceable contactor and sensors. Avoid claiming the shell is fireproof: high-energy failure and toxic smoke require an engineered site response. Repair parts should be obtainable without proprietary cloud software; recycle electronics and steel conventionally. Do not shred or open batteries at the cabinet. Ship all accepted and rejected packs under the applicable local requirements to an authorized battery destination, using separate damaged-battery procedures when required.

## Development horizon

Bench feasibility and quantitative hazard comparison first; only if the supervised design beats collection-only controls should certification, local approvals and small-site pilots be pursued. A 10–20 year route to broader use is plausible if reliable heterogeneous-pack rejection, fire safety and affordable servicing are demonstrated, but none is yet demonstrated. No patent novelty or regulatory approval is claimed.

## Sources

EPA battery recycling and handling guidance: https://www.epa.gov/hw/lithium-ion-battery-recycling-frequently-asked-questions
