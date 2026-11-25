# Data Explorer

Exploratory data analysis of CO2 emissions with Python, pandas and matplotlib.

> **Status:** work in progress. Data loading and first exploration are done; cleaning, analysis and visualizations are next.

## Goals

This project explores the [Our World in Data CO2 dataset](https://github.com/owid/co2-data) to answer four questions (countries only, 1950–2024):

1. How have global CO2 emissions changed since 1950?
2. Are the 10 largest emitters in total also the largest per capita?
3. How has the share of coal, oil and gas in emissions changed?
4. Is CO2 per capita related to GDP per capita (2022)?

## Tech stack

Python 3.15 · pandas · matplotlib · Jupyter (VS Code) · Git

## Setup

```bash
git clone https://github.com/nassima44/data-explorer.git
cd data-explorer
python -m venv .venv
.venv\Scripts\Activate.ps1      # Windows (PowerShell)
# source .venv/bin/activate     # macOS / Linux
pip install -r requirements.txt
```

## Data

The raw data is not stored in this repository. Download it into `data/raw/`:

```powershell
mkdir data\raw
Invoke-WebRequest -Uri "https://owid-public.owid.io/data/co2/owid-co2-data.csv" -OutFile "data\raw\owid-co2-data.csv"
```

The analysis uses the version downloaded on 25 November 2026 (56,269 rows × 79 columns). OWID updates this file regularly, so newer versions may differ slightly.

**Source:** Our World in Data, *CO2 and Greenhouse Gas Emissions*, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Project structure

```
data-explorer/
├── data/raw/          # raw CSV (not tracked by Git)
├── notebooks/         # Jupyter notebooks
├── requirements.txt   # Python dependencies
└── README.md
```