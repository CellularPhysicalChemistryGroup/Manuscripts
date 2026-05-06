# Manuscripts
Code and datasets from published papers.
Link for paper: <<Put Bioxriv link>>

# All Analysis except EM

(Josh update)



# EM Analysis — Figure S5

Electron microscopy image analysis for Figure S5. Code is written in Mathematica 14.

## Files

- `EMCode.nb` — all analysis and figure generation
- `data_extraction.py` — Python script to download the raw data from OpenOrganelle and generate the CSV input files (run this first)

## Data

Five of the six input CSV files are small and included directly in this folder:

| File | Dataset |
|------|---------|
| `jrc_hela-3_x6290_6700_y250_500_z5740.csv` | HeLa v1 |
| `jrc_hela-3_x5301_5711_y233_483_z5730.csv` | HeLa v2 |
| `jrc_hela-3_x5297_5707_y440_690_z5584.csv` | HeLa v3 |
| `jrc_hela-3_x5938_6348_y336_586_z5660.csv` | HeLa v4 |
| `jrc_jurkat-1_x7763_8173_y926_1176_z3788.csv` | Jurkat |

The sixth file, `jrc_hela-3_z5740.csv`, is a full-width slice of the HeLa cell used for the whole-cell overview panel (Figure S5A). It is too large to host here and must be generated locally by running `data_extraction.py`. The script downloads the data anonymously from the public [OpenOrganelle](https://www.openorganelle.org/datasets/jrc_hela-3) S3 repository — no account is required.

## How to run

1. Install Python dependencies: `pip install fsspec zarr dask numpy`
2. Run `data_extraction.py` to generate `jrc_hela-3_z5740.csv` (the other CSVs are already present)
3. Place all CSV files in the same folder as `EMCode.nb`
4. Open `EMCode.nb` in Mathematica 14 and run top to bottom






Feel free to contact the Riback Lab with questions/concerns: www.RibackLab.com
