# Atmospheric Protein Synthesizer — Technical Specification

## 1. System Architecture

### 1.1 Form factor
- **20-ft ISO shipping container**, 6.1 × 2.4 × 2.6 m, insulated, climate-controlled
- **Mass (operating):** ~8,000 kg
- **Input power:** 150 kW peak (electrolysis), 30 kW steady-state (fermentation + downstream)
- **Water input:** 500 L/day make-up (net); 2,000 L/day recirculating
- **Output:** 100 kg/day dry protein product (configurable 50–200 kg/day)

### 1.2 Subsystem breakdown

| Subsystem | Function | Key components |
|-----------|----------|----------------|
| **A. Power & electrolysis** | Generate H₂ and O₂ from water | PEM electrolyzer stack (Nafion 212 membrane, IrO₂ anode, Pt/C cathode), 50 Nm³/h H₂, DC-DC converter, PV/wind/grid input |
| **B. CO₂ capture** | Concentrate atmospheric CO₂ | DAC module — amine-functionalized porous silica sorbent (PEI/SBA-15), 0.5 g CO₂/kg-sorbent/cycle, 120°C desorption, 30 cycles/day, ~5 kg CO₂/h output |
| **C. Nutrient preparation** | Mineral broth from seawater/rock dust | Seawater reverse-osmosis brine concentrate + basalt rock-dust leachate + FeSO₄ + trace metals; sterilization via UV + 0.2 µm filtration |
| **D. Gas-fermentation bioreactor** | Grow *C. necator* on H₂/CO₂/O₂ | 2 × 1,500 L stirred membrane-delivered bioreactors (alternating fill/draw, continuous output), 37°C, pH 6.8–7.2, OD control loop |
| **E. Membrane gas-delivery** | Safe H₂/O₂/CO₂ transfer to liquid | Silicone hollow-fiber modules (3 m² each, 50 µm wall, 200 µm ID), 8 modules/reactor; headspace N₂-blanketed to <2% H₂ (below 4% LEL) |
| **F. Harvest & downstream** | Convert biomass to food product | Disk-stack centrifuge (3,000 G, 500 L/h), thermal kill (75°C, 90 s), twin-screw extruder texturization, spray dryer |
| **G. Nutrient recycle** | Close mineral loop | Hydrothermal liquefaction mini-reactor (280°C, 10 MPa, 10 min), recovers 85% N/P/K/Fe to broth |
| **H. Control & safety** | Autonomous operation | PLC (Siemens S7-1500 or open-source equivalent), H₂ detectors (4 redundant catalytic bead sensors), pressure relief, N₂ inerting auto-activation |

### 1.3 Process parameters

| Parameter | Target | Basis |
|-----------|--------|-------|
| Biomass productivity | 30 g/L/h | Membrane delivery k_La 0.15 s⁻¹ (vs. 0.03 sparged) |
| Cell density | 60–80 g/L | Draw-and-fill continuous, OD-controlled |
| Protein content (dry) | 65–72% | Engineered *C. necator*, storage protein overexpression |
| H₂ utilization | 92–96% | Hollow-fiber delivery, low headspace |
| Energy to protein | 15–25 kWh/kg | Electrolysis 50 kWh/kg H₂; 0.3 g biomass/g H₂ → ~15 kWh/kg biomass minimum; downstream adds ~5 |
| CO₂ to protein | 2.2 kg CO₂/kg protein | Stoichiometric (C₅H₇NO₂ biomass, 53% C) |
| Yield | 0.45 g biomass / g H₂ | *C. necator* chemolithoautotrophic Y_H₂ |

## 2. Organism specification

### 2.1 Base strain
- *Cupriavidus necator* H16 (ATCC 17699) — GRAS-adjacent, history of safe industrial use (Biopolymers, feed), EU novel-food dossier precedent (Solar Foods Solein®).

### 2.2 Genetic modifications

| Modification | Genes / approach | Purpose |
|--------------|-------------------|---------|
| Methionine-rich storage protein | Insert codon-optimized *phaC1*-driven methionine-rich fusion (MBP-tagged) | PDCAAS > 1.0 (wild-type ~0.85, methionine-limited) |
| Lysine boost | Overexpress *lysC* feedback-resistant + *asd* | Lysine exceeds FAO ref |
| B12 biosynthesis | *Salmonella* cob operon cassette (*cobA–cobO*, ~20 genes) under constitutive promoter | 5–15 µg B12/g protein (meets adult RDA at 50g protein/day) |
| Heme-iron | Soy leghemoglobin (*Lba*) + *E. coli hemA-hemH* boost | 8–20 mg heme-Fe/g; matches beef bioavailability |
| Chaperone robustness | GroEL/GroES + DnaK overexpression, σB stress regulon | Tolerates gas-mixture excursions, 4× viable range |
| Biocontainment | Synthetic auxotrophy (Δ*ilvA*, Δ*thyA*) + kill-switch (mazF under lac promoter) | <10⁻⁸ survival outside reactor |

### 2.3 Nutritional output (per 100 g dry product)

| Nutrient | Content | FAO/WHO ref (per 100g adult) |
|----------|---------|------------------------------|
| Protein | 65–70 g | 50 g (RDA) |
| Methionine + cysteine | 2.8 g | 2.5 g |
| Lysine | 6.5 g | 4.5 g |
| B12 | 1.0–1.5 mg | 2.4 µg (RDA) — **>400× RDA** |
| Heme iron | 8–20 mg | 8 mg (RDA) |
| Fat | 8–12 g (PHB, reducible) | — |
| Fiber | 3–5 g (cell wall debris) | 25 g (RDA) |

## 3. Materials & manufacturing

### 3.1 Bill of materials (community unit, 100 kg/day)

| Component | Qty | Unit cost | Total |
|-----------|-----|-----------|-------|
| PEM electrolyzer stack (50 Nm³/h H₂) | 1 | $35,000 | $35,000 |
| DAC CO₂ module (5 kg/h) | 1 | $8,000 | $8,000 |
| Membrane bioreactor (1,500 L, jacketed) | 2 | $6,000 | $12,000 |
| Silicone hollow-fiber gas modules | 16 | $400 | $6,400 |
| Disk-stack centrifuge | 1 | $7,000 | $7,000 |
| Twin-screw extruder | 1 | $5,000 | $5,000 |
| Spray dryer | 1 | $4,000 | $4,000 |
| Hydrothermal liquefaction mini-reactor | 1 | $3,000 | $3,000 |
| PLC + sensors + H₂ safety | 1 | $4,000 | $4,000 |
| Container + insulation + HVAC | 1 | $6,000 | $6,000 |
| Pumps, valves, piping | lot | $4,000 | $4,000 |
| PV array (150 kWp) + battery | 1 | $45,000 | $45,000 |
| **Total** | | | **$139,400** → target **$100K at scale** |

### 3.2 Scaling cost curve
- 100 units: ~$120K each
- 1,000 units: ~$95K each
- 10,000 units: ~$80K each (electrolyzer & membrane dominate, both on steep learning curves)

## 4. Safety

- **H₂ explosion risk**: eliminated by membrane-delivered, sub-LEL gas handling. Redundant H₂ sensors trigger N₂ inerting + auto-shutdown at 2% H₂ headspace.
- **Biological containment**: synthetic auxotrophy (2 auxotrophies) + kill-switch; no environmental persistence.
- **Food safety**: thermal kill (75°C/90s) before any downstream contact; product dry-stable (aw < 0.3), 24-month shelf life at ambient.
- **Pathogen prevention**: closed sterile system, 0.2 µm sterile inlet air, UV broth sterilization.

## 5. Performance benchmarks

| Metric | APS (target) | Beef | Chicken | Soy | Quorn (fungal) | Solar Foods (industrial) |
|--------|-------------|------|---------|-----|----------------|---------------------------|
| Land (m²/kg protein) | 0.15 | 250 | 45 | 12 | 3 | 1 |
| Water (L/kg) | 10–30 | 15,000 | 4,300 | 300 | 1,500 | 100 |
| CO₂-eq (kg/kg) | −1.5 to −2.0 | +60 | +6 | +0.9 | −0.5 | −1.0 |
| Energy (kWh/kg) | 15–25 | 100 | 30 | 8 | 20 | 18 |
| B12 | Yes (native) | Yes | No | No | No | Fortified |
| Heme iron | Yes | Yes | Low | No | No | No |
| Climate-independent | **Yes** | No | No | No | No | Partial (factory) |
| Decentralizable | **Yes** | No | No | No | No | No |

## 6. Deployment scenarios

### 6.1 Dadaab refugee camp, Kenya
- 250,000 residents, arid, no arable land
- 3 APS units (300 kg/day) = protein for 15,000 people daily
- Powered by 450 kWp solar
- Replaces food-aid logistics; dry product stores 24 months

### 6.2 Reykjavík, Iceland
- Geothermal electricity at $0.04/kWh
- 1 unit runs at 200 kg/day (cold climate helps)
- Protein cost: ~$2.5/kg
- Excess capacity for export

### 6.3 Dubai, UAE
- Solar + DAC in desert (high insolation, zero arable land)
- 10 units (1 tonne/day) feeds 50,000 people
- Carbon-negative (−2 tonne CO₂/day)
- Net water use: <30,000 L (vs. ~150M L for equivalent beef)

## 7. Roadmap

| Phase | Years | Milestone |
|-------|-------|-----------|
| **1. Lab validation** | 2026–2028 | Engineered strain (B12, heme, methionine), membrane bioreactor prototype (5 L), 30 g/L/h demonstrated |
| **2. Pilot** | 2028–2030 | 100-L membrane bioreactor, 1 kg/day, food-safety dossier, regulatory novel-food filing |
| **3. Community unit** | 2030–2033 | First 100 kg/day container prototype, 6-month unattended operation, 3 field deployments |
| **4. Scale** | 2033–2038 | 1,000 units deployed; <$100K/unit; protein <$5/kg |
| **5. Ubiquity** | 2038–2045 | 100,000+ units; protein <$3/kg; 500M person-days/year |

## 8. Risks & mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| H₂ safety incident | Low (membrane design) | Critical | Sub-LEL handling, redundant sensors, N₂ inerting, no gas headspace |
| Regulatory (novel food) | Medium | High | Leverage Solar Foods EU precedent; start dossier Phase 2; open data |
| Strain instability | Medium | Medium | Synthetic auxotrophy + kill-switch; master cell bank; genome re-sequencing |
| Public acceptance | Medium | Medium | "From air, not from animals"; transparent process; chef partnerships |
| Electrolyzer cost floor | Medium | Medium | PEM cost falling 18%/yr; alkaline fallback at $400/kW stack |
| Mineral supply (P, Fe) | Low | Medium | Seawater + rock dust sourcing; nutrient recycle loop (85% recovery) |

## 9. Comparison to alternatives

| Approach | Land | Water | CO₂ | Climate-independent | Decentralizable |
|----------|------|-------|-----|---------------------|-----------------|
| **APS** | 0.15 | 10–30 | −1.5 | **Yes** | **Yes** |
| Precision fermentation (industrial) | 1 | 100 | −1.0 | Partial | No |
| Plant protein (soy) | 12 | 300 | +0.9 | No | No |
| Cell-cultured meat | 1 | 50 | +2 | Partial | No |
| Algae photobioreactor | 8 | 200 | −0.5 | Partial | No |
| Animal agriculture | 250 | 15,000 | +60 | No | No |

## 10. Open questions / research frontiers

1. **Can a single organism also produce omega-3 (DHA/EPA)?** — testing *C. necator* + desaturase cassette.
2. **Can the system fix its own N₂ from air** (eliminating mineral N input)? — integrating *nifHDK* into *C. necator* is energy-costly under H₂; explore *Xanthobacter* dual-fixation chassis.
3. **Can product be tuned** to flour, fibrous meat-analog, or vitamin supplement by downstream selection?
4. **Microplastic-free, fully recyclable container materials** — bio-PE insulation, aluminum frame.
5. **Coupling with excess curtailled renewable energy** — when grid has surplus wind/solar, APS ramps up as a flexible demand sink, producing storable dry protein (a form of food-energy storage).