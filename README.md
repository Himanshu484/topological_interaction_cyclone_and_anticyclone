# Topological Structure of the Cyclonic-Anticyclonic Interactions

This repository contains the code and analysis pipeline for the research paper "Topological Structure of the Cyclonic-Anticyclonic Interactions" by Himanshu Yadav, Gisela D. Charó, and Davide Faranda.

## Abstract

We apply persistent homology to analyze cyclonic-anticyclonic interactions in North Atlantic sea-level pressure anomalies from 1950-2022. Our topological data analysis approach provides an objective, filtering-free method to quantify the size, duration, and persistence of atmospheric pressure structures, offering novel insights into North Atlantic climate variability.

## Key Features

- **Persistent Homology Analysis**: Apply topological data analysis to sea-level pressure anomalies
- **Feature Tracking**: Track topological features across time using optimal matching algorithms
- **Climate Index Correlation**: Correlate topological metrics with major climate indices (NAO, AMO, ENSO, etc.)
- **Seasonal Analysis**: Examine seasonal patterns in cyclonic and anticyclonic structures
- **Trajectory Analysis**: Track long-lived atmospheric features over multiple days/weeks


## Repository Structure

```
topological_interaction_cyclone_and_anticyclone/
├── Code/
│   ├── Data/                           # Data files and datasets
│   ├── figures/                        # Generated figures and plots
│   ├── correlation_analysis.pynb.ipynb # Climate index correlation analysis
│   ├── exploratory_data_analysis.ipynb # Initial data exploration and preprocessing
│   └── feature_tracking_analysis.ipynb # Topological feature tracking analysis
└── README.md                          # This file
```

## Installation

### Prerequisites

- Python 3.8+
- Conda (recommended) or pip

### Key Dependencies

- `numpy >= 1.21.0`
- `scipy >= 1.8.0`
- `matplotlib >= 3.5.0`
- `pandas >= 1.4.0`
- `xarray >= 0.20.0`
- `gudhi >= 3.5.0` (for persistent homology)
- `netCDF4 >= 1.5.8` (for ERA5 data)
- `cartopy >= 0.20.0` (for geographic projections)
- `scikit-learn >= 1.0.0`
- `seaborn >= 0.11.0`

## Data Sources

### ERA5 Reanalysis Data
- **Source**: Copernicus Climate Change Service (C3S)
- **Variable**: Sea-level pressure
- **Temporal Coverage**: 1950-2022
- **Spatial Coverage**: North Atlantic (22.5°N-70°N, 80°W-50°E)
- **Resolution**: Daily, 0.25° × 0.25°

### Climate Indices
- **NAO**: North Atlantic Oscillation Index
- **AMO**: Atlantic Multidecadal Oscillation
- **ENSO**: El Niño-Southern Oscillation Index
- **EA**: East Atlantic Pattern
- **PDO**: Pacific Decadal Oscillation
- **SCAND**: Scandinavian Pattern

## Key Results

- **Seasonal Patterns**: Winter cyclonic features persist 35-38% longer than summer features
- **NAO Correlation**: Strong negative correlation (-0.573) between superlevel persistence and NAO index
- **Feature Lifetimes**: Longest tracked cyclonic feature: 59 days (Jan-Mar 1966)
- **Topological Metrics**: Novel quantitative measures for atmospheric circulation regimes

## Methodology

### Persistent Homology
- **Sublevel Filtration**: Captures anticyclonic regions surrounded by cyclonic regions
- **Superlevel Filtration**: Captures cyclonic regions surrounded by anticyclonic regions
- **1-Total Persistence (1-TP)**: Quantifies the total topological "significance" of pressure structures

### Feature Tracking
- Uses Wasserstein distance and optimal matching to track features across time
- Minimum persistence threshold of 1000 Pa for significant features
- Trajectory analysis for features lasting ≥2 days

## Citation

If you use this code in your research, please cite our paper submission to *Physica D: Nonlinear Phenomena*.

## Contact

- **Himanshu Yadav** - yadav.himanshu@ufl.edu
- **Gisela D. Charó** - gisela.charo@cima.fcen.uba.ar
- **Davide Faranda** - [institutional email]

## Acknowledgments

- University of Florida, Department of Mathematics
- CONICET – Universidad de Buenos Aires, CIMA
- Laboratoire des Sciences du Climat et de l'Environnement
- ERA5 data provided by the Copernicus Climate Change Service
- Climate indices data from NOAA and other meteorological services

## Related Publications
---

For detailed methodology and results, please refer to the full paper submission to *Physica D: Nonlinear Phenomena*.
