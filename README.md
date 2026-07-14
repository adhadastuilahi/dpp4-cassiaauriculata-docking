# dpp4-cassiaauriculata-docking
# Discovery of Potential DPP-4 Inhibitors from *Cassia auriculata* Through Dual Molecular Docking with GNINA and PLANTS

## Overview

This repository contains the complete computational workflow used to identify potential dipeptidyl peptidase-4 (DPP-4) inhibitors from *Cassia auriculata* phytochemicals using a consensus molecular docking strategy. The workflow integrates ligand preparation, molecular docking with GNINA and PLANTS, and consensus analysis to prioritize promising phytochemicals for further investigation.

---

## Workflow

```
Literature Mining
        │
        ▼
Compound Library Construction
        │
        ▼
PubChem Search
(SMILES & CID Retrieval)
        │
        ▼
Ligand Preparation
(RDKit)
        │
        ▼
Protein Preparation
(DPP-4, PDB ID: 5Y7H)
        │
        ▼
───────────────────────────────
│                             │
▼                             ▼
GNINA Docking           PLANTS Docking
│                             │
└──────────────┬──────────────┘
               ▼
Merge Docking Results
               │
               ▼
Min–Max Normalization
               │
               ▼
Pearson Correlation
Spearman Correlation
               │
               ▼
Venn Analysis
(Top 20 Compounds)
               │
               ▼
Consensus Scoring
               │
               ▼
Hit Compound Visualization
(2D Chemical Structures)
```

---

# Repository Structure

```
.
├── Chapter 1 - Ligand Preparation.ipynb
├── Chapter 2 - Molecular Docking Using GNINA and PLANTS.ipynb
├── Chapter 3 - Consensus Analysis of Molecular Docking Results.ipynb
│
├── data/
│
├── ligands/
│
├── protein/
│
├── docking_results/
│
├── consensus_results/
│
├── figures/
│
└── README.md
```

---

# Chapter Description

## Chapter 1 – Ligand Preparation

Preparation of *Cassia auriculata* phytochemicals prior to molecular docking.

Main workflow:

- PubChem CID retrieval
- Canonical SMILES retrieval
- 3D structure generation using RDKit
- Hydrogen addition
- Geometry optimization (MMFF94)
- Export to PDB format

---

## Chapter 2 – Molecular Docking Using GNINA and PLANTS

Automated virtual screening of the prepared ligand library against the DPP-4 crystal structure (PDB ID: 5Y7H).

Main workflow:

- Batch docking with GNINA
- Batch docking with PLANTS
- Automatic extraction of docking scores
- Generation of docking summary tables

---

## Chapter 3 – Consensus Analysis

Post-docking analysis integrating results obtained from GNINA and PLANTS.

Main workflow:

- Merge docking results
- Min–Max normalization
- Pearson correlation analysis
- Spearman correlation analysis
- Scatter plot visualization
- Venn diagram analysis
- Consensus score calculation
- Compound ranking
- Generation of 2D chemical structures from Canonical SMILES

---

# Software Requirements

- Python 3.11+
- Google Colab
- PubChemPy
- RDKit
- Open Babel
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- matplotlib-venn

Docking software:

- GNINA
- PLANTS

---

# Target Protein

| Property | Description |
|-----------|-------------|
| Target | Dipeptidyl Peptidase-4 (DPP-4) |
| PDB ID | 5Y7H |
| Organism | Homo sapiens |

---

# Input

- Compound library (.xlsx)
- DPP-4 receptor (PDB)
- Ligand structures

---

# Output

The workflow generates:

- SMILES dataset
- 3D ligand structures
- Docking results (GNINA)
- Docking results (PLANTS)
- Correlation plots
- Venn diagram
- Consensus scores
- Ranked hit compounds
- 2D structures of selected phytochemicals

---

# Citation

If you use this repository in your research, please cite:

Illahi AD, Candra TM, Hakim IL, Eliza D, Mustafidah M, Makambwa E.

**Discovery of Potential DPP-4 Inhibitors from *Cassia auriculata* Through Dual Molecular Docking with GNINA and PLANTS.**

(Manuscript under review)

---

# Authors

**Adha Dastu Illahi***¹

Tifany Maulida Candra²

Imam Lukmanul Hakim²

Delila Eliza¹

Mabrurotul Mustafidah¹

Ezekiel Makambwa³

¹ Department of Pharmacy, Faculty of Health Sciences, Universitas Islam Negeri Syarif Hidayatullah Jakarta, Indonesia

² Department of Pharmacy, Sekolah Tinggi Ilmu Kesehatan Salsabila, Indonesia

³ Department of Chemistry and Earth Sciences, University of Zimbabwe, Zimbabwe

*Corresponding author*

📧 adha.dastu@uinjkt.ac.id

---

# License

This repository is intended for academic and research purposes.
