# In-Silico Homology Modeling, Molecular Docking & Industrial Formulation of Phytochemical H2R Antagonists for GERD

[![Target: Human H2R](https://img.shields.io/badge/Target-Human_H2R_(UniProt:P25021)-00557f.svg)](https://www.uniprot.org/uniprotkb/P25021/entry)
[![Methodology: SWISS-MODEL & AutoDock 4](https://img.shields.io/badge/Methodology-SWISS--MODEL_%26_AutoDock_4-brightgreen.svg)](https://autodock.scripps.edu/)
[![ADMET: admetSAR & pkCSM](https://img.shields.io/badge/ADMET-admetSAR_%26_pkCSM-orange.svg)](#pharmacokinetic--admet-profiling)
[![Application: Industrial Hard Candy](https://img.shields.io/badge/Application-Industrial_Hard_Candy_Formulation-blueviolet.svg)](#industrial-formulation--manufacturing-pipeline)

---

## 📌 Executive Summary

Gastroesophageal Reflux Disease (GERD) is a prevalent gastrointestinal motility and acid-peptic disorder characterized by mucosal damage and reflux of gastric contents. This project presents an integrated in-silico drug discovery, comparative molecular docking, ADMET screening, and industrial formulation pipeline to develop a functional phytochemical-based hard candy targeting the Human Histamine $H_2$ Receptor ($H_2R$).

By integrating homology modeling, energy minimization, docking simulations against standard controls, and full industrial scaling calculations, this study establishes safe, bioavailable, and potent natural antagonists for gastric acid suppression.

---
## 🔬 Computational Pipeline & Methodology
* Phase 1: Target Preparation & 3D Homology Modeling (SWISS-MODEL & SPDBV GROMOS96)
* Phase 2: Bioactive Phytochemical Library Construction (PubChem & MM2 Energy Minimization)
* Phase 3: Molecular Docking & Benchmark Validation (AutoDock 4 / LGA with 50 runs per ligand)
* Phase 4: Pharmacokinetic & ADMET Safety Profiling (pkCSM & admetSAR)
* Phase 5: Industrial Scale-Up & Formulation Design (Hard Candy Matrix & Vacuum Cooking)
---
### 1. Target Preparation & Homology Modeling
* Receptor: Human Histamine $H_2$ Receptor ($H_2R$).
* Accession: UniProtKB: P25021 (359 amino acids).
* 3D Structural Generation: Modeled via SWISS-MODEL homology algorithms.
* Energy Minimization: Refined with Swiss-PdbViewer (SPDBV) using the GROMOS96 force field to eliminate steric clashes and resolve backbone geometry.
* Structural Validation: Verified via Ramachandran Plot analysis to ensure core-region conformational validity.

### 2. Ligand Preparation & Energy Minimization
* Multi-source bioactive phytochemical library curated from gastroprotective medicinal plants (*Glycyrrhiza glabra*, *Plantago major*, *Ceratonia siliqua*, *Terminalia chebula*, *Anethum graveolens*, *Mentha*, etc.).
* 3D structures constructed and energy-minimized using MM2 force field geometry optimization.

### 3. Molecular Docking Setup (AutoDock 4 / Cygwin Environment)
* Docking Engine: AutoDock 4 (v4.2.6) executed in Cygwin environment.
* Search Algorithm: Lamarckian Genetic Algorithm (LGA) with 50 independent runs per ligand for rigorous conformational convergence.
* Grid Box Dimensions: $60 \times 82 \times 70$ grid points along $X, Y, Z$ with $0.375\ \text{Å}$ spacing centered on the binding pocket ($X = -70.952, Y = 421.879, Z = 24.178$).

---

## 📊 Key Findings: Comparative Docking & Benchmark Controls

The binding affinities of screening leads were benchmarked against native substrates, pharmaceutical antagonist controls, and reference herbal compounds:

| Compound Role | Compound Name | Source / Category | Binding Energy ($\Delta G$, kcal/mol) | Inhibition Constant ($K_i$) |
|:---|:---|:---|:---:|:---:|
| Natural Substrate | Histamine | Endogenous Agonist | $-4.73$ | $339.6\ \mu\text{M}$ |
| Synthetic Drug Control | Icotidine | Reference $H_2R$ Antagonist | $-8.42$ | $673.2\ \text{nM}$ |
| Plant Reference Control | Liquiritin (A1) | *Glycyrrhiza glabra* | $-10.36$ | $25.4\ \text{nM}$ |
| Top Screening Lead | Acteoside (S1) | *Plantago major* | $-14.36$ | $29.9\ \text{pM}$ |
| Top Screening Lead | Galactomannan (B1) | *Ceratonia siliqua* | $-13.06$ | $270.8\ \text{pM}$ |
| Top Screening Lead | Corilagin (AI1) | *Terminalia chebula* | $-11.18$ | $6.33\ \text{nM}$ |
| Top Screening Lead | Quercetin glucuronide (K5)| *Anethum graveolens* | $-10.87$ | $10.7\ \text{nM}$ |

---

## 💊 Pharmacokinetic & ADMET Profiling

Selected lead candidates were screened through admetSAR and pkCSM:
* Human Intestinal Absorption (HIA): Demonstrated high gastrointestinal permeation profiles.
* Safety & Cardiotoxicity: Negative for hERG I/II potassium channel inhibition risk in top leads.
* Toxicity Endpoints: Verified negative for mutagenicity (Ames test) and low acute/sub-chronic mammalian oral toxicity.

---

## 🏭 Industrial Formulation & Manufacturing Pipeline

Unlike purely academic screenings, this project engineered a complete industrial production model for a functional Hard Candy (Lozenges):
1. Carrier Matrix: Sucrose, liquid glucose syrup ($42\ \text{DE}$), purified deionized water.
2. Standardized Herbal Extracts: Aqueous-ethanolic percolator extraction with standardized polyphenol/flavonoid ratios.
3. Thermal Processing: High-vacuum cooker processing ($135\text{--}140^\circ\text{C}$) to minimize thermal degradation of polyphenols.
4. Forming & Packaging: Rotary die-forming line with individual moisture-barrier pillow-pack sealing.

---

## 👥 Project Background & Team Attribution

* Academic / Training Context: BioCamp (Spring 2021 / 1400) – Advanced Industrial Drug Discovery & Bioinformatics Pipeline.
* Collaborative Research Team: Equal collaborative contributions across target homology modeling, docking simulations, pharmacokinetic evaluation, and formulation design:
* * Taban Tavanmand *(documented as Atefeh Tavanmand in original academic course records)*
  * Samaneh Kazem
  * Mahya Mohammadzaheri

---

## 📂 Repository Structure
```text
anti-reflux-h2r-phytochemical-screening/
├── README.md                 # Full project documentation and technical report
└── figures/                   # 2D/3D interaction diagrams, Ramachandran plots (in progress)
