# CASA0006 Assessment – Burglary Risk Modelling in London

This repository contains the coursework materials and analysis for the CASA0006 module at UCL. The project investigates the spatial patterns of burglary risk in Greater London using point-of-interest (POI) data and machine learning techniques.

## Repository Structure

```
.
├── data/                     # Processed and raw spatial data (e.g., grid, POIs)
├── cache/                   # Intermediate or temporary outputs
├── guide/                   # Guidance documents for analysis or replication
├── proposal/                # Project proposal and outline
├── references/              # Key academic sources or citation files
├── Template_submission_CASA0006.ipynb  # Main Jupyter Notebook (analysis & results)
├── assessment.ipynb         # Supplementary notebook (if applicable)
```

## Project Overview

- **Objective**: To explore spatial correlates of burglary risk across London and evaluate the predictive power of different urban POIs using geospatial machine learning.
- **Methods**:
  - Data collection from OpenStreetMap (via OSMnx)
  - Grid-based spatial aggregation
  - Feature engineering from POIs
  - Burglary density normalisation
  - Model training using XGBoost and interpretation using SHAP

## Requirements

The following Python libraries are required (install via pip or conda):

```bash
geopandas
osmnx
scikit-learn
shap
xgboost
matplotlib
```

## How to Reproduce

1. Clone this repository.
2. Run the Jupyter Notebook `Template_submission_CASA0006.ipynb` step by step.
3. Ensure the correct data files are available in the `data/` directory.

## Notes

- All spatial layers use the British National Grid (EPSG:27700).
- POIs were selected based on criminological theories (e.g., routine activity theory).
- Feature standardisation was applied using Z-score normalisation.
- Burglary data are based on interpolated values (IDW) at 200 m resolution.

## References

Relevant academic sources and theoretical frameworks can be found in the `references/` folder.