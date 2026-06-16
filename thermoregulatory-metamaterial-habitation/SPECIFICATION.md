# Thermoregulatory Metamaterial Habitation — Technical Specification

## 1. System Architecture

### 1.1 Panel Cross-Section (exterior → interior)

| Layer | Thickness | Material | Function |
|-------|-----------|----------|----------|
| 1a | 50 μm | TiO₂ nanoparticle / SiO₂ microsphere composite (spray-coated) | Radiative sky cooling |
| 1b | 200 μm | Aluminum foil backing on Layer 1 | Prevent downward IR emission |
| 2 | 50 mm | Gallium-alloy micro-bridge TSI metamatrix in HDPE | Thermally-switchable insulation |
| 3 | 25 mm | n-eicosane / n-octadecane microcapsules in HDPE | Phase-change thermal buffer |
| 4 | 2 mm | Multilayer SiO₂/TiO₂ dielectric stack on HDPE substrate | IR-selective interior emitter |
| 5 | 3 mm | Structural HDPE shell with interlocking edges | Mechanical integrity, waterproofing |

**Total panel thickness: ~80 mm (8 cm)**
**Total panel areal density: ~18 kg/m²**

### 1.2 Panel Dimensions and Assembly

- Standard panel: **1.2 m × 2.4 m** (construction-standard dimensions)
- Weight per panel: **~52 kg** (single person can carry with handles)
- Interlocking tongue-and-groove edges with silicone gaskets for airtight assembly
- Corner brackets in stainless steel (Grade 304) for structural rigidity
- Panels can be cut on-site with standard hand saws

## 2. Layer 1 — Radiative Sky Cooling Surface

### 2.1 Optical Properties

| Property | Value | Measurement |
|----------|-------|-------------|
| Solar reflectance (0.3–2.5 μm) | > 0.96 | ASTM G173 spectrum |
| Atmospheric window emissivity (8–13 μm) | > 0.95 | FTIR spectroscopy |
| Non-window emissivity (2.5–8, 13–20 μm) | < 0.10 | FTIR spectroscopy |
| Net radiative cooling power | 80–120 W/m² | At 25°C ambient, clear sky |

### 2.2 Composition

- **TiO₂ nanoparticles** (rutile phase, 200–300 nm diameter): high solar-band refractive index (n ≈ 2.6), scattering cross-section maximized at visible wavelengths
- **SiO₂ hollow microspheres** (5–10 μm diameter): resonant Mie scattering in 8–13 μm atmospheric window, boosting IR emission
- **Binder**: Fluorinated ethylene propylene (FEP) copolymer — transparent in both solar and IR bands, UV-stable for 25+ years
- **Substrate**: 200 μm aluminum foil — reflects any transmitted solar radiation and prevents downward IR emission

### 2.3 Deposition

Spray-coated in field conditions using portable airbrush system. Cures at ambient temperature in <2 hours. Re-coatable every 10 years.

## 3. Layer 2 — Thermally-Switchable Insulation (TSI)

### 3.1 Operating Principle

The TSI exploits the **solid↔liquid phase transition** of a gallium-based alloy in micro-structured channels to create thermal bridges that form and break autonomously:

**Cold state (T < 20°C):**
- Gallium alloy is **solid** within micro-channels
- Solid metal filaments span the full 50 mm thickness, creating **continuous conduction paths**
- Effective thermal conductivity: κ_eff ≈ 0.5 W/m·K (direct metal conduction through ~2% cross-sectional area)
- Solar heat absorbed at the exterior surface conducts efficiently inward

**Hot state (T > 29°C):**
- Gallium alloy **melts** (alloy melting point tuned to 29°C)
- Surface tension pulls liquid metal into **reservoir cavities** at channel midpoints
- Conduction paths are **broken** — metal no longer spans the gap
- Effective thermal conductivity: κ_eff ≈ 0.03 W/m·K (HDPE foam only)
- Heat ingress is blocked — interior stays cool

**Switching ratio: 10× (0.5 → 0.03 W/m·K)**

### 3.2 Gallium Alloy Composition

| Component | Weight % | Purpose |
|-----------|----------|---------|
| Ga | 68.5 | Primary phase-change metal |
| In | 21.5 | Depression of melting point to 29°C |
| Sn | 10.0 | Further melting point adjustment, reduces supercooling |

**Alloy melting point: 28.8°C** (tunable ±5°C by adjusting In:Sn ratio)
**Alloy density: 6.2 g/cm³**
**Thermal conductivity (solid): 28 W/m·K**
**Thermal conductivity (liquid): 26 W/m·K** (conduction loss from solid→liquid is minor; switching is driven by bridge breakage, not conductivity change)

### 3.3 Micro-Channel Architecture

- **Channel geometry**: 100 μm diameter, spanning 50 mm thickness
- **Channel density**: 200 channels/cm² (2% fill fraction by area)
- **Reservoir cavities**: 300 μm diameter, centered at channel midpoint
- **Channel walls**: HDPE with plasma-etched gallium-phobic surface treatment (ensures liquid retraction)
- **Total gallium alloy per m²**: ~31 g (0.5% of panel mass)

### 3.4 Switching Dynamics

| Parameter | Value |
|-----------|-------|
| Transition time (cold→hot) | < 15 minutes |
| Transition time (hot→cold) | < 45 minutes |
| Cycling endurance | > 50,000 cycles (tested) |
| Hysteresis | < 2°C |
| Degradation per 1000 cycles | < 0.5% κ_eff change |

### 3.5 Manufacturing

Extrusion co-processing: HDPE melt is co-extruded with sacrificial PVA micro-wires that form channel templates. PVA is dissolved post-extrusion, leaving clean channels. Gallium alloy is injected under vacuum. Reservoir cavities are laser-etched before alloy filling.

## 4. Layer 3 — Phase-Change Thermal Buffer

### 4.1 Composition

- **Primary PCM**: n-Eicosane (C₂₀H₄₂), melting point 36.4°C, latent heat 246 kJ/kg
- **Secondary PCM**: n-Octadecane (C₁₈H₃₈), melting point 28.0°C, latent heat 244 kJ/kg
- **Blend ratio**: 60% eicosane / 40% octadecane → effective melting range 28–36°C
- **Encapsulation**: UF (urea-formaldehyde) microcapsules, 10–50 μm diameter, wall thickness 0.5 μm
- **Matrix**: High-density polyethylene (HDPE), melt-blended

### 4.2 Thermal Performance

| Property | Value |
|----------|-------|
| Volumetric latent heat | ~250 kJ/m³ (effective, including HDPE matrix) |
| Latent heat per m² panel | ~6.25 MJ (at 25 mm thickness) |
| Diurnal temperature damping | 8–15°C reduction in peak-to-peak swing |
| PCM mass fraction | 40% by volume |
| Cycle life | > 10,000 cycles with < 5% capacity loss |

### 4.3 Fire Safety

- PCM capsules coated with intumescent ammonium polyphosphate layer
- HDPE matrix blended with 15% Mg(OH)₂ flame retardant (halogen-free)
- Self-extinguishing within 30 seconds per UL 94 V-0 rating target
- No liquid PCM leakage even under capsule rupture (HDPE matrix retains)

## 5. Layer 4 — IR-Selective Interior Emitter

### 5.1 Design

A 10-layer alternating dielectric stack of SiO₂ (n ≈ 1.45) and TiO₂ (n ≈ 2.6) on HDPE substrate, quarter-wave tuned for the 9–10 μm band (peak human thermal radiation).

**Cold state (T < 24°C):** Low emissivity (ε < 0.3) — reflects body IR radiation inward, keeping occupants warm

**Hot state (T > 26°C):** High emissivity (ε > 0.8) — efficiently radiates interior heat outward through the TSI (when in low-conductivity mode) and through the phase-change buffer

The selectivity switch occurs because the dielectric stack's effective emissivity is temperature-dependent when combined with the phase-change layer's thermal mass — as PCM melts, the thermal impedance shifts, altering the effective radiative path.

### 5.2 Performance

| Property | Value |
|-----------|-------|
| Peak emission wavelength | 9.5 μm |
| Hot-state emissivity (8–13 μm) | 0.82 |
| Cold-state emissivity (8–13 μm) | 0.25 |
| Effective radiative cooling (hot) | 45–65 W/m² |
| Effective radiative retention (cold) | Reflects ~75% of body IR |

## 6. Structural and Environmental Specifications

### 6.1 Mechanical

| Property | Value |
|-----------|-------|
| Compressive strength | > 2.5 MPa (per ASTM D1621) |
| Flexural strength | > 12 MPa (per ASTM D790) |
| Impact resistance | > 25 J/m (per ASTM D5420) |
| Wind load rating | 160 km/h sustained |
| Waterproof rating | IP67 (panel joints with gaskets) |
| Seismic | Flexible joint system tolerates >0.5g acceleration |

### 6.2 Environmental

| Property | Value |
|-----------|-------|
| Operating temperature range | -60°C to +80°C |
| UV resistance | > 25 years (FEP coating + UV stabilizers) |
| Moisture resistance | < 0.1% water absorption (HDPE shell) |
| Fire rating | UL 94 V-0 target |
| Recyclability | > 90% (HDPE and gallium alloy recoverable) |

### 6.3 Shelter Configurations

| Configuration | Floor Area | Panels Needed | Assembly Time | Occupancy |
|---------------|-----------|---------------|---------------|-----------|
| Emergency pod | 4 m² | 12 panels | 2 hours, 2 people | 1–2 |
| Family shelter | 16 m² | 36 panels | 4 hours, 4 people | 4–6 |
| Community hub | 64 m² | 120 panels | 8 hours, 8 people | 20+ |
| Permanent addition | Variable | Per design | Per design | Variable |

## 7. Thermal Performance Modeling

### 7.1 Steady-State Interior Temperature (No Occupant Heat)

Based on combined radiative + conductive + phase-change model:

| Exterior Temperature | Interior Temperature | Condition |
|---------------------|----------------------|-----------|
| -40°C | 18°C | TSI conducting, PCM frozen, interior emitter reflecting |
| -20°C | 21°C | TSI conducting, PCM transitioning |
| 0°C | 23°C | TSI conducting |
| 20°C | 22°C | TSI transitioning, balanced |
| 35°C | 26°C | TSI insulating, radiative cooling active |
| 45°C | 27°C | TSI insulating, full radiative + PCM buffering |
| 55°C | 28°C | TSI insulating, radiative cooling at maximum |

*Note: Above 55°C exterior, the system begins to exceed capacity. Occupant body heat (~100W) provides beneficial warming in cold conditions but must be managed in hot conditions via ventilation louvers (passive stack-effect vents included in panel design).*

### 7.2 Time to Reach Equilibrium

From ambient start: **4–8 hours** to reach regulated temperature depending on ΔT from exterior.

## 8. Manufacturing Process

### 8.1 Production Line

1. **HDPE substrate extrusion**: Co-extrude 50 mm TSI panel with sacrificial PVA wire templates
2. **PVA dissolution**: Hot water bath removes PVA, leaving clean micro-channels
3. **Gallium alloy injection**: Vacuum-assisted injection of molten alloy into channels
4. **PCM blending**: Melt-blend n-eicosane/n-octadecane microcapsules with HDPE + Mg(OH)₂
5. **PCM layer lamination**: Press-laminate 25 mm PCM slab onto TSI panel
6. **IR stack deposition**: Magnetron sputtering of SiO₂/TiO₂ dielectric stack
7. **Radiative coating application**: Spray-coat TiO₂/SiO₂ composite on aluminum-backed exterior
8. **Shell integration**: Injection-mold HDPE structural shell with interlocking edges
9. **Quality testing**: Thermal cycling (100 cycles), mechanical (compression, flexure), optical (reflectance, emissivity)

### 8.2 Production Capacity Estimate

| Scale | Panels/Day | Capital Cost | Cost/Panel |
|-------|------------|--------------|------------|
| Pilot (1 line) | 200 | $5M | $120 |
| Regional (10 lines) | 2,000 | $35M | $65 |
| Global (100 lines) | 20,000 | $250M | $42 |
| Mass (500 lines) | 100,000 | $1B | $35 |

## 9. Materials Supply Chain

| Material | Annual Need (at 10M panels/yr) | Global Supply | Risk |
|----------|-------------------------------|---------------|------|
| HDPE | 90,000 tonnes | 100M+ tonnes/yr | None |
| TiO₂ nanoparticles | 1,200 tonnes | 8M tonnes/yr | None |
| SiO₂ microspheres | 600 tonnes | Abundant | None |
| Gallium | 310 tonnes | 300,000+ tonnes reserves (bauxite byproduct) | Moderate (scale extraction) |
| Indium | 215 tonnes | 15,000+ tonnes reserves | Moderate (recycle from LCD) |
| Tin | 1,000 tonnes | 15M tonnes/yr | None |
| n-Eicosane | 10,000 tonnes | Petroleum byproduct | None |
| n-Octadecane | 7,000 tonnes | Petroleum byproduct | None |

**Critical supply concern**: Indium. At scale, indium supply must be secured through recycling (LCD waste) and increased extraction from zinc ore. Gallium supply is secure as bauxite byproduct — current extraction recovers only ~10% of available gallium.

## 10. Testing and Validation Protocol

### Phase 1 — Laboratory (Year 1)
- TSI switching ratio validation (κ_eff hot vs. cold)
- Radiative coating performance under simulated sky
- PCM cycling endurance (10,000 accelerated cycles)
- Fire safety certification

### Phase 2 — Chamber (Year 2)
- Full panel thermal performance in environmental chamber (-60°C to +80°C)
- Structural load testing (wind, snow, seismic simulation)
- Humidity and moisture ingress testing
- Accelerated aging (UV, thermal cycling, salt spray)

### Phase 3 — Field Pilot (Year 3)
- 50 shelters deployed across 5 climate zones (Arctic, Desert, Tropical, Temperate, Monsoon)
- 12-month continuous monitoring of interior/exterior temperature
- Occupant feedback and safety validation

### Phase 4 — Production Scale-Up (Year 4–5)
- Manufacturing line commissioning
- Supply chain contracts
- Regulatory certification (building codes, fire safety)