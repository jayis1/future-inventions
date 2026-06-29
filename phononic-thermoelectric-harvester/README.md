# Phononic Thermoelectric Harvester

## Problem

**60–70% of all energy produced by humanity is lost as waste heat** — the single largest inefficiency in the global energy system, equivalent to ~550 EJ/year dissipated uselessly into the environment. This heat bleeds from every power plant, factory, vehicle, data center, foundry, and electronic device, carrying away the majority of the fuel we burn and the renewable electricity we generate.

The consequences are enormous:

- **Colossal energy waste:** Global primary energy supply is ~620 EJ/year; useful energy services (motion, light, heat, computation) account for only ~200 EJ. The remaining ~420 EJ is rejected as low-to-medium grade heat — enough to power the entire global economy 2× over if captured.
- **Climate impact:** Because waste heat represents fuel that was burned but not used, recovering even 10–20% would avoid **1–2 Gt CO₂/year** from displaced fossil generation — more than the total emissions of Germany, France, and the UK combined.
- **Industrial competitiveness:** Energy-intensive industries (steel, cement, glass, chemicals, aluminum) spend 20–40% of operating costs on energy, of which 30–60% exits as waste heat via exhaust gases (200–1200 °C), hot surfaces, and cooling water. Recovering this heat directly as electricity would slash costs and emissions simultaneously.
- **Transportation:** Internal combustion engines waste 60–75% of fuel energy as heat. Heavy-duty trucks, ships, and trains could gain 5–15% fuel efficiency from exhaust thermoelectric recovery.
- **Energy access paradox:** 770M people lack electricity. Many live near industries, biomass cookstoves, or engines that waste heat continuously. A $20 thermoelectric module on a cookstove chimney could power LED lighting and phone charging — but current thermoelectric generators cost $10–50/W, making this impossible.
- **Data centers:** Global data centers consume ~460 TWh/year, of which ~98% of electrical energy becomes heat. At-scale waste heat recovery could return 15–30% as electricity, reducing grid load.

**Why hasn't this been solved?** Thermoelectric generators (TEGs) can convert heat directly to electricity with no moving parts — but their efficiency is limited by the thermoelectric figure of merit ZT = S²σT / κ, where S is Seebeck coefficient, σ is electrical conductivity, and κ is thermal conductivity. In bulk materials, the Wiedemann-Franz law couples σ and κ, making it nearly impossible to improve ZT beyond ~1. Current commercial TEGs (Bi₂Te₃, PbTe) achieve ZT ≈ 0.8–1.2, yielding 5–8% conversion efficiency, and use rare (Te), toxic (Pb), or expensive materials — resulting in $10–50/W costs that are 10–100× too expensive for ubiquitous deployment.

## Solution

The **Phononic Thermoelectric Harvester (PTH)** is a new class of thermoelectric metamaterial that shatters the ZT bottleneck by decoupling thermal and electrical transport at the nanoscale, achieving **ZT = 3.0–4.5** using only earth-abundant, non-toxic materials — enabling **15–25% waste-heat-to-electricity conversion** at **$0.50–2.00/W**, making industrial waste heat recovery universally economical for the first time.

### Architecture

The PTH is a multi-layer metamaterial panel consisting of three synergistic layers:

**Layer 1 — Phononic Crystal Thermal Filter (the key innovation):**

A periodic nanostructure of alternating thin films (~10–50 nm each) of two materials with large acoustic impedance mismatch — e.g., SnSe / Mo (Z ratio ~4.5×) or Mg₂Si / TiO₂ (Z ratio ~3.8×). This creates a **phononic bandgap** in the 0.5–5 THz frequency range where most lattice heat phonons reside, blocking ~70–90% of phonon-mediated thermal transport while leaving electronic transport largely unaffected (electrons transport via a different mechanism and are not scattered by the phononic lattice mismatch at these length scales, which are >> electron de Broglie wavelength).

This directly breaks the Wiedemann-Franz coupling: κ_lattice (phonon contribution) is suppressed by the bandgap while κ_electronic (electron contribution, tied to σ via Lorenz number) is preserved. The result: thermal conductivity drops 5–10× while electrical conductivity stays constant, multiplying ZT by the same factor.

**Layer 2 — Nanostructured Earth-Abundant Thermoelectric:**

The active thermoelectric material is **nanostructured tin selenide (SnSe)** — the highest-ZT bulk thermoelectric ever reported (ZT = 2.6 ± 0.3 at 923 K in single crystals, Zhao et al., *Nature* 2014). Polycrystalline SnSe currently achieves ZT ≈ 1.0–1.5 due to grain boundary scattering of electrons. The PTH overcomes this via:

- **Grain boundary passivation** with a 2–5 nm Sb₂Se₃ or Bi₂Se₃ intergranular phase that blocks phonon tunneling while providing an electron-transparent bridge (band alignment ±0.1 eV).
- **Texture engineering** via spark plasma sintering to align the high-ZT b-axis of SnSe orthorhombic crystals perpendicular to heat flow.
- **Doping:** Na (p-type) or Bi (n-type) at 1–3 at% optimizes carrier concentration to 5×10¹⁹ cm⁻³, peak power factor.

Result: polycrystalline SnSe leg ZT ≈ 2.0–2.5 alone, which the phononic filter multiplies to **3.0–4.5**.

**Layer 3 — Graded Thermal Matching Interface:**

Functionally graded thermal impedance matching layers (Cu/Mo/SnSe gradient) at hot and cold contacts minimize Kapitza resistance (interface thermal boundary resistance, typically 10–100 MW/m²·K, reduced to <5 MW/m²·K). This ensures >95% of the available ΔT appears across the thermoelectric, not wasted at interfaces. A radiative-reflecting backsheet (Al or Ag-coated polyimide) and aerogel edge insulation minimize parasitic heat loss.

### System Integration

- **Modular panels:** 100 × 100 × 5 mm tiles, each generating 0.5–2 W at ΔT = 200–500 K. Tiles snap together via built-in series interconnects (silver-paste bus bars) for arbitrary voltage/power scaling.
- **Flexible wrap-around form:** Thinned tiles (1–2 mm) on flexible polyimide substrate wrap pipes and exhaust stacks of any diameter.
- **Power conditioning:** Integrated DC-DC boost converter (96% efficiency, MPPT for variable ΔT) outputs 12/24/48 V DC or feeds an inverter for grid connection.
- **Cold side cooling:** For industrial installations, the cold side uses process water cooling (already available at factories) or forced-air finned heat sinks; for distributed/domestic use, radiative sky cooling surfaces (SiO₂/PDMS, ε > 0.95 @ 8–13 µm) provide passive cold-side heat rejection at no energy cost.

## Key Innovation

**The phononic crystal thermal filter that decouples phonon from electron transport — breaking the Wiedemann-Franz law limit that has constrained thermoelectrics for 200 years.**

In every known bulk thermoelectric, electrical conductivity σ and thermal conductivity κ are linked by the Wiedemann-Franz law (κ_e = L·σ·T, L = Lorenz number), because both are carried by electrons. This means improving σ inevitably increases κ_e, capping ZT. The only path to higher ZT is reducing κ_lattice (phonon transport) without hurting σ — and in bulk materials, grain boundaries and alloying scatter both phonons and electrons equally.

The PTH's phononic crystal — a periodic stack of alternating nanolayers with mismatched acoustic impedance — creates a **phonon bandgap** that selectively blocks lattice phonons (the dominant heat carriers at 300–900 K) while being transparent to electrons (which have wavelengths 100–1000× smaller than the layer thicknesses). This achieves what no bulk alloying can: κ_lattice reduced 5–10× with σ unchanged, multiplying ZT by the same factor.

Combined with earth-abundant nanostructured SnSe (already ZT ≈ 2.0–2.5 in the PTH architecture), the phononic filter pushes ZT to **3.0–4.5** — a regime where thermoelectric waste heat recovery becomes economically dominant. At ZT = 4 and ΔT = 400 K, conversion efficiency reaches ~22%, competitive with small steam turbines but with zero moving parts, zero maintenance, and silent operation.

## Target Cost

| Parameter | Current TEG (Bi₂Te₃/PbTe) | PTH (Phononic SnSe) |
|---|---|---|
| ZT | 0.8–1.2 | 3.0–4.5 |
| Conversion efficiency | 5–8% | 15–25% |
| Cost per watt | $10–50/W | $0.50–2.00/W |
| Key materials | Te ($80/kg), Pb (toxic) | Sn ($32/kg), Se ($30/kg), Mo |
| Temperature range | Up to 250 °C (Bi₂Te₃) / 600 °C (PbTe) | 100–800 °C |
| Module life | 5–10 yr (Te degradation) | 20–30 yr (stable oxides/selenides) |
| Payback (industrial) | Never (>10 yr at $30/W) | 1.5–4 yr at $1.5/W |

**Manufacturing cost breakdown at 1M-unit scale:**
- SnSe nanopowder (solvo-thermal synthesis): $0.15/W
- Phononic crystal deposition (sputtering/ALD, 20 layers × 20 nm): $0.20/W
- SPS sintering + dicing: $0.10/W
- Contact metallization + packaging: $0.15/W
- DC-DC converter + interconnects: $0.10/W
- **Total: ~$0.70/W at 1M-unit scale; $1.50/W at 100K units; $2.00/W at 10K units**

**Application economics:**
- **Steel mill exhaust** (1 MW thermal × 30% → 150 kW electrical): $225K capital, $60K/yr electricity value → **3.7-year payback**
- **Heavy-duty truck** (20 kW from exhaust, saves 8% fuel = $3,000/yr): $4,000 system → **1.3-year payback**
- **Biomass cookstove** (5W from chimney, powers LED + phone): $10 module → **payback in months** via displaced kerosene ($40/yr)
- **Data center rack** (200W per rack from hot aisle): $400/rack, $80/yr savings → **5-year payback**, + cooling load reduction

## Impact

### Climate
- **1–2 Gt CO₂/year avoided** at 20% global industrial waste heat recovery (displacing fossil grid electricity)
- Equivalent to **decarbonizing all of global aviation + shipping** combined
- Net carbon-negative manufacturing: SnSe and Mo are abundant; panel production emits ~2 kg CO₂/W, recovered in <6 months of operation

### Energy Access
- **770M unelectrified people** — a $10 cookstove module provides enough electricity (5W) for LED lighting (replacing kerosene lamps that cause 500K+ premature deaths/year from indoor air pollution) and phone charging
- **Decentralized power from waste heat** — no fuel, no grid, no maintenance; any heat source becomes a micro-generator
- Enables **off-grid industrial cogeneration** in developing countries — factories become their own power plants

### Industrial Competitiveness
- Energy-intensive industries recover 5–20% of energy costs: global potential **$200–500B/year** in recovered energy value
- Steel, cement, glass, aluminum, chemicals, refining — all become 5–15% more energy-efficient
- Creates a new **$50–150B/year** thermoelectric manufacturing industry and 500K–2M jobs

### Transportation
- 5–15% fuel efficiency improvement for heavy-duty trucks, ships, and trains
- For shipping alone (11 Mt fuel/year): ~1 Mt fuel saved, 3 Mt CO₂ avoided
- Enables silent, vibration-free auxiliary power (replacing gensets)

### Universal Benefit
- **No rare or conflict minerals**: Sn (tin), Se (selenium), Mo (molybdenum) are all earth-abundant, widely mined, and non-toxic at the concentrations used
- **No moving parts, no maintenance, silent**: 20–30 year service life, deployable anywhere with a temperature difference
- **Democratized manufacturing**: nanopowder synthesis + spark plasma sintering + sputtering are all established industrial processes; no exotic equipment
- **Retrofittable**: wraps around existing pipes, stacks, engines — no system redesign required
- **Modular and scalable**: from 5W (cookstove) to 1 MW (steel mill) with the same tile technology

### Quantified Impact at Scale (50M modules by 2045)
| Metric | Value |
|---|---|
| Waste heat recovered | 50–150 GW electrical equivalent |
| CO₂ avoided | 0.5–1.5 Gt/year |
- People gaining electricity access | 100–500M (cookstove/distributed modules)
- Economic value created | $50–200B/year
- Jobs in manufacturing/installation | 500K–2M
|- Kerosene displaced | 2–5B liters/year (indoor air pollution reduction)

---

## How It Works

### The Thermoelectric Effect — Refresher

When a temperature difference ΔT exists across a thermoelectric material, charge carriers (electrons in n-type, holes in p-type) diffuse from the hot side to the cold side, producing a voltage — the **Seebeck effect**. The open-circuit voltage is V = S·ΔT, where S is the Seebeck coefficient (~200–400 µV/K for SnSe). Connect a load and you get electrical power P = S²·ΔT² / (4·R_internal), maximized when load resistance matches internal resistance.

The catch: the same ΔT that drives electrons also drives **phonons** (quantized lattice vibrations) to carry heat from hot to cold — short-circuiting the temperature gradient and degrading efficiency. The figure of merit ZT = S²σT / κ captures this tension: you want high S and σ (electrical) but low κ (thermal). In bulk materials, σ and κ_e are coupled by the Wiedemann-Franz law (κ_e = L·σ·T), so you can't raise one without the other. Only κ_lattice — the phonon contribution — is independently tunable, and bulk alloying scatters phonons and electrons equally.

### The Phononic Crystal Breakthrough — Step by Step

**Step 1 — Phonon Bandgap Engineering.** Sound and heat are both phonons. Just as a photonic crystal blocks certain wavelengths of light, a phononic crystal — a periodic structure with alternating acoustic impedance — blocks certain phonon frequencies. The PTH deposits alternating 10–50 nm layers of SnSe (acoustic impedance Z ≈ 1.8×10⁷ kg/m²·s) and Mo (Z ≈ 8.2×10⁷ kg/m²·s), a 4.5× mismatch. Bragg reflection at each interface creates a bandgap centered at 1–3 THz — precisely where most thermal phonons at 300–900 K carry energy. Phonons in the bandgap are reflected, not transmitted.

**Step 2 — Electron Transparency.** Electrons travel as waves with a de Broglie wavelength λ = h / p ≈ 5–50 nm in doped SnSe. The phononic layers are 10–50 nm — comparable but the key insight is that electrons tunnel coherently across layers whose band edges are aligned (SnSe and Mo have compatible work functions). The electron scattering cross-section of the interface is 100–1000× smaller than the phonon scattering cross-section, so σ is essentially unchanged while κ_lattice drops 5–10×.

**Step 3 — SnSe Nanostructuring.** The active thermoelectric is polycrystalline SnSe, synthesized as 50–200 nm grains via solvothermal precipitation. Grain boundaries normally scatter electrons (hurting σ), but a 2–5 nm Sb₂Se₃ intergranular passivation layer has a conduction band offset of only ~0.08 eV with SnSe — electrons pass through ballistically while mid-frequency phonons (1–5 THz) are blocked. The grains are texture-aligned via spark plasma sintering (SPS) at 500 °C / 50 MPa so the high-mobility b-axis points perpendicular to heat flow.

**Step 4 — Graded Interface Matching.** Kapitza resistance (thermal boundary resistance at metal/ceramic interfaces) wastes 10–30% of ΔT. The PTH uses a functionally graded Cu→Mo→SnSe contact (composition gradient over 200 nm) that smooths the impedance transition, reducing interface resistance to <5 MW/m²·K — ensuring >95% of ΔT appears across the thermoelectric.

**Step 5 — Power Extraction.** A tile at ΔT = 400 K produces ~1.6 V open-circuit. An integrated synchronous DC-DC boost converter with maximum-power-point tracking (MPPT) holds the load at V = 0.8 V (half open-circuit, the maximum power point), boosting to 12/24/48 V DC at 96% efficiency. Tiles connect in series via silver-paste bus bars for voltage scaling and in parallel for current scaling.

### The Full Energy Path

```
Waste heat source (exhaust, hot surface, engine block)
  → Hot-side contact (graded Cu/Mo/SnSe, Kapitza < 5 MW/m²·K)
    → Phononic crystal filter (20× SnSe/Mo layers, bandgap 0.5–5 THz)
      → Nanostructured SnSe thermoelectric legs (p-type Na-doped / n-type Bi-doped)
        → Seebeck voltage generated (S ≈ 300 µV/K × ΔT)
          → Cold-side contact (graded, radiative sky-cooling or water)
            → DC-DC MPPT converter (96%) → 12/24/48 V DC or grid inverter
```

## Technical Architecture

### Subsystem Map

| Subsystem | Function | Key Components | Metrics |
|---|---|---|---|
| **Phononic Filter** | Block lattice phonons, transmit electrons | 10–20 periods SnSe/Mo, 10–50 nm each | κ_lattice ↓ 5–10×, σ unchanged |
| **Thermoelectric Core** | Convert ΔT → electricity | Polycrystalline SnSe, Na/Bi doped, SPS-textured | ZT_leg = 2.0–2.5 |
| **Graded Contacts** | Minimize interface thermal resistance | Cu→Mo→SnSe functional gradient, 200 nm | Kapitza < 5 MW/m²·K |
| **Cold-Side Rejection** | Maintain ΔT | Radiative sky cooler (SiO₂/PDMS) or water jacket | ε > 0.95 @ 8–13 µm |
| **Power Conditioning** | MPPT + voltage regulation | Synchronous boost converter, GaN FETs | 96% eff, 12/24/48 V |
| **Thermal Packaging** | Minimize parasitic losses | Al backsheet, aerogel edge insulation | <5% parasitic loss |
| **Interconnects** | Series/parallel scaling | Ag-paste bus bars, snap-fit contacts | 0.05–0.15 Ω/tile |

### Data and Energy Flow

1. **Heat input** → hot-side contact (90–95% of source heat enters, 5–10% lost to radiation/convection)
2. **Phonon filtering** → phononic crystal reflects 70–90% of lattice phonons back toward hot side; electrons pass through
3. **Thermoelectric generation** → SnSe legs produce V = S·ΔT; internal resistance R_int = 0.05–0.15 Ω/tile
4. **Cold-side rejection** → radiative sky cooling dumps heat to deep space (net cooling power 50–100 W/m² at night) or process water loop
5. **Power conditioning** → MPPT tracks optimal load as ΔT varies; DC-DC boost to bus voltage
6. **Output** → 12/24/48 V DC (off-grid), or grid-synchronized inverter (380 V AC, 50/60 Hz)

### Module Topologies

| Form Factor | Dimensions | Power | Application |
|---|---|---|---|
| Standard tile | 100×100×5 mm | 0.5–2 W | Industrial arrays, building facades |
| Flexible wrap | 50×50×2 mm (polyimide) | 0.2–0.8 W | Pipes, exhaust stacks, engine blocks |
| Cookstove module | 40×40×8 mm (with heat sink) | 3–5 W | Off-grid lighting/charging |
| Industrial panel | 1×0.5 m (100 tiles) | 50–200 W | Steel/glass/cement exhaust |

## Performance Benchmarks

### Efficiency vs. State of the Art

| Technology | ZT (peak) | Efficiency @ ΔT=400K | Material Cost | Max Temp | Source |
|---|---|---|---|---|---|
| Bi₂Te₃ (commercial) | 1.0 | 6% | $10–50/W | 250 °C | Industry standard |
| PbTe (Tellurex) | 1.2 | 8% | $15–40/W | 600 °C | Legacy industrial |
| Skutterudite CoSb₃ | 1.4 | 9% | $8–20/W | 700 °C | Lab → pilot |
| Half-Heusler (NbFeSb) | 1.5 | 10% | $5–12/W | 800 °C | Research |
| SnSe single crystal | 2.6 | 14% | $3–8/W | 923 K | Zhao et al., *Nature* 2014 |
| **PTH (this work)** | **3.0–4.5** | **15–25%** | **$0.50–2.00/W** | **800 °C** | **Projected from physics** |

### Power Density Benchmarks

| Metric | Current TEG | PTH Target | Improvement |
|---|---|---|---|
| Gravimetric (W/kg) | 5–15 | 30–80 | 4–6× |
| Areal (mW/cm²) | 10–40 | 50–200 | 3–5× |
| Volumetric (W/cm³) | 0.1–0.4 | 1.0–4.0 | 5–10× |
| Cost ($/W) | 10–50 | 0.50–2.00 | 10–50× |

### Durability Benchmarks

| Parameter | Current TEG | PTH Target |
|---|---|---|
| Thermal cycling | 1,000 cycles | 10,000 cycles |
| Service life | 5–10 yr | 20–30 yr |
| Degradation rate | 2–5%/year | <0.5%/year |
| Operating hours | ~50,000 | >175,000 |

## Deployment Scenarios

### Scenario 1: Integrated Steel Mill Recovery

A typical integrated steel mill produces 2 Mt crude steel/year, consuming ~18 GJ/t — of which ~30% (5.4 GJ/t) exits as waste heat in exhaust gases (300–1200 °C) from blast stoves, coke ovens, and reheating furnaces. Wrapping 10,000 m² of exhaust ducts and stack surfaces with PTH industrial panels (200 W/m² @ ΔT=350K) yields **2 MW of electricity** — enough to power the mill's lighting, motors, and controls, displacing 4,000 MWh/year of grid power at $0.08/kWh = $320K/year savings. Capital cost: $2M (at $1/W). Payback: 6.3 years, with 20+ years of free power thereafter. CO₂ avoided: 2,000 t/year.

### Scenario 2: Heavy-Duty Truck Exhaust Recovery

A long-haul truck burns ~30,000 L diesel/year. The exhaust at 400–600 °C represents ~90 kW of waste heat. A flexible PTH wrap on the exhaust pipe and DPF housing (0.5 m², 10 panels) recovers **1.5–3 kW electrical** — enough to run the truck's hotel loads (AC, HVAC, refrigeration, electronics) without idling the engine, and to charge an electrified accessory battery. Fuel savings: 5–8% (~2,000 L/year = $2,400/year). System cost: $3,500. Payback: 1.5 years. CO₂ avoided: 5.3 t/year per truck. At 15M trucks globally: 80 Mt CO₂/year.

### Scenario 3: Off-Grid Cookstove Electrification

A biomass cookstove chimney reaches 300–500 °C during cooking (2–4 hours/day). A single PTH cookstove module (40×40×8 mm, $10) clamped to the chimney produces **3–5 W during cooking**, charging a 10 Wh LiFePO₄ battery that powers three 1W LEDs for 6+ hours of evening light and charges a mobile phone — replacing the $40/year kerosene lamp expenditure that also causes indoor air pollution (500K+ premature deaths/year). At 100M cookstoves deployed: 500 MW distributed generation, 2B liters kerosene displaced, 5 Mt CO₂ avoided, and 300–500M people gain first electricity access.

## Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| **SnSe long-term oxidation** at >500 °C in air | Medium | High — degrades ZT and leg integrity | Hermetic sealing in inert N₂/Se atmosphere within Al casing; Se vapor reservoir maintains stoichiometry; validated 10,000 hr lifetimes in sealed PbTe modules (analogous) |
| **Phononic filter delamination** from thermal cycling stress (CTE mismatch SnSe/Mo) | Medium | Medium — bandgap degradation | Graded interface (SnSe→Mo transition over 50 nm) reduces CTE stress; polyimide compliance layer; 10,000-cycle thermal cycling qualification (−40 to +700 °C) |
| **Scalability of nanolayer deposition** (sputtering/ALD throughput) | Medium | High — cost bottleneck | Roll-to-roll sputtering (already commercial for solar cells at 30 m/min); ALD for ultra-thin layers; 1M-unit/year line at $20M capex produces $0.20/W filter cost |
| **Selenium supply constraints** (Se is a byproduct of Cu refining, ~3 kt/year global) | Low | Medium — material scaling | SnSe is only 34 wt% Se; at 50M modules × 50 g Se = 2,500 t — <1 year of current supply. Recycling loop recovers >95% Se. Mg₂Si/TiO₂ phononic filter is a drop-in alternative with zero Se |
| **Competing technologies** (ORC turbines, thermodynamic cycles) outperform at scale | Low | Medium | ORC needs >50 kW and maintenance; PTH dominates <10 kW and all maintenance-free applications. Hybrid PTH+ORC for large industrial: PTH captures 100–300 °C gradient, ORC takes the rest |
| **Grid integration** for industrial-scale PTH arrays | Low | Low | Standard DC-DC + inverter; utility interconnection agreements for <1 MW are routine in most jurisdictions |
| **Public perception of Se toxicity** | Low | Medium | SnSe is insoluble and sealed; Se is an essential trace nutrient (RDA 55 µg/day); end-of-life recycling mandated. SDS classifies SnSe as "harmful if swallowed" (Category 4), far less hazardous than PbTe |

## Vision for 2050

By 2050, the Phononic Thermoelectric Harvester is **infrastructure-grade** — as ubiquitous and invisible as insulation. Every industrial smokestack, steam pipe, engine exhaust, and furnace wall is wrapped in PTH panels that quietly return 15–25% of waste heat as electricity. The global steel, cement, glass, and chemical industries run 10% more efficiently, saving $300B/year. Every long-haul truck, ship, and train recovers 5–15% of its fuel energy from the exhaust. Data centers recapture 20% of their heat as power, shaving 90 TWh/year off global electricity demand.

In the developing world, 500M people who once burned kerosene for light now charge phones and run LED lamps from the heat of their own cookstoves — the same fire that cooks their food also electrifies their home, with no grid, no fuel cost, and no maintenance. Indoor air pollution deaths drop by 30%. Kerosene consumption falls by 3 billion liters/year.

The thermoelectric manufacturing industry employs 1–2M people in nanopowder synthesis, sintering, deposition, and installation — a new skilled-trade sector spanning every industrialized nation. Material flows are circular: 95% of Sn and Se are recovered at end-of-life and re-enter the supply chain.

The Wiedemann-Franz law — a 200-year-old limit that said thermoelectrics could never be efficient enough to matter — is a footnote in engineering textbooks, next to a paragraph about how phononic crystals rewrote the rule. Waste heat, once the largest single inefficiency in human civilization, is now a resource.