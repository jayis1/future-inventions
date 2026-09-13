# Circular PCB Electrorefinery

> A containerized, closed-loop microfactory that separates printed circuit boards and recovers their copper, tin, gold, silver, palladium, glass, and polymers without smelting or exported toxic waste.

## Problem

Discarded electronics are one of the world's fastest-growing waste streams. More than 60 million tonnes of e-waste are generated each year, yet only a minority is formally collected and recycled.

Printed circuit boards (PCBs) are especially difficult:

- They laminate valuable metals into glass-fiber-reinforced epoxy and mix copper, tin, nickel, gold, silver, and palladium at millimeter scales.
- Informal recovery by burning, open acid leaching, or crude heating exposes workers and nearby communities to lead, brominated compounds, corrosive fumes, and contaminated wastewater.
- Centralized smelters can recover valuable metals, but their scale and transport requirements leave many regions dependent on export or unsafe backyard processing.
- Conventional shredding mixes materials into fine particles, lowers product purity, and makes glass fiber and resin difficult to reuse.
- Electronics contain richer metal concentrations than many mined ores, while mining and refining replacement metals consume land, water, and energy.

A safe recycling system must work near the waste source, retain its chemicals, produce auditable material outputs, and be affordable to cooperatives and municipalities rather than only multinational smelters.

## Solution

The **Circular PCB Electrorefinery (CPE)** is a modular microfactory for depopulated and component-bearing circuit boards. It combines selective physical liberation with reusable aqueous chemistry and potential-stepped electrochemical recovery.

The process has five stages:

1. **Component liberation:** boards are heated to **120–180°C** under nitrogen or filtered low-oxygen air while pulsed mechanical flexure and localized induction heating soften solder joints. Components fall away intact enough for testing, direct reuse, or separate battery/magnet processing.
2. **Electrohydraulic delamination:** submerged microsecond pressure pulses propagate along copper-epoxy interfaces, peeling foil and traces from the glass-fiber laminate with far fewer fines than rotary shredding.
3. **Closed-loop selective leaching:** liberated metal fractions move through sequential, oxygen-regenerated **glycine**, **citrate**, and **thiosulfate** loops. pH, redox potential, and ligand concentration are tuned to dissolve base and precious metals in separate campaigns.
4. **Potential-stepped electrowinning:** flow-through carbon-felt and stainless cathodes recover copper, tin, nickel, silver, and gold in discrete voltage windows. Ion-selective membrane cells prevent co-deposition and regenerate leachant oxidants at the counterelectrode.
5. **Materials finishing:** cleaned glass fiber becomes filler for geopolymer panels; brominated epoxy is converted in a sealed **350–450°C** low-temperature solvolysis unit into reusable aromatic oil and a bromide-rich aqueous stream that is crystallized for controlled industrial reuse.

The entire liquid inventory remains inside double-contained tanks. Conductivity, pH, oxidation-reduction potential, dissolved-metal sensors, and mass balance software prevent discharge when the metal balance does not close.

## How It Works

### 1. Feed acceptance and hazard isolation

Machine vision and X-ray fluorescence identify board class and flag mercury switches, batteries, large capacitors, beryllium-containing parts, and radioactive or unknown devices for specialist handling. The system records each accepted batch by mass, not by personal or device data.

### 2. Preserve value before grinding

A low-speed flexure bed bends warmed boards while induction loops concentrate heat in solder-rich regions. This removes chips, connectors, and heat sinks before destructive processing. Reusable components can carry more value than their constituent metals, so the refinery prioritizes reuse over dissolution.

### 3. Delaminate at interfaces

Electrohydraulic spark gaps discharge **0.5–3 kJ** pulses into a water-filled chamber. Shock waves reflect differently at copper, epoxy, and glass interfaces, opening laminated boundaries. Screened fractions separate copper-rich foil, solder-rich particles, components, and glass-epoxy flakes without producing respirable dry dust.

### 4. Dissolve selectively in reusable loops

A mildly alkaline glycine loop first complexes copper and nickel. Citrate chemistry mobilizes tin under controlled oxidation. A separate thiosulfate-ammonia-free ligand loop treats the small precious-metal-rich residue. Oxygen or electrochemically regenerated ferric mediator supplies oxidation; no aqua regia or cyanide is used.

### 5. Plate saleable metals and regenerate chemistry

The dissolved streams pass through a cascade of electrowinning cells. Cathode potential and residence time are adjusted from sensor measurements, allowing metals to plate sequentially rather than as a mixed sludge. Bipolar and ion-exchange membranes return pH and oxidant gradients to the leach tanks, reducing reagent replacement.

### 6. Close the material balance

Every batch must reconcile feed mass against reusable components, plated metals, mineral filler, recovered organics, salts, filters, and retained process inventory. A sealed residue cassette captures the small non-recoverable fraction for licensed disposal.

## Technical Architecture

### Physical plant

The 100 kg/day refinery occupies a 12 m high-cube process container and a covered receiving bay. Fire-rated partitions divide it into a dry feed cell, a wet high-voltage liberation cell, three chemically isolated leach/electrowinning loops, and a negative-pressure residue-finishing cell. A secondary-containment floor holds at least **110% of the largest tank plus 10 minutes of fire-water input**. Wetted parts use HDPE, PVDF, titanium, 316L stainless steel, or compatible elastomers selected for each loop.

The modular hardware consists of:

- **Feed and assay module:** guarded depowering station, residual-voltage tester, interlocked XRF, machine vision, scales, and hazard quarantine.
- **Component-recovery module:** nitrogen-recirculating induction chamber, flexure bed, condensate train, HEPA filtration, alkaline scrubber, and component tester.
- **Liberation module:** pulsed-power cabinet, submerged spark vessel, hydrocyclone, screens, eddy-current separator, and ceramic water filter.
- **Three wet-process skids:** independently bunded glycine, citrate, and thiosulfate tanks with pumps, heat exchangers, filters, dissolved-metal sensing, and dedicated electrowinning cassettes.
- **Finishing module:** cathode stripping, glass washing, optional sealed resin conversion, bromide capture, and serialized residue cassettes.
- **Utility spine:** deionized-water polisher, nitrogen generator, ventilation, heat recovery, DC bus, uninterruptible controls, and optional **30–60 kWh** battery for safe shutdown rather than full production.

### Material and data flow

```text
Board batch -> depower/XRF -> component recovery -> wet delamination
                 |                 |                    |
          process passport   tested components    Cu/Sn/PM/glass fractions
                                                       |
                          isolated leach loops -> electrowinning -> products
                                                       |
                                    regenerated ligands/water <- polishing
```

A safety PLC owns pumps, heaters, XRF shutters, pulse power, gas valves, and containment interlocks; a separate supervisory computer optimizes recipes but cannot override safe limits. Tank load cells, inline pH/ORP/conductivity, periodic XRF or ICP assays, coulomb counting, and product scales update a batch **digital material passport**. The control model predicts dissolved inventory from assay and electric charge, then compares it with direct measurements. A discrepancy outside the validated uncertainty freezes product release and liquid transfer.

No cloud link is required to operate. Signed, append-only batch records can be exported to producer-responsibility auditors, while serial numbers or data from source devices are excluded. Regional service hubs receive only equipment diagnostics, certified mass flows, and sealed consumable identifiers.

## Key Innovation

CPE's key innovation is **interface-first liberation coupled to electrochemically regenerated, potential-stepped recovery**.

Today's small recyclers often shred first and then try to separate a contaminated powder. CPE instead exploits the physical interfaces deliberately manufactured into every PCB. Warm flexure releases components; underwater shock waves split metal from laminate; only then does chemistry act on concentrated fractions.

That sequencing provides three advantages:

- **Higher-value recovery:** functioning components are preserved before materials recycling.
- **Lower chemical demand:** selective fractions expose more metal surface area while carrying less epoxy and glass into leach tanks.
- **Closed-loop chemistry:** electrowinning recovers metals and regenerates oxidants and pH gradients in the same electrical cycle.

The result is a refinery that behaves like a materials printer in reverse: it deconstructs a complex manufactured object into specified streams without a furnace, open acid vats, or uncontrolled wastewater.

## Target Cost

### Community module: 100 kg PCB/day

- **Capital cost at 10,000-unit production:** **$140,000–260,000**
- **Footprint:** one 12 m container plus covered sorting area
- **Electricity:** **1.5–3.5 kWh/kg PCB**, compatible with a grid or solar-plus-storage microgrid
- **Fresh water:** **<0.5 L/kg**, mainly replacing drag-out and evaporation losses
- **Net reagent makeup:** **20–80 g/kg PCB**, with **>95%** process-water recirculation
- **Operating cost:** **$0.80–1.80/kg** before recovered-material revenue
- **Target net margin:** **$1–5/kg**, highly dependent on board grade and successful component reuse

### Cooperative module: 20 kg PCB/day

- **Capital cost:** **$35,000–70,000**
- **Staffing:** two trained operators per shift
- **Service model:** sealed reagent and residue cassettes exchanged through a regional hub

No economic case assumes all e-waste has high-grade telecom-board value. Low-grade batches are priced and routed separately, and recovered-value estimates are based on measured XRF composition before acceptance.

## Quantitative Targets

| Metric | Target |
|---|---:|
| Copper recovery | **>97%** |
| Tin recovery | **>95%** |
| Gold and silver recovery | **>95%** |
| Palladium recovery | **>90%** |
| Components removed before comminution | **>80% by count** for accessible packages |
| Reusable components surviving removal | **>60%** after electrical screening |
| Process-water recirculation | **>95%** |
| Liquid effluent during normal operation | **Zero** |
| Material mass balance closure | **>99%** per batch |
| Non-recoverable hazardous residue | **<3% of feed mass** |
| Brominated organic destruction or capture | **>99.9%** |

These are development targets, not claims of demonstrated integrated performance.

## Performance Benchmarks

The comparison below defines engineering gates for a future integrated pilot. Conventional performance varies with feed grade and plant configuration, so ranges are baselines—not claims that every incumbent process performs identically.

| Measure | Informal burning/open leaching | Central shredding + smelting or specialist hydrometallurgy | CPE pilot target |
|---|---:|---:|---:|
| Cu recovery from accepted PCB feed | **30–80%** | **90–98%** | **>97%** |
| Au/Ag recovery | **20–70%** | **90–99%** | **>95%** |
| Pd recovery | usually uncontrolled | **80–95%** | **>90%** |
| Reusable component preservation | typically **<5%** | typically **<5%** after shredding | **>60%** of accessible removed parts pass screening |
| Specific process electricity | poorly measured; combustion often supplies heat | roughly **1–5 kWh/kg PCB**, excluding transport | **1.5–3.5 kWh/kg PCB** |
| Fresh-water demand | uncontrolled and often discharged | site-dependent, often multi-pass treatment | **<0.5 L/kg** makeup |
| Routine liquid discharge | common | treated discharge or off-site treatment | **zero** |
| Fine fraction below 100 µm | high with aggressive milling | commonly material-dependent | **<10% of feed** |
| Audited batch mass closure | absent | plant-level accounting | **>99% per batch** |

Success is not metal recovery alone. A 12-month pilot must sustain the targets across at least **20 representative PCB classes**, close **100 consecutive batch balances**, keep occupational Pb, mist, halogen, dust, hydrogen, and noise exposures below local limits, and demonstrate **>90% availability** excluding scheduled service. Product purity gates are **>99.5% Cu**, **>98% Sn**, and a precious-metal concentrate acceptable to a certified regional refiner.

## Deployment Scenarios

### Repair-cooperative hub in a major city

A network of repair shops sends depowered boards to one 20 kg/day cooperative module. The refinery pays separately for reusable packages and assayed material content; the shops retain repairable devices rather than being rewarded for destruction. Two operators run one shift, while a regional laboratory verifies product and exposure samples monthly. Sealed ligand, filter, and residue cassettes leave on the same vehicles that deliver replacement supplies.

### Island or remote regional materials utility

A 100 kg/day unit consolidates PCB waste that would otherwise be stockpiled or exported at high cost. A solar-plus-storage microgrid supplies daytime batch loads, but the unit pauses safely when power is scarce. Copper and washed mineral filler serve local manufacturers where certified; precious-metal concentrate and nonconforming residues travel in dense, tracked shipments to specialist refiners, replacing export of whole low-density boards.

### Producer-owned reverse-logistics center

An electronics maker installs several modules beside a returns warehouse. Machine-readable design records create model-specific removal recipes, raising intact component yield and reducing assay uncertainty. Requalified connectors, heat sinks, and chips re-enter service parts; plated copper and precious-metal concentrate return through contracted refiners. Audited batch passports support extended-producer-responsibility reporting without exposing customer data.

## Impact

- **Public health:** Replaces open burning and uncontrolled acid extraction with enclosed, monitored processes, reducing worker and community exposure to lead, corrosive mist, brominated smoke, and metal-laden wastewater.
- **Circular materials:** Returns high-purity copper, tin, gold, silver, and palladium to manufacturing and preserves reusable chips and connectors before material destruction.
- **Climate and land:** Reduces demand for primary mining and long-distance shipment of low-density electronic scrap. Lifecycle targets are **60–85% lower greenhouse emissions** than producing the same recovered metals from primary ores.
- **Economic inclusion:** Gives existing repair shops, waste-picker cooperatives, and municipalities a path into formal, higher-value recycling with training, PPE, and verified outputs.
- **Regional resilience:** Creates distributed sources of critical manufacturing metals without requiring every country to build a large smelter.
- **Accountability:** Batch-level mass balance and sealed residue logistics make hidden dumping harder and enable extended-producer-responsibility payments based on verified recovery.

At one million 100 kg/day modules operating 300 days per year, nominal capacity would exceed present PCB waste generation; practical deployment would therefore be constrained by actual regional feedstock and should scale only with audited collection. The goal is not maximum machine count, but universal access to safe recovery wherever electronics are discarded.

## Risks & Mitigations

### Variable feed composition

Board chemistry changes by device age and class, and a fixed recipe can contaminate product streams.

**Mitigation:** XRF-based batch characterization, conservative blending limits, recipe libraries, and automatic diversion of incompatible feed.

### Hazardous components entering the line

Batteries, mercury devices, and charged capacitors can cause fires or contamination.

**Mitigation:** mandatory front-end screening, voltage checks, puncture-resistant quarantine boxes, and interlocked rejection gates.

### Ligand degradation and wastewater leakage

Organic ligands eventually degrade, and even mild leachants become hazardous after metal loading.

**Mitigation:** double containment, leak sumps, total-organic-carbon tracking, activated-carbon polishing, and sealed periodic bleed treatment at regional hubs.

### Brominated resin byproducts

Poorly controlled heating can create toxic brominated emissions.

**Mitigation:** keep initial desoldering below decomposition temperatures; run resin conversion only in oxygen-starved sealed equipment with rapid quench, alkaline bromide capture, activated-carbon guard beds, and continuous halogen monitoring.

### Misleading recovery economics

Precious-metal-rich boards can subsidize low-grade feed, but average values vary widely.

**Mitigation:** publish batch assays, separate service fees from commodity revenue, and require producer-responsibility payments for feed that cannot pay for its own safe treatment.

## 10–20 Year Feasibility

Every major operation has a laboratory or industrial precedent: automated desoldering, induction heating, electrohydraulic fragmentation, amino-acid and thiosulfate leaching, membrane electrodialysis, electrowinning, XRF sorting, and polymer solvolysis. The frontier work is integrating them into a small, robust, chemically closed appliance and proving reliable separation across heterogeneous boards.

A plausible development path is:

1. Pilot interface-first liberation and copper/tin recovery on one standardized board family.
2. Add precious-metal residue processing and automated electrolyte regeneration.
3. Validate worker exposure, emissions, mass balance, and product purity with independent laboratories.
4. Deploy supervised regional pilots with repair cooperatives and producer-responsibility programs.
5. Standardize sealed consumable logistics and certify modular plants for widespread operation.

CPE is designed to complement repair, reuse, and large specialist refineries—not to justify shorter device lifetimes or unsafe treatment of every electronic product in one box.

## Vision for 2050

By 2050, circuit boards carry standardized material passports and release features designed for automated depopulation. Every metro region—and many remote regions—has access to a certified electrorefinery through a repair cooperative, municipal utility, or producer take-back network. Boards are routed first to repair and harvesting; only irreparable material enters chemical recovery.

The distributed plants do not replace specialist smelters and precious-metal refiners. They replace unsafe first-mile processing: concentrating valuable outputs near the waste source, retaining hazardous inventory, and shipping only dense products or sealed residues. Open burning and backyard acid baths become economically obsolete because formal cooperatives can recover more value while providing safer skilled work.

The larger shift is informational. Manufacturers buy verified secondary copper, tin, gold, silver, and palladium through batch passports that account for every input and residue. Design teams see which assemblies resist separation and redesign them. Electronics cease to be anonymous hazardous waste and become a traceable urban ore reserve—locally harvested, repeatedly refined, and never accepted as somebody else's pollution.
