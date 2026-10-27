# Synthetic Hospital Occupancy Dataset

This repository contains simulated hospital occupancy and arrivals data, the code used to generate them, and forecasting notebooks for a dissertation revision. The patient records are synthetic; no real patient data are included.

## Contents

- `Dataset Generator/` — notebook that generates the synthetic data.
- `Dataset Specs/` — released occupancy and arrivals data, simulation settings, patient-level synthetic records, and validation summaries.
- `90 Days/`, `180 Days/`, `270 Days/` — forecasting notebooks for different horizons.
- `90_10 Split/`, `80_20 Split/`, `70_30 Split/` — forecasting notebooks for different chronological train/test splits.

## Getting started

Open this folder as the Jupyter working folder. Run `Dataset Generator/synthetic_hospital_occupancy_generator.ipynb` from top to bottom to create fresh files in `synthetic_hospital_outputs/`. The forecasting notebooks use the released daily series at `Dataset Specs/hospital_occupancy_daily.csv`. Run the individual model notebooks before the fusion notebooks, which use their saved predictions.

The notebooks use Python with NumPy, pandas, Matplotlib, scikit-learn, and statsmodels. The simulation settings and validation files document the assumptions and checks; they do not establish that the simulated data represent a real hospital.
