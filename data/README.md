## Download Instructions

### Step 1 — Go to the IBDMDB data portal

https://ibdmdb.org

### Step 2 — Download these two files

| File | Direct Link | Description |
|---|---|---|
| `hmp2_metadata.tsv` | [Download](https://ibdmdb.org/tunnel/products/HMP2/Metadata/hmp2_metadata.tsv) | Participant metadata including diagnosis, fecal calprotectin, visit week, and clinical scores |
| `taxonomic_profiles.tsv` | [Download](https://ibdmdb.org/tunnel/products/HMP2/WGS/metaphlan2_taxonomic_profiles.tsv) | MetaPhlAn3 species-level relative abundance profiles |

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
