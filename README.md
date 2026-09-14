# Uzbekistan SPI v4.0 — Reproducible Verification Package

This repository contains a fully reproducible verification package for the World Bank
Statistical Performance Indicators (SPI) figures for Uzbekistan (2016–2024), prepared
in support of a scientific-practical report and an accompanying data descriptor
manuscript.

## Contents

| File | Description |
|---|---|
| `UZBEKISTAN_SPI_v4_0_VERIFICATION_EN.ipynb` | Executable Python (Jupyter/Colab) notebook. Retrieves the pinned World Bank SPI v4.0 source files, independently reconstructs the aggregation formulas, checks every numerical claim in the report, and reports PASS/WARN/FAIL. |
| `UZBEKISTAN_SPI_CLAIMS_REGISTER_EN.xlsx` | Structured register of all numerical claims in the report, cross-referenced to the pinned source field, with rounding rules and PASS/CHECK status. |
| `UZBEKISTAN_SPI_v4_0_INTERACTIVE_PANEL_EN.html` | Self-contained, static interactive dashboard (open directly in any browser, no server required) summarising the trend, pillar decomposition, SDG-level detail, international comparison, and conditional scenarios. |

## Data source

All figures derive from the World Bank's public SPI GitHub repository, release **v4.0**,
pinned at commit
[`2dd02f746cb4e2159281adc74d6865f948e90ce1`](https://github.com/worldbank/SPI/tree/2dd02f746cb4e2159281adc74d6865f948e90ce1).
Pinning to this exact commit (rather than the mutable `master` branch) ensures that the
figures in this package remain reproducible even if the World Bank later revises
historical rows in a subsequent release.

- Source repository: https://github.com/worldbank/SPI
- Pinned data file: `03_output_data/SPI_index.csv`
- Pinned aggregation code: `02_programs/02-SPI_index.Rmd`

## How to reproduce

1. Open `UZBEKISTAN_SPI_v4_0_VERIFICATION_EN.ipynb` in Google Colab or a local Jupyter
   environment (Python ≥3.10; requires `pandas`, `numpy`, `requests`).
2. Run all cells. The notebook downloads the pinned source files directly from GitHub
   at runtime — no manual data entry is required.
3. The final sections generate a PASS/FAIL summary and an electronic evidence package
   (CSV/JSON/HTML) with SHA-256 checksums of the source files.

## Citation

If you use this package, please cite the accompanying data descriptor:

> [Author names]. A Reproducible Verification Framework for Country-Level World Bank
> Statistical Performance Indicators (SPI): The Case of Uzbekistan, 2016–2024.
> [Journal, year, DOI — to be completed upon publication].

and the underlying World Bank data:

> World Bank. Statistical Performance Indicators (SPI), release v4.0.
> https://github.com/worldbank/SPI (commit `2dd02f746cb4e2159281adc74d6865f948e90ce1`).

## License

Code and analysis in this repository: MIT License (see `LICENSE`).
Underlying World Bank SPI data is licensed under CC BY 4.0 by the World Bank.

## Contact

[Name, affiliation, email to be completed by the author.]
