# 311 Service Requests: Differential Privacy Analysis

Applying differential privacy techniques to Chicago 311 service request data to extract aggregate insights without compromising individual privacy.

## Background

Public service request datasets (noise complaints, graffiti removal, sanitation requests) contain location coordinates and timestamps that can reveal personal information about the people who submitted them. This project demonstrates how epsilon-delta differential privacy mechanisms can add calibrated noise to sensitive fields while preserving the statistical patterns that city planners and resource allocators need.

Built as the final project for the Human-Centered Data course at UIUC.

## Dataset

Chicago 311 Service Requests, covering complaint types, geographic coordinates, ZIP codes, ward numbers, request status, and timestamps. The dataset is preprocessed to handle missing values, standardize coordinates, and parse timestamps.

## Methodology

1. Data preprocessing: cleaning missing values, normalizing coordinates, parsing timestamps
2. Exploratory analysis: complaint type distributions, geographic clustering by ZIP code and ward
3. Differential privacy implementation: adding Laplacian noise to coordinates and counts at varying epsilon values
4. Utility analysis: comparing noisy outputs against true aggregates to measure privacy-utility tradeoffs

## Key Findings

- The most common request types are Information Only Calls, Aircraft Noise Complaints, and Graffiti Removal
- Requests cluster in specific ZIP codes (60612, 60666), reflecting neighborhood-level patterns
- Differential privacy at epsilon=1.0 preserves spatial and categorical trends while obscuring exact locations
- Lower epsilon values provide stronger privacy but degrade fine-grained geographic analysis

## Repository Structure

```
311_DP_Analysis_English.ipynb   Primary notebook with EDA and privacy implementation
IS597.ipynb                     Supplementary analysis and data processing
final/
  311_DP_Analysis final.ipynb   Finalized analysis with all results
  311_DP_Analysis.ipynb         Clean working version
  311_dp_analysis.py            Standalone Python script version
output.png                      Sample visualization output
```

## Tech Stack

Python, pandas, NumPy, Plotly, Seaborn, Matplotlib

## License

MIT
