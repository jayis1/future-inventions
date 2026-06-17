# APTP — Technical Specification

## 1. System Architecture

### 1.1 Physical Enclosure

| Parameter | Specification |
|-----------|--------------|
| Form factor | 1.8 m H × 0.8 m W × 0.7 m D (standard lab refrigerator footprint) |
| Mass | 85 kg (with reagent cartridges installed) |
| Power | 500W continuous (220V AC / 110V AC / 24V DC solar input) |
| Operating temperature | 15–35°C ambient |
| Containment | ISO Class 7 (Class 10,000) HEPA-filtered internal work area; negative pressure enclosure |
| User interface | 15" touchscreen; voice-guided workflow for low-literacy settings; multi-language (20+ at launch) |
| Connectivity | 4G/LTE, Wi-Fi 6, Ethernet; offline-capable with local AI inference |

### 1.2 Subsystem Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    APTP Enclosure (ISO 7)                    │
│                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │ Pathogen  │  │  Phage   │  │   AI     │  │  Cell-   │  │
│  │Isolation │──│ Discovery│──│Engineering│──│Free Synth│  │
│  │  Module   │  │  Engine  │  │  Module   │  │  Module   │  │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘  │
│       │                                          │         │
│       ▼                                          ▼         │
│  ┌──────────┐                            ┌──────────┐      │
│  │ Nanopore │                            │   QC &   │      │
│  │Sequencer │                            │Formulation│     │
│  └──────────┘                            └──────────┘      │
│                                                │            │
└────────────────────────────────────────────────│────────────┘
                                                 ▼
                                          ┌──────────┐
                                          │ Sterile  │
                                          │  Output  │
                                          │ Vials/   │
                                          │ Nebulizer│
                                          └──────────┘
```

## 2. Pathogen Isolation & Identification Module

### 2.1 Microfluidic Sample Processing

- **Input**: 100 µL patient swab eluate or 1 mL liquid sample
- **Processing**: Differential centrifugation on-chip (magnetofluidic sorting) → bacterial enrichment → single-cell isolation in 10,000-well microwell array
- **Time**: 1 hour from sample to isolated colony

### 2.2 Rapid Genomic Sequencing

- **Platform**: Oxford Nanopore Flongle (integrated)
- **Library prep**: Rapid barcoding kit (10-minute prep, automated)
- **Sequencing**: 30-minute run for species/strain ID + resistome
- **Analysis**: On-device basecalling (GPU-accelerated) + ML species ID + AMR gene detection
- **Output**: Species, MLST type, resistome profile, virulence factor list
- **Accuracy**: >99.5% species ID, >98% resistome gene detection

### 2.3 Target Strain Cultivation

- Microfluidic growth chambers (48 parallel chambers, 10 µL each)
- Controlled atmosphere (aerobic/anaerobic/microaerophilic)
- Optical density monitoring every 5 minutes
- Auto-generates fluorescent reporter strain (luciferase under constitutive promoter) for phage screening

## 3. Phage Discovery Engine

### 3.1 Environmental Sample Processing

- **Input**: 10 mL environmental sample (sewage, river water, soil slurry)
- **Processing**: Sequential filtration (0.45 µm → 0.22 µm) to isolate phage-sized particles → enrichment culture against target strain (4 hours) → plaque assay

### 3.2 High-Throughput Plaque Screening

- **Chip**: PDMS microfluidic chip with 10,000 nanoliter wells
- **Method**: Each well contains target reporter bacteria + diluted phage fraction
- **Detection**: Luciferase fluorescence (real-time, >10× signal-to-noise when lysis occurs)
- **Throughput**: 10,000 wells screened in 30 minutes
- **Hit rate**: Typically 0.5–5% of wells show lysis (50–500 candidate phages per run)
- **Recovery**: Positive wells are flushed to recovery channels for amplification and genome extraction

### 3.3 Candidate Phage Genome Sequencing

- **Platform**: Oxford Nanopore MinION (integrated, dedicated to phage genomes)
- **Library prep**: Automated, on-chip DNA extraction + ligation
- **Sequencing**: 1-hour run per batch of 50 phages
- **Assembly**: On-device Flye assembler + polishing
- **Time**: 2 hours total from hit recovery to complete phage genome

## 4. AI-Guided Engineering Module

### 4.1 Phage Selection Model (PhageFormer)

- **Architecture**: Transformer encoder (12 layers, 768 hidden dim, 12 attention heads)
- **Training data**: 50,000+ annotated phage genomes (NCBI GenBank, PhagesDB, GPD), 200,000+ phage-host interaction records, 10,000+ experimental lysis assays
- **Input**: Phage genome sequence + target bacterium genome + resistome
- **Output**: 
  - Lysis probability (calibrated, AUC > 0.85 on held-out set)
  - Host range prediction (which strains within species will be susceptible)
  - Resistance risk score (estimated generations until escape mutant)
  - Lysogenicity prediction (integrases, repressors, prophage signals)
  - Safety flags (toxin genes, AMR gene carriage, allergenicity)

### 4.2 CRISPR Engineering Design

- **Target modifications**:
  1. **Host range broadening**: Swap tail fiber/receptor-binding protein (RBP) domains to expand or redirect tropism
  2. **Anti-resistance engineering**: Encode anti-CRISPR proteins or depolymerase enzymes targeting bacterial defense systems
  3. **Lysogeny removal**: Delete integrase/repressor genes; enforce strictly lytic cycle
  4. **Payload insertion**: Add biofilm-degrading enzymes (DspB, PelBh) or sensitizing agents (OmpA ligands)
- **Design tool**: In-silico CRISPR guide RNA designer + homology-directed repair template generator
- **Output**: Engineering blueprint (DNA edits + synthesis plan) in <30 minutes

### 4.3 Cocktail Optimization

- Select 3–5 phages targeting independent cell-surface receptors
- Minimize cross-resistance probability (model-estimated)
- Maximize synergistic lytic kinetics (inferred from genome → lysis dynamics model)
- Ensure no immunogenic overlap in capsule depolymerases

## 5. Cell-Free Phage Synthesis (CFPS) Module

### 5.1 DNA Synthesis

- **Method**: Inkjet oligonucleotide synthesis (200 bp → Gibson assembly → full phage genome)
- **Platform**: Custom microfluidic DNA synthesis chip (modified from twist Bioscience silicon chip approach)
- **Capacity**: Genomes up to 250 kb (covers 95% of known phages; largest known lytic phage ~250 kb)
- **Synthesis time**: 8–12 hours (parallel oligo synthesis + error correction + assembly)
- **Error rate**: <1/10,000 bp after enzymatic error correction (ErCC)
- **Cost per genome**: ~$5–10 at scale

### 5.2 Cell-Free Transcription-Translation (CF-Tx)

- **System**: *E. coli* lysate-based (NEB PURExpress-compatible, optimized for phage protein folding)
- **Reaction volume**: 5 mL per phage (standard), up to 20 mL (large tailed phages)
- **Key additives**:
  - GroEL/GroES chaperone mix (2 µM) — essential for proper capsid folding
  - T7 RNA polymerase (for T7-like promoters)
  - E. coli σ⁷⁰ RNA polymerase (native)
  - ATP regeneration system (creatine phosphate + creatine kinase)
  - Trehalose (5% w/v) — protein stability
  - Mg²⁺ optimization buffer (12 mM optimal for most phage morphogenesis)
- **Incubation**: 37°C, 4–6 hours for virion self-assembly
- **Yield**: Target 10⁸–10¹⁰ PFU/mL (current state of art: 10⁶–10⁸ PFU/mL; 100× improvement projected by 2030 with chaperone optimization)
- **Quality**: Virion morphology confirmed by on-device nanopore impedance spectroscopy (size/shape proxy)

### 5.3 Phage Amplification (Yield Boost)

- For phages with low CFPS yield (<10⁶ PFU/mL), a secondary amplification step uses the isolated target strain in a sealed, disposable 10 mL bioreactor pouch (single-use, sterilizable)
- Controlled lysis kinetics: MOI = 0.01, 4-hour infection cycle, 2 passages maximum
- Filtration (0.22 µm) removes bacterial debris before QC
- This backup mode adds 12 hours but ensures therapeutic titer

## 6. Quality Control & Formulation Module

### 6.1 QC Tests (Automated, On-Device)

| Test | Method | Threshold | Time |
|------|--------|-----------|------|
| Phage titer | Drop-plaque assay (microfluidic) | >10⁸ PFU/mL | 8 hours |
| Sterility | Growth in BHI broth (on-chip) | No growth at 48 hrs | 48 hrs (concurrent) |
| Endotoxin | LAL chromogenic assay | <0.5 EU/mL (IV) / <5 EU/mL (topical) | 30 min |
| pH | Micro pH electrode | 6.5–7.5 | 1 min |
| Osmolality | Vapor pressure osmometer | 280–320 mOsm/kg | 5 min |
| Residual DNA | PicoGreen fluorescence | <10 ng/mL | 15 min |
| Morphology | Nanopore impedance spectroscopy | Within 2σ of reference | 15 min |

### 6.2 Formulation Options

| Route | Formulation | Volume | Additives |
|-------|-------------|--------|-----------|
| Intravenous | Sterile isotonic solution (0.9% NaCl) | 10–100 mL vial | 5% trehalose, 1 mM MgSO₄ |
| Topical | Hydrogel dressing (1% carbopol) | 50 mL pump | N/A |
| Inhalation | Nebulizer cartridge | 5 mL | 0.1% Tween 80 (prevent aerosol aggregation) |
| Oral | Enteric-coated capsule (if GI infection) | 10¹⁰ PFU | Alginate encapsulation |

## 7. Real-Time Monitoring & Adaptive Response

### 7.1 Post-Administration Monitoring

- Patient samples at 12-hour intervals for 72 hours
- Nanopore sequencing of bacterial population to detect:
  - Phage-susceptible strain clearance (quantitative)
  - Escape mutant emergence (receptor mutation detection)
  - Secondary infection / dysbiosis
- If escape mutant detected: AI module redesigns cocktail within 4 hours, CFPS produces updated phages within 12 hours → new cocktail ready in **18 hours**

### 7.2 Pharmacokinetic / Pharmacodynamic Model

- On-device PK/PD model (validated against published phage therapy pharmacology data)
- Predicts optimal dosing schedule: initial bolus + maintenance doses
- Tracks phage amplification in vivo (bacterial lysis → phage replication → self-dosing)
- Adjusts for infection site (blood, lung, wound, urinary tract)

## 8. Consumable Cartridges

### 8.1 Patient Cartridge (Single-Use, Per-Course)

| Component | Specification |
|-----------|--------------|
| Environmental sample vial | 15 mL, sterile |
| Patient sample vial | 2 mL, transport medium |
| CF-Tx reagent pack | 5 × 5 mL reactions (for 5 phages) |
| DNA synthesis chip | 1 × 250 kb capacity |
| Microfluidic screening chip | 1 × 10,000-well |
| Bioreactor pouch (backup) | 1 × 10 mL |
| Formulation supplies | Vials, labels, sterile connectors |
| Shelf life | 18 months at 4–30°C |
| Cost target | $50–80 at 100K units/year |

### 8.2 Service Cartridge (Monthly)

- QC calibration standards
- HEPA filter replacement
- Nanopore flow cell (Flongle × 2)
- CF-Tx lysate master mix (bulk)
- Waste collection container

## 9. Safety & Dual-Use Safeguards

### 9.1 Biosecurity Locks

- **DNA synthesis screening**: All synthesis orders checked against curated pathogenic gene database (virulence factors, toxins, AMR genes); synthesis blocked for matches
- **Access logging**: Every cartridge, synthesis, and output logged with timestamp, user ID, and target pathogen
- **Hardware interlock**: Synthesis module will not operate without valid patient sample ID (linked to clinical record)
- **Phage genome review**: AI module flags any phage genome carrying integrase, repressor, toxin, or AMR genes for manual review; auto-rejects lysogenic candidates
- **Remote audit**: Encrypted telemetry sent to public health authority (opt-in; required in some jurisdictions)

### 9.2 Environmental Safeguards

- All waste streams heat-inactivated (85°C, 30 min) before disposal
- Phage output is strictly lytic (no lysogenic phages released)
- Phages are target-specific (narrow host range by design, reducing ecological impact)
- Built-in kill-switch: phages engineered with thermolabile capsid mutations (denature above 50°C, ensuring no environmental persistence in tropical waterways)

## 10. Performance Benchmarks

| Metric | Target | Current Best (Manual) |
|--------|--------|----------------------|
| Time from sample to therapy | ≤48 hours | 2–16 weeks |
| Cost per course | $50–150 | $30,000–100,000 |
| Personnel required | 1 nurse (trained) | 5 PhDs + lab techs |
| Facility requirement | District hospital | BSL-2 reference lab |
| Phage cocktail diversity | 3–5 phages per cocktail | 1–12 (variable) |
| Success rate (clearance) | >80% (target) | 60–80% (published) |
| Resistance emergence detection | 12-hour intervals | Days to weeks |
| Cold chain requirement | 4–30°C storage | -80°C (frozen phage stocks) |
| Annual throughput per unit | 200–500 patients | 10–50 patients |

## 11. Materials & Supply Chain

### 11.1 Key Materials

| Material | Source | Scalability | Cost Trajectory |
|----------|--------|-------------|-----------------|
| *E. coli* CF-Tx lysate | Biomanufacturing (NEB/commercial) | High (commodity) | Declining ($5/mL → $1/mL by 2030) |
| DNA synthesis reagents | Phosphoramidite chemistry | High | Declining |
| PDMS microfluidic chips | Injection molding | High | <$1/chip at 100K/yr |
| Oxford Nanopore Flongle | Commercial | Medium | $90/flow cell |
| Trehalose, MgSO₄, buffers | Commodity chemicals | Very high | Negligible |
| Sterile vials/pouches | Medical packaging | Very high | $0.10–0.50/unit |

### 11.2 Manufacturing

- APTP units: Contract manufacturing (Thermo Fisher / Danaher OEM), estimated 10K units/year by 2035
- Cartridges: High-speed automated filling lines (similar to insulin pen manufacturing)
- Microfluidic chips: Soft lithography → injection molding transition (same path as pregnancy test strips)

## 12. Software & AI

### 12.1 PhageFormer Model

- **Training**: Pre-trained on NCBI GenBank (all phage genomes), PhagesDB, GPD, and proprietary interaction datasets from clinical phage therapy centers
- **Architecture**: Modified ESM-2 (protein language model) + custom genome-level transformer
- **Inference**: On-device (NVIDIA Jetson Orin, 40 TOPS, 15W); cloud backup for complex cases
- **Update cycle**: Monthly model updates via encrypted channel; retraining on new phage-host data quarterly
- **Explainability**: Attention maps and feature attribution for every prediction (clinician-facing UI)

### 12.2 Regulatory Intelligence Module

- Continuously updated database of phage therapy regulations by country
- Auto-generates required documentation for local regulatory submission
- Tracks evolving FDA/EMA/WHO guidance on personalized biologics

---

*Specification v1.0 — 2026-06-17 — Adaptive Phage Therapeutics Platform*