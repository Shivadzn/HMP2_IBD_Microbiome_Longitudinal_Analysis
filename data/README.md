# Data

Raw data for this analysis is not included in this repository
due to file size and HMP2 data access terms.

---

## Download Instructions

### Step 1 — Download the two required files

| File | Direct Link | Description |
|---|---|---|
| `hmp2_metadata.tsv` | [Download](https://g-227ca.190ebd.75bc.data.globus.org/ibdmdb/metadata/hmp2_metadata_2018-08-20.csv) | Participant metadata — diagnosis, fecal calprotectin, visit week, clinical scores |
| `taxonomic_profiles.tsv` | [Browse metagenomics products](https://ibdmdb.org/downloads/html/products_MGX_2017-08-12.html) | MetaPhlAn3 species-level relative abundance profiles |

> **Note on taxonomic profiles:** The metagenomics products page
> contains per-sample files. For the merged taxonomic profiles
> table used in this analysis, navigate to:
> https://ibdmdb.org/results → Metagenomics (MGX) → products
> and download the merged taxonomic profiles TSV
> (bioBakery Version 3.0 recommended).

### Step 2 — Rename files if necessary

The metadata file downloads as `hmp2_metadata_2018-08-20.csv`.
Rename it to `hmp2_metadata.tsv` before placing in this directory.

### Step 3 — Place files in this directory

After downloading, place both files here:

```
HMP2_IBD_Microbiome_Longitudinal_Analysis/
└── data/
├── hmp2_metadata.tsv          ← place here
├── taxonomic_profiles.tsv     ← place here
└── README.md                  ← this file
```

### Step 4 — Run the notebook

The notebook expects both files in this directory. Once placed,
open `HMP2_IBD_Research_v3.ipynb` and run from Part 1.

---

## File Details

### hmp2_metadata.tsv

Contains per-sample clinical and demographic metadata:

| Column | Description |
|---|---|
| `External ID` | Unique sample identifier |
| `Participant ID` | Participant-level identifier for grouping |
| `diagnosis` | Healthy · Crohn's Disease · Ulcerative Colitis |
| `week_num` | Visit week number (0–57) |
| `fecal_calprotectin` | Mucosal inflammation marker (µg/g) |

### taxonomic_profiles.tsv

Contains MetaPhlAn3 species-level relative abundance estimates:

- Rows = samples (matched to `External ID` in metadata)
- Columns = 566 microbial taxa at species level
- Values = relative abundances summing to 100 per sample
- Sparsity = ~91% zeros (expected for metagenomics)

---

## Data Citation

If you use this data please cite the primary cohort paper:

Lloyd-Price J, Arze C, Ananthakrishnan AN, et al.
Multi-omics of the gut microbial ecosystem in inflammatory
bowel diseases. Nature. 2019;569(7758):655-662.
https://doi.org/10.1038/s41586-019-1237-9

---

## Access Terms

Data is provided by the NIH Human Microbiome Project under
the HMP Data Analysis and Coordination Center (DACC) data
access policy. Please review terms at https://ibdmdb.org
before downloading.
