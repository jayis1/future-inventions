# Atmospheric Water Harvester — Technical Specification

## Core Mechanism

### Sorbent Cycle
1. **Night phase (adsorption):** MOF-303 panels expose to ambient air. Water molecules adsorb into nanopores (pore size 0.6-1.0 nm). Adsorption is exothermic and spontaneous at RH > 10%.
2. **Day phase (desorption):** Solar absorber plate heats MOF to 65-80°C. Adsorbed water desorbs as vapor.
3. **Condensation:** Vapor contacts condenser coil at ambient temperature. Liquid water drips into collection reservoir.
4. **Filtration:** Activated carbon + UV-C LED final sterilization.

### Materials

| Component | Material | Specs |
|-----------|----------|-------|
| Sorbent panel | MOF-303 (Aluminum fumarate) | 0.5 kg/m², 0.45 g/g water uptake at 30% RH |
| Solar absorber | Black chromium on aluminum | α=0.96, ε=0.08 |
| Condenser | Copper microchannel | 40 m²/m³ surface area |
| Housing | Recycled HDPE | UV-stabilized, 10-year life |
| Sterilizer | UV-C LED (265nm) | 30mW, 5-min cycle per liter |

### Performance Targets

| Metric | Household Unit | Village Unit |
|--------|---------------|--------------|
| Daily output (20% RH) | 20 L | 10,000 L |
| Daily output (50% RH) | 45 L | 22,500 L |
| Panel area | 3.3 m² | 1,660 m² |
| Weight | 12 kg | Modular |
| Solar input | 600 W/m² peak | Same |
| Water quality | WHO potable standard | Same |
| Service life | 10 years | 10 years |

### Energy Budget

- **Total:** ~0.3 kWh/L (thermal, from solar — no grid)
- **Electrical:** UV-C LED only — 0.15 Wh/L (tiny solar cell + battery)

### Manufacturing

- MOF-303 synthesis: aluminum nitrate + fumaric acid, hydrothermal, 24h at 65°C
- Scalable to 100 tons/year with continuous flow reactors
- MOF recyclable: wash with ethanol, reactivate at 150°C