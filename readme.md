# CASA0006 Assessment – Burglary Risk Modelling in London

This repository contains coursework materials and analysis for the CASA0006 module at UCL. The project investigates spatial burglary risk across Greater London using point-of-interest (POI) data and interpretable machine learning techniques.

## Repository Structure

```
.
├── data/                     # Raw and processed spatial data (e.g. POIs, grids, burglary rates)
├── cache/                   # Temporary or intermediate outputs (e.g. model artefacts)
├── flowchart/               # Visual workflows and diagrams
├── guide/                   # Supporting guides and reproducibility notes
├── proposal/                # Research proposal and project outline
├── references/              # Academic sources and citation files
├── Template_submission_CASA0006.ipynb  # Final submission notebook (analysis + visualisation)
├── readme.md                # This file
```

## Project Overview

- **Objective**: To explore spatial correlates of burglary hotspots in London and identify key urban features contributing to elevated risk.
- **Key Questions**:
  - Which types of POIs are most associated with burglary risk?
  - How can interpretable machine learning reveal spatial drivers of crime?

## Methodology Summary

- POI collection via [OSMnx](https://github.com/gboeing/osmnx) from OpenStreetMap
- Feature engineering on selected POIs (shops, pubs, restaurants, etc.)
- Grid-based spatial aggregation (200 m × 200 m cells)
- Burglary rate interpolation using Inverse Distance Weighting (IDW)
- Modelling using XGBoost regression
- Model interpretation via SHAP values
- Spatial analysis using Kernel Density Estimation and residual mapping

## Requirements

Install required libraries via pip or conda:

```bash
geopandas
osmnx
scikit-learn
shap
xgboost
matplotlib
```

## How to Reproduce

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/CASA0006_assessment.git
   ```
2. Ensure all data files are placed in the `data/` directory.
3. Open and run `Template_submission_CASA0006.ipynb` in Jupyter Lab or VSCode with Python kernel.
4. Use “Restart & Run All” to reproduce all results and figures.

## Notes

- All spatial layers are projected to EPSG:27700 (British National Grid).
- POIs were selected based on theories of crime attractors and generators (e.g. Brantingham & Brantingham, 1995).
- SHAP results highlighted commercial POIs and proximity to existing hotspots as strong predictors.
- Final runtime: 0.04 hours depending on system performance.

## References

Relevant academic literature and theory references are included in the `references/` folder and cited within the notebook.