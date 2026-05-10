# NOAA OISST Environmental Stress Analysis

## Author

Beija Richardson

## Authorship

This project was completed independently by Beija Richardson.

All data preprocessing, feature engineering, visualization development, and modeling preparation were completed by the author.

## Repository Structure

- NOAA_OISST_Report.ipynb → primary notebook
- README.md → project documentation
- LICENSE → MIT license

## Testing & Validation

The notebook was tested in Google Colab using the NOAA OISST NetCDF files listed in this repository documentation.

All notebook cells were executed sequentially to confirm:
- successful package installation
- dataset loading
- feature engineering
- ESMS generation
- visualization creation
- model evaluation outputs

The notebook completed without runtime errors after dependency installation.

## Project Overview

This project investigates how sea surface temperature anomalies relate to environmental variability patterns that may reflect behavioral irregularity in marine systems.

## Research Question

How do sea surface temperature anomalies in the North Atlantic relate to environmental variability patterns that may reflect behavioral irregularity in Atlantic Bluefin Tuna migration systems?

## Required Packages

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xarray
- netCDF4

## Dataset

### NOAA OISST V2.1 High Resolution Dataset

Files Used:

* oisst-avhrr-v02r01.20200101.nc
* oisst-avhrr-v02r01.20210101.nc
* oisst-avhrr-v02r01.20220101.nc
* oisst-avhrr-v02r01.20230101.nc
* oisst-avhrr-v02r01.20240101.nc
* oisst-avhrr-v02r01.20250101.nc

Primary Variable:

* `anom` = Sea Surface Temperature Anomaly

Supporting Variables:

* `sst`
* `lat`
* `lon`
* `time`

Region:

* North Atlantic Ocean

Species Focus:

* Atlantic Bluefin Tuna (proxy-based biological relevance)

## Custom Functions

This project includes custom functions for:

* North Atlantic regional extraction
* ESMS calculation
* Rolling volatility calculation
* Environmental regime classification

## How to Run

1. Open `NOAA_OISST_Report.ipynb` in Google Colab
2. Upload NOAA `.nc` files
3. Run all notebook cells
4. Export figures and CSV outputs

## Output Files

* processed CSV
* summary statistics
* correlation matrix
* visualization figures
* final report PDF

## Key Features Engineered

* Rolling Temperature (7-day average)
* Temperature Change
* Volatility (rolling standard deviation)
* Environmental Stress Movement Score (ESMS)

## Validation Limitations

Because this project uses time-dependent environmental observations and lagged features, temporal leakage was considered during evaluation.

Initial model testing used Leave-One-Out Cross-Validation (LOOCV) due to the extremely small dataset size (n = 6 yearly observations). However, LOOCV does not fully preserve chronological ordering and may allow future observations to influence training data indirectly.

This limitation means model performance metrics may be optimistic and should be interpreted cautiously.

Future iterations of this project will prioritize forward-chaining or rolling-window validation strategies that better preserve temporal structure for time-series modeling.

## Future Modeling Plan

Planned next steps include:

* Linear regression baseline model
* Non-linear modeling approaches
* Tree-based models for feature importance
* Clustering methods for environmental regime segmentation

This project combines marine biology concepts with data science and machine learning techniques to explore environmental instability patterns in ocean systems.
