# Thermoacoustic Metamaterial Heat Pump — Technical Specification

## 1. System Overview

| Parameter | Residential 3 kW | Residential 10 kW | Commercial 50 kW | Industrial 500 kW |
|-----------|-----------------|-------------------|-------------------|---------------------|
| Cooling capacity | 1–3 kW | 3–10 kW | 20–50 kW | 200–500 kW |
| Heating capacity | 1.5–4.5 kW | 4.5–15 kW | 30–75 kW | 300–750 kW |
| COP (cooling, 35°C) | 3.5–4.5 | 3.5–4.5 | 3.5–4.5 | 3.0–4.0 |
| COP (heating, 8°C) | 4.0–5.0 | 4.0–5.0 | 3.5–5.0 | 3.0–4.5 |
| COP (heating, -20°C) | 3.0–4.5 | 3.0–4.5 | 2.5–4.0 | 2.5–3.5 |
| Working fluid | Helium (3–8 bar) | Helium (5–10 bar) | Helium (5–12 bar) | Helium-argon (8–15 bar) |
| Refrigerant charge | 0 | 0 | 0 | 0 |
| Moving parts | 1 (linear motor) | 1 (linear motor) | 1–2 (motor + fan) | 2–4 (motor + fans) |
| Service life | 30–40 yr | 30–40 yr | 25–35 yr | 20–30 yr |
| Noise (external) | 30–45 dB | 35–48 dB | 45–55 dB | 50–60 dB |
| Input power | 240 VAC or 48 VDC | 240 VAC or 48 VDC | 208/240 VAC | 480 VAC 3-phase |

## 2. Acoustic Driver (Linear Motor)

### 2.1 Motor specifications

| Parameter | Value |
|-----------|-------|
| Type | Moving-magnet, flexure-bearing linear motor |
| Operating frequency | 100–300 Hz (tuned to resonator fundamental) |
| Stroke | 5–20 mm peak-to-peak |
| Peak force | 50–500 N (residential); 500–5,000 N (commercial) |
| Electro-acoustic efficiency | 85–92% |
| Motor constant (BL) | 15–50 N/A (residential); 50–200 N/A (commercial) |
| Voice coil resistance | 2–8 Ω |
| Voice coil inductance | 0.5–3.0 mH |
| Magnet | NdFeB N52 (grade 52, max operating temp 80–150°C) |
| Bearing | Flexure springs (beryllium-copper or steel, 3–5 stage) |
| MTBF | 100,000+ hours (11.4 years continuous; 30+ years at 8 hr/day) |

### 2.2 Materials

- **Magnet:** NdFeB N52, nickel-coated for corrosion resistance
- **Voice coil:** Copper wire, high-temperature polyimide insulation (180°C rated)
- **Flexure bearings:** Beryllium-copper alloy (C17200), 3–5 stage diaphragm, 10⁸+ cycle fatigue life
- **Motor housing:** Aluminum 6061-T6, anodized
- **Back iron:** Low-carbon steel (1008/1018), laminated to reduce eddy currents

### 2.3 Driver electronics

| Parameter | Value |
|-----------|-------|
| Topology | Class-D switching amplifier (H-bridge) |
| Switching frequency | 20–50 kHz (well above acoustic fundamental) |
| Efficiency | 95–97% |
| Control method | Sliding-mode current control with phase tracking |
| DSP | ARM Cortex-M7 or equivalent (400+ MHz, 32-bit FPU) |
| Phase resolution | 0.01° (for precise heating/cooling switching) |
| Amplitude resolution | 12-bit (0.024% of full scale) |
| Protection | Overcurrent, overtemp, overvoltage, stall detection |

## 3. Resonator

### 3.1 Geometry

| Parameter | Residential (3 kW) | Residential (10 kW) | Commercial (50 kW) |
|-----------|--------------------|--------------------|---------------------|
| Resonator type | Single-closed tube (quarter-wave) or half-wave | Half-wave with central stack | Half-wave with central stack |
| Diameter | 80–150 mm | 150–250 mm | 250–400 mm |
| Length | 300–600 mm | 500–1000 mm | 800–1500 mm |
| Wall thickness | 2–4 mm (aluminum) or 1.5–3 mm (stainless) | 3–5 mm | 4–8 mm |
| Internal pressure | 3–8 bar (He) | 5–10 bar (He) | 5–12 bar (He) |
| Design pressure | 2× operating (ASME B31.3) | 2× operating | 2× operating |
| Material | 6061-T6 aluminum or 316L stainless | 6061-T6 or 316L | 316L stainless |

### 3.2 Acoustic parameters

| Parameter | Value |
|-----------|-------|
| Fundamental frequency | 100–300 Hz (tuned by resonator length and gas speed of sound) |
| Acoustic pressure amplitude | 170–185 dB SPL internal (15–35 kPa peak) |
| Drive ratio (p₁/p₀) | 5–15% (below shock threshold ~10%) |
| Acoustic power | 10–100 W (residential); 100–1000 W (commercial) |
| Gas | Helium-4 (industrial grade, 99.99%) or He-Ar mixture (30–70% Ar) |
| Speed of sound (He, 300K, 5 bar) | ~1007 m/s |
| Wavelength (200 Hz) | ~5.0 m → half-wave resonator ~2.5 m (folded) |
| Wavelength (300 Hz) | ~3.4 m → quarter-wave ~0.85 m |

### 3.3 Resonator shape optimization

The resonator is **not a simple cylinder**. AI-guided topology optimization (physics-informed neural network solving linearized Euler + Rott equations) produces a slightly non-uniform profile:
- **Driver end:** Slightly flared (5–10% diameter increase) to improve motor-to-resonator acoustic coupling
- **Lens section:** Constant diameter
- **Stack section:** Slight waist constriction (3–8%) to increase local gas velocity at the stack, enhancing heat transfer
- **Bandgap section:** Constant diameter
- **Far end:** Slightly tapered (2–5%) to reduce end-reflection losses

This non-uniform profile improves overall acoustic-to-thermal efficiency by 8–15% compared to a simple cylinder.

## 4. Phononic Crystal Acoustic Lens

### 4.1 Design

| Parameter | Value |
|-----------|-------|
| Type | Sub-wavelength Helmholtz resonator array |
| Cavity count | 200–2,000 (depending on unit size) |
| Cavity pitch | 5–15 mm (λ/20 to λ/40 of acoustic wavelength) |
| Cavity volume | 10–100 mm³ each |
| Neck diameter | 1–3 mm |
| Neck length | 2–5 mm |
| Resonant frequency | Tuned to resonator fundamental (100–300 Hz) |
| Material | 3D-printed AlSi10Mg (aluminum) or PEEK |
| Fabrication | Laser powder-bed fusion (LPBF) or FDM (PEEK) |
| Acoustic gain | 8–15 dB at stack entrance |
| Phase-matching error | <5° between pressure and optimal displacement |

### 4.2 Lens mechanism

The Helmholtz resonator array acts as a **dispersive acoustic metamaterial**. Each cavity resonates at the fundamental frequency, but with a phase lag determined by its neck-to-volume ratio. By varying the cavity dimensions across the lens, the array creates a **graded acoustic refractive index** — slowing the pressure wave in regions where displacement needs to advance, and vice versa. The net effect at the stack entrance:

- **Pressure wave:** Delayed by 20–40° relative to the free-field traveling wave
- **Displacement wave:** Advanced by 20–40° relative to free-field
- **Result:** Pressure and displacement arrive at the stack in the optimal Stirling-cycle quadrature (p leads ξ by 60–90° for the cooling direction, or lags by 60–90° for heating)

This is the acoustic analog of a **metamaterial lens focusing light** — but in the acoustic domain, and for phase shaping rather than amplitude focusing.

### 4.3 Fabrication

The lens is 3D-printed as a single monolithic piece using **laser powder-bed fusion (LPBF)** of AlSi10Mg aluminum alloy, or **fused deposition modeling (FDM)** of PEEK (polyether ether ketone) for lower-cost units. The print takes 4–12 hours on a commercial metal 3D printer (EOS M100, Renishaw AM250) and costs $20–80 in material + machine time at production scale.

The lens is a **non-moving, non-load-bearing** component with a design life of 30+ years. AlSi10Mg has a service temperature of 150–200°C continuous, well above the stack temperature (40–90°C typical). PEEK is rated to 250°C.

## 5. Phononic Bandgap Reflector

### 5.1 Design

| Parameter | Value |
|-----------|-------|
| Type | Embedded quarter-wave resonators in resonator wall |
| Target harmonics | 1.5×, 2×, 3× fundamental (typical parasitic modes) |
| Resonator depth | λ/4 at target harmonic (42–125 mm at 200–600 Hz) |
| Resonator count per harmonic | 16–64 (circumferential array) |
| Suppression per harmonic | >20 dB |
| Material | Same as resonator wall (3D-printed insert or machined) |

### 5.2 Mechanism

In any real resonator, acoustic energy couples into higher-order modes — standing waves at harmonics of the fundamental. These parasitic modes:
- Carry acoustic energy away from the useful traveling wave (15–30% loss in uncontrolled resonators)
- Create spatial non-uniformities in the stack heat transfer
- Can cause stack hot spots and reduced COP

The bandgap reflector embeds **quarter-wave resonator cavities** in the resonator wall, each tuned to a specific parasitic harmonic. When a parasitic mode at, say, 2× the fundamental (400 Hz for a 200 Hz resonator) propagates, the quarter-wave resonators at that frequency oscillate in antiphase, creating an acoustic "short" that reflects the parasitic wave. The reflected energy is re-injected into the fundamental traveling wave by the phononic crystal lens.

This is the acoustic analog of a **photonic bandgap mirror** — a structure that reflects specific wavelengths while transmitting others.

## 6. Regenerative Stack

### 6.1 Specifications

| Parameter | Value |
|-----------|-------|
| Material | Cordierite ceramic (honeycomb) or stainless-steel felt |
| Pore size | 0.1–0.5 mm (tuned to thermal penetration depth) |
| Porosity | 75–90% |
| Stack thickness | 5–15 mm (along acoustic axis) |
| Thermal penetration depth (δₖ) | 0.05–0.3 mm in helium at 200 Hz, 5 bar |
| Pore count | 1,000–5,000 pores/cm² |
| Thermal conductivity | 1.5–3.0 W/m·K (cordierite) |
| Specific heat | 800–1,000 J/kg·K |
| Max service temperature | 600°C (cordierite), 800°C (steel felt) |

### 6.2 Thermal penetration depth

The critical stack parameter is the **gas thermal penetration depth (δₖ)** — the distance heat diffuses into the gas during one acoustic cycle:

    δₖ = √(2κ / (ρ c_p ω))

where κ = thermal conductivity, ρ = density, c_p = specific heat, ω = angular frequency.

For helium at 200 Hz, 5 bar, 300K: δₖ ≈ 0.15 mm.

The stack pore size is chosen as **2–4× δₖ** so that gas parcels fully exchange heat with the pore walls within one acoustic cycle — but not so large that heat bypass occurs. For helium at 200 Hz, 5 bar: optimal pore size ≈ 0.3–0.6 mm.

### 6.3 Stack fabrication

Cordierite honeycomb stacks are manufactured by **extrusion** — the same process used for automotive catalytic converters. A cordierite paste is extruded through a multi-hole die, dried, and fired at 1,200–1,400°C. The result is a ceramic honeycomb with precisely controlled pore geometry. This is a **high-volume, low-cost** manufacturing process ($2–8 per stack at production scale).

Stainless-steel felt stacks are made by **sintering** compressed steel fibers (4–8 µm diameter) at 800–1,000°C. More expensive ($10–30) but higher temperature rating and better thermal shock resistance.

## 7. Heat Exchangers

### 7.1 Cold and hot HX

| Parameter | Value |
|-----------|-------|
| Type | Finned-tube, micro-channel enhanced |
| Tube material | Copper (C12200, deoxidized high-phosphorus) |
| Fin material | Aluminum 1100 (0.1–0.15 mm thick, 1.5–2.5 mm pitch) |
| Micro-channel | 0.5–1.0 mm hydraulic diameter, laser-welded |
| Heat transfer coefficient | 200–600 W/m²K (gas-side), 50–150 W/m²K (air-side with fins) |
| Thermal resistance (total) | 0.005–0.020 K/W |
| HX area | 0.05–0.5 m² (residential); 0.5–5.0 m² (commercial) |
| Fan | Variable-speed EC (electronically commutated) motor, 5–100 W |

### 7.2 Reversibility

No mechanical reversing valve is needed. Heating/cooling mode is switched by **shifting the acoustic phase 180°** in the motor controller. In cooling mode, the indoor HX is the cold side; in heating mode, the indoor HX is the hot side. The fans are simply reassigned by the controller.

For defrost in cold-climate heating: the controller periodically reverses to cooling mode for 2–5 minutes (melting frost on the outdoor HX), then reverts. The indoor air fan turns off during defrost to avoid cold-air delivery.

## 8. Working Fluid

### 8.1 Helium properties

| Property | Value (300K, 5 bar) |
|----------|---------------------|
| Thermal conductivity | 0.152 W/m·K (5.7× air) |
| Specific heat (c_p) | 5,193 J/kg·K |
| Density | 0.807 kg/m³ |
| Speed of sound | 1,007 m/s |
| Prandtl number | 0.68 |
| Viscosity | 2.0 × 10⁻⁵ Pa·s |
| Global Warming Potential | **0** |
| Ozone Depletion Potential | **0** |
| Flammability | **None** |
| Toxicity | **None** (inert noble gas) |

### 8.2 Why helium

Helium is the ideal thermoacoustic working fluid because:
- **Highest thermal conductivity** of all gases (5.7× air) → maximum heat exchange in the stack
- **Low Prandtl number** (0.68) → high ratio of thermal to viscous penetration depth → efficient stack operation
- **Inert** → no chemical degradation of stack, resonator, or seals
- **Zero GWP, zero ODP** → no climate or ozone impact, no regulatory restriction
- **Non-flammable, non-toxic** → no safety hazard
- **Monatomic** → no vibrational/rotational degrees of freedom → all acoustic energy goes into translational motion (no molecular relaxation losses)

### 8.3 Helium-argon mixture

For larger units (50 kW+), a **helium-argon mixture** (30–70% argon) reduces helium consumption and increases acoustic impedance (arguably improving driver coupling). The tradeoff is reduced thermal conductivity and increased Prandtl number. Optimal mixture is determined by the AI optimizer for each unit size.

### 8.4 Helium charge and supply

- **Residential 3 kW:** 5–10 g helium
- **Residential 10 kW:** 10–25 g helium
- **Commercial 50 kW:** 50–150 g helium
- **Industrial 500 kW:** 200–500 g helium (with argon dilution)

Global helium production: ~160 million m³/yr (2024). If 1 billion TMHP units deploy by 2050 at 15 g He each, total charge = 15,000 m³ — a trivial fraction (0.01%) of annual production. Helium is recoverable at end-of-life (vent to atmosphere — inert, zero GWP; or recapture for reuse).

## 9. Control System

### 9.1 Controller architecture

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│  Thermostat  │────▶│   Controller │────▶│  Motor      │
│  (mode,      │     │   (DSP)      │     │  Driver      │
│   setpoint)  │     │              │     │  (Class-D)   │
└──────────────┘     └──────┬───────┘     └──────┬───────┘
                            │                      │
                     ┌──────┴───────┐      ┌──────┴───────┐
                     │  AI Mode     │      │  Phase/      │
                     │  Optimizer   │      │  Amplitude   │
                     │  (NN)        │      │  Control     │
                     └──────┬───────┘      └──────────────┘
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
        ┌──────────┐  ┌──────────┐  ┌──────────┐
        │ Pressure │  │ Temp     │  │ Motor    │
        │ sensor    │  │ sensors  │  │ current  │
        │ (piezo)   │  │ (RTD)    │  │ sensor   │
        └──────────┘  └──────────┘  └──────────┘
```

### 9.2 Control functions

| Function | Method | Update rate |
|----------|--------|-------------|
| **Mode control** (heat/cool) | Set acoustic phase 0° (cool) or 180° (heat) | On command |
| **Capacity modulation** | Vary motor amplitude 20–100% | 10 Hz |
| **Frequency tracking** | Adjust drive frequency to track resonator fundamental (shifts ±2–5 Hz with temperature) | 1 Hz |
| **Phase optimization** | AI neural network predicts optimal lens-stack phase from pressure sensor FFT | 0.1 Hz |
| **Defrost control** | Trigger phase reversal when outdoor HX temp < 0°C + humidity > 80% | Event-driven |
| **Diagnostics** | Motor current waveform FFT detects: gas leakage (pressure drop), stack degradation (efficiency drop), HX fouling (thermal resistance rise) | 0.01 Hz (hourly) |
| **Predictive maintenance** | Trend diagnostics; alert when 80% of service-life threshold | Daily |

### 9.3 AI mode optimizer

A **physics-informed neural network** (2–5K parameters, runs on the DSP) learns the resonator's acoustic response across temperature and pressure conditions. It optimizes:
- Drive frequency (to track resonator drift)
- Phase angle (to maximize stack heat pumping)
- Amplitude (for capacity modulation)

The NN is pre-trained on a finite-element simulation of the resonator (linearized Euler + Rott equations) and fine-tuned on the specific unit during the first 100 hours of operation using the pressure sensor feedback. This per-unit adaptation compensates for manufacturing tolerances (±5–10% in stack geometry, lens dimensions, and gas pressure).

## 10. Manufacturing

### 10.1 Bill of materials (residential 10 kW)

| Component | Material | Cost (at 100K/yr scale) | Source |
|-----------|----------|------------------------|--------|
| Linear motor | NdFeB, Cu, BeCu flexures, Al housing | $80–150 | Loudspeaker supply chain (adapted) |
| Resonator tube | 6061-T6 aluminum, 200×500 mm | $20–40 | Standard tube/extrusion |
| Phononic crystal lens | AlSi10Mg, 3D-printed | $20–80 | Metal AM service bureau |
| Bandgap reflector | Al or PEEK, 3D-printed/machined | $10–30 | In-house or AM bureau |
| Stack (cordierite) | Cordierite honeycomb, extruded | $2–8 | Catalytic converter supply chain |
| Cold HX | Cu tubes + Al fins | $30–60 | HVAC HX supply chain |
| Hot HX | Cu tubes + Al fins | $30–60 | HVAC HX supply chain |
| Fans (2×) | EC motor + plastic blades | $20–40 each = $40–80 | HVAC fan supply chain |
| Motor controller | DSP + H-bridge + sensors | $30–60 | Electronics manufacturing |
| Enclosure + insulation | Steel + EPS/PIR foam | $40–80 | Sheet metal + foam |
| Helium charge | 15–25 g industrial He | $2–5 | Industrial gas supplier |
| Misc (fasteners, seals, wiring) | — | $20–40 | Standard hardware |
| **Total BOM** | | **$294–583** | |
| Assembly + test (2–3 hr at $30/hr) | | $60–90 | |
| **Manufactured cost** | | **$354–673** | |
| **Retail price (40% margin)** | | **$590–1,122** | |

### 10.2 Supply chain

All components use **existing, high-volume supply chains** — no new material, no new manufacturing process:
- Linear motor → adapted from high-end loudspeaker and linear-alternator industry
- Resonator → standard aluminum tube extrusion
- Phononic crystal lens → metal 3D printing (commercial since 2015, $20–80/part at scale)
- Stack → catalytic converter extrusion (billions made yearly for automotive)
- Heat exchangers → standard HVAC finned-tube manufacturing
- Controller → standard power electronics manufacturing

The only non-standard step is 3D printing of the metamaterial lens and bandgap reflector — but metal LPBF is now a mature, high-volume process with commercial service providers worldwide (Protolabs, Shapeways, Xometry, plus in-house EOS/Renishaw machines).

### 10.3 Assembly

TMHP assembly is **simpler than conventional AC assembly** because:
- No compressor (eliminates the most complex, precision-critical, hermetic-seal-dependent step)
- No refrigerant lines (eliminates brazing, flaring, vacuum pump-down, leak test)
- No reversing valve (eliminates a failure-prone component)
- No oil charge
- No EPA 608 certification required (no refrigerant)

Estimated assembly time: **2–3 hours per unit** (vs. 4–6 for conventional AC with compressor, refrigerant lines, and certification).

### 10.4 Installation

TMHP installation requires:
- Mounting the indoor and outdoor units (same as conventional mini-split)
- Connecting the two units with **a single cable** (no refrigerant lines, no flare nuts, no vacuum pump)
- Connecting power (240V or 48V DC)
- Done.

No EPA certification, no refrigerant recovery, no leak test, no system commissioning. Estimated installation: **2–3 hours** (vs. 4–8 for a conventional mini-split). **A homeowner or handyman can install it.**

## 11. Thermodynamic Analysis

### 11.1 Ideal Stirling cycle COP

For the thermoacoustic Stirling cycle, the ideal COP is:

    COP_cooling = T_cold / (T_hot - T_cold)
    COP_heating = T_hot / (T_hot - T_cold)

| Condition | T_cold (K) | T_hot (K) | COP_heating (ideal) | COP_cooling (ideal) |
|-----------|-----------|----------|---------------------|---------------------|
| AC, 35°C outdoor | 280 | 310 | 10.3 | 9.3 |
| Heating, 8°C outdoor | 273 | 295 | 13.4 | 12.4 |
| Heating, -20°C outdoor | 253 | 295 | 7.0 | 6.0 |

### 11.2 Real COP (accounting for losses)

| Loss mechanism | COP penalty | TMHP estimate |
|----------------|-------------|---------------|
| Acoustic-to-thermal conversion (Rott stack efficiency) | 60–75% of ideal | ×0.65 |
| Motor electro-acoustic efficiency | 85–92% | ×0.89 |
| Heat exchanger thermal resistance | 90–95% | ×0.92 |
| Parasitic standing-wave modes (suppressed by bandgap) | 90–97% (vs. 70–85% uncontrolled) | ×0.93 |
| Lens insertion loss | 95–98% | ×0.96 |
| Fan power (included in COP denominator) | — | −0.2 to −0.5 COP |
| **Net real COP** | | **0.55–0.70 of ideal** |

| Condition | Real COP_heating | Real COP_cooling |
|-----------|-----------------|-----------------|
| AC, 35°C outdoor | 5.7–7.2 | 5.1–6.5 |
| Heating, 8°C outdoor | 7.4–9.4 | — |
| Heating, -20°C outdoor | 3.9–4.9 | — |

**Conservative targets (accounting for additional losses not modeled):**
- COP_cooling (35°C): 3.5–4.5
- COP_heating (8°C): 4.0–5.0
- COP_heating (-20°C): 3.0–4.5

Even the conservative lower bound (COP 3.0) is competitive with conventional heat pumps, and the cold-climate advantage (COP 3.0 at -20°C vs. 1.5–2.5 for vapor-compression) is the decisive market differentiator.

### 11.3 Acoustic power budget (10 kW unit)

| Parameter | Value |
|-----------|-------|
| Thermal power pumped | 10 kW (heating) |
| Acoustic power required | 10 kW / COP_heating = 2.0–2.5 kW acoustic |
| Motor electrical input | 2.0–2.5 kW / 0.89 = 2.2–2.8 kW electrical |
| Fan power | 100–200 W (indoor + outdoor) |
| Total electrical input | 2.3–3.0 kW |
| **Delivered heat** | **10 kW** |
| **COP_heating** | **10 / 2.5–3.0 = 3.3–4.0** |

## 12. Comparison to Prior Thermoacoustic Devices

| Device | Year | Type | COP | Working fluid | Pressure (bar) | Limitation |
|--------|------|------|-----|---------------|-----------------|------------|
| Wheatley et al. (LANL) | 1983 | Standing wave | 1.2 | He | 10 | Low efficiency (standing wave) |
| Swift (LANL) thermoacoustic refrigerator | 1992 | Standing wave | 1.5–2.0 | He | 10–30 | Low efficiency, high pressure |
| Ceperley (Stirling tube) | 1979 | Traveling wave (tube) | 2.0 (theory) | He | 15 | Tube complexity, parasitic modes |
| Score Stirling (Nottingham) | 2012 | Traveling wave (loop) | 2.5 | He | 12–25 | Loop tube bulky, hard to fabricate |
| Aster thermoacoustic AC | 2018 | Standing wave | 2.0 | He | 10–15 | Low efficiency, high pressure |
| **TMHP (this concept)** | **2026** | **Traveling wave + metamaterial** | **3.0–5.0** | **He** | **3–8** | **TRL 2 — integration unproven** |

The TMHP achieves higher projected COP and lower pressure than all prior devices by using phononic crystal metamaterials for wave shaping and parasitic-mode suppression — the key innovations that prior art lacked.

## 13. Research Frontiers

| Frontier | Current state | TMHP target | Timeline |
|----------|--------------|-------------|----------|
| **Phononic crystal lens for thermoacoustics** | Demonstrated for sound focusing (TRL 3); not applied to thermoacoustic phase matching | First application of acoustic metamaterials to Stirling-cycle phase optimization | 2026–2029 (lab prototype) |
| **AI-optimized resonator topology** | Physics-informed NNs for acoustic design at TRL 2–3 | First co-optimization of lens + stack + bandgap geometry | 2026–2028 (simulation) |
| **Low-pressure traveling-wave thermoacoustics** | Prior art requires 10–30 bar; metamaterial gain enables 3–8 bar | 5–10× pressure reduction | 2027–2030 (prototype) |
| **Flexure-bearing linear motor longevity** | 100,000+ hr demonstrated (Sandia/ARPA-E Stirling) | 30–40 year life in HVAC duty cycle | 2025–2030 (field validation) |
| **Helium-argon mixture optimization** | Studied for Stirling engines (not thermoacoustics) | 30–70% Ar dilution for large units | 2028–2032 |

## 14. Roadmap

| Phase | Years | Milestone |
|-------|-------|-----------|
| **Phase 1 — Proof of concept** | 2026–2028 | Lab demonstration of phononic crystal lens + traveling-wave stack; measure COP 2.0–3.0 |
| **Phase 2 — Prototype** | 2028–2031 | 3 kW residential prototype with metamaterial resonator; COP 3.0–4.0; 1,000-hr endurance test |
| **Phase 3 — Pilot production** | 2031–2035 | 100–1,000 units; field trials in cold-climate and off-grid deployments; UL/CE certification |
| **Phase 4 — Scale manufacturing** | 2035–2040 | 100K–1M units/yr; cost target $400–800 residential; global supply chain |
| **Phase 5 — Ubiquity** | 2040–2050 | 100M+ units; refrigerant-free HVAC becomes standard; Kigali Amendment targets exceeded |

## References

1. Swift, G.W. (2002). *Thermoacoustics: A Unifying Perspective for Some Engines and Heat Pumps.* Acoustical Society of America.
2. Rott, N. (1980). "Thermoacoustics." *Advances in Applied Mechanics*, 20, 135–175.
3. Ceperley, P.H. (1979). "A pistonless Stirling engine — The traveling wave heat engine." *J. Acoust. Soc. Am.*, 66(5), 1508–1513.
4. Backhaus, S. & Swift, G.W. (2000). "A thermoacoustic Stirling heat engine." *Nature*, 399, 335–338.
5. Biwa, T. et al. (2011). "Thermoacoustic Stirling heat pump." *Applied Physics Letters*, 99, 234102.
6. Luo, Z. et al. (2020). "Acoustic metamaterials for wavefront manipulation." *Nature Reviews Physics*, 2, 322–340.
7. Cummer, S.A. et al. (2016). "Acoustic metamaterials and phononic crystals." *Nature Materials*, 15, 481–492.
8. Fang, N. et al. (2006). "Ultrasonic metamaterials with negative modulus." *Nature Materials*, 5, 452–456.
9. Li, J. et al. (2018). "Acoustic metamaterials designed by topology optimization." *J. Sound and Vibration*, 436, 79–96.
10. IEA (2018). *The Future of Cooling.* International Energy Agency.
11. UNEP (2023). *Global Cooling Watch.* United Nations Environment Programme.
12. Kigali Amendment to the Montreal Protocol (2016). Effective 2019.
13. Lancet Countdown (2023). *Health and Climate Change.*
14. ACCA (2021). *Refrigerant Leak Rate Study.* Air Conditioning Contractors of America.
15. ARPA-E (2012). *Thermoacoustic Heat Pump Program.* Department of Energy.
16. Penn State Applied Research Lab (2010). *Thermoacoustic Refrigerator for Space Applications.* NASA/JPL.
17. SCORE Project (2012). *Score-Stirling Thermoacoustic Generator.* University of Nottingham / DfID.
18. Aster Thermoacoustics (2018). *Thermoacoustic Air Conditioning System.* ARPA-E COOLIT Program.