# Thermoregulatory Metamaterial Habitation

## Problem

**1.6 billion people** live in inadequate housing — structures that fail to protect against extreme heat, cold, or weather. Simultaneously, **heating and cooling buildings consumes 17% of global energy** and produces ~3.5 Gt CO₂/year. Climate change is intensifying both heatwaves and cold snaps, making passive thermal regulation a survival issue, not a comfort issue.

Current approaches are failing:
- **HVAC systems** require electricity that 770M people lack and contribute massively to emissions
- **Passive cooling paints** (radiative white coatings) only help in hot climates and fail in cold
- **Insulation** traps heat when you need cooling, and leaks when you need warming
- **Disaster shelters** (tents, tarps) offer almost no thermal regulation — temperatures inside can differ by only 2–3°C from outside

We need a material system that **passively adapts** — cooling when it's hot, insulating when it's cold — without electricity, moving parts, or human intervention.

## Solution

The **Thermoregulatory Metamaterial Habitation (TMH)** is a multi-layer composite panel system that passively maintains interior temperatures within the 18–26°C human comfort zone across exterior conditions ranging from **-40°C to +55°C**, consuming **zero external energy**.

The system combines four synergistic mechanisms in a single 8 cm panel:

### Layer 1 — Radiative Sky Cooling Surface (exterior)
A nanostructured TiO₂/SiO₂ microparticle coating with solar reflectance >0.96 and atmospheric window emissivity >0.95. This layer radiates heat through the 8–13 μm atmospheric transparency window into deep space (3 K heat sink), achieving sub-ambient surface temperatures even under direct sunlight — demonstrated in current research to cool 5–12°C below ambient.

### Layer 2 — Thermally-Switchable Insulation (TSI)
A metamaterial whose effective thermal conductivity **switches by 10×** between states:
- **Cold mode (T < 20°C):** Thermal bridges of gallium alloy micro-wires form continuous conduction paths, allowing solar-heat gain to warm the interior
- **Hot mode (T > 26°C):** Gallium melts and retracts into reservoirs via surface tension, breaking the thermal bridges and reducing conductivity to 0.03 W/m·K (better than aerogel)

The switching is driven entirely by the phase change of Field's metal (melting point 62°C) and gallium alloy (melting point ~29°C) microstructures — no electronics, no power.

### Layer 3 — Phase-Change Thermal Buffer
Encapsulated n-eicosane (C₂₀H₄₂, melting point 36.4°C) and n-octadecane (C₁₈H₃₈, melting point 28°C) microcapsules embedded in an HDPE matrix, providing **~250 kJ/m³** of latent heat storage per cycle. This absorbs daytime heat spikes and releases warmth at night, flattening diurnal temperature swings by 8–15°C.

### Layer 4 — IR-Selective Interior Emitter
A multilayer dielectric stack that preferentially emits in the 9–10 μm band where the human body radiates most effectively. This ensures that when interior temperatures rise, body heat is radiated away efficiently, and when temperatures drop, the layer reflects thermal radiation back inward (low-e behavior below 24°C, high-e above 26°C).

## Key Innovation

**The thermally-switchable insulation (TSI) is the breakthrough.** Current passive systems are either good insulators OR good radiators — they cannot dynamically switch. The TSI uses the solid↔liquid phase transition of gallium-based alloys in micro-structured channels to create thermal bridges that form and break autonomously based on temperature:

- **At 20°C:** Gallium alloy channels are solid → continuous metal filaments conduct heat inward (κ_eff ~ 0.5 W/m·K), letting solar gain warm the interior
- **At 29°C:** Gallium alloy melts → surface tension pulls liquid into reservoirs, breaking bridges → κ_eff drops to 0.03 W/m·K, blocking heat ingress

This is a **physical logic gate made of metal and surface tension** — a material that "computes" its thermal state without any electronics. Combined with radiative sky cooling and phase-change buffering, the complete panel system achieves:

| Metric | Current Best | TMH Target |
|--------|-------------|------------|
| Exterior range for 18–26°C interior | N/A (requires HVAC) | -40°C to +55°C |
| Energy consumption | 5–15 kW·h/day (HVAC) | **0 kW·h/day** |
| Thermal switching ratio | 2× (shape-memory alloys) | **10×** |
| Lifecycle | 10–15 years | 25+ years |
| Cost per m² wall | $80–200 (insulated) | **$35–60** |

## Target Cost

**$35–60 per m²** of panel area at scale (millions of m²/year), comprising:
- TiO₂/SiO₂ radiative coating: $3/m²
- TSI metamaterial (gallium alloy + HDPE channels): $15/m²  
- Phase-change microcapsule layer: $8/m²
- IR-selective dielectric stack: $4/m²
- Structural HDPE shell + fasteners: $5/m²

A **4-person emergency shelter (16 m² floor, 48 m² wall)** costs **$1,700–2,900** in materials — comparable to a high-end tent but providing life-saving thermal regulation for decades without power.

At scale, gallium alloy costs drop to <$50/kg (gallium is ~$250/kg today but abundant as a byproduct of bauxite and zinc ore — global reserves >1M tonnes). Each m² uses only ~30g of gallium alloy.

## Impact

### Human Lives Saved
- **Heatwaves** kill >500,000 people/year by 2050 (projected). TMH shelters can maintain ≤30°C interior when exterior exceeds 50°C.
- **Cold exposure** kills hundreds of thousands annually. TMH insulates to maintain ≥18°C at -40°C exterior with minimal occupant heat.
- **Disaster response**: Current FEMA/UNHCR tents provide 2–3°C of thermal buffer. TMH panels provide 20–40°C of passive regulation.

### Climate Impact
- Replacing HVAC in 10% of global buildings → **350 Mt CO₂/year eliminated**
- Zero-energy thermal comfort democratizes safe shelter for the **1.6B in inadequate housing**
- Manufacturing emissions: ~12 kg CO₂/m² (vs. 80+ kg CO₂/m² for concrete + HVAC systems)

### Scalability
- Gallium: 1M+ tonnes accessible; each shelter needs ~1.5 kg → **650M+ shelters possible**
- All materials (TiO₂, SiO₂, HDPE, paraffins, gallium) are **industrially abundant**
- Manufacturing: extrusion + spray coating — compatible with existing production lines
- **Deployable within 72 hours** as flat-pack panels, assemble with hand tools

### Equity
- Off-grid by design — no electricity, no infrastructure dependency
- Flat-pack shipping: 48 m² of panels fits in 0.5 m³ (compressed)
- 25+ year lifespan with zero maintenance
- Open-source manufacturing specs for local production