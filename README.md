# 🏙️ UK Crime Analysis For Real Estate

> 🚧 **Work in Progress:** This repository is currently under active development. 
> * **Completed:** Phase 1 & 2 (Data Collection & Cleaning)
> * **Current Focus:** Phase 3 (Exploratory Data Analysis and Spatial Mapping).

### Project Aims
The primary objective of this project is to identify emerging, undervalued real estate markets across the UK. By analysing geospatial street crime data, this analysis seeks to pinpoint regions experiencing statistically significant drops in crime rates *before* the wider market catches on and house prices adjust.

### Key Business Questions
1. **The Safety Trajectory:** Which specific local authorities are demonstrating the sharpest decline in reported street crime over the last 24 months?
2. **The Urban vs. Rural Divide:** How do seasonal crime trends in dense metropolitan hubs compare to commuter belts and coastal regions?
3. **The Arbitrage Opportunity:** (Phase 4 integration) Which postcodes currently possess both low/falling crime rates and below-average property valuations?

---

## 📊 Methodology

Note: this analysis can be reproduced by following the steps below and the notebook links provided.

### Scope & Constraints
* **Geographic Focus:** 4 contrasting UK Police Constabularies (Metropolitan Police, Greater Manchester, Thames Valley, and Sussex).
* **Timeframe:** January 2022 to December 2023 (24 Months).
* **Exclusions:** 'Stop and Search' data has been deliberately excluded to maintain a strict analytical focus on metrics that directly impact residential desirability and property valuation.

### Phase 1: Data Acquisition
Raw data was sourced directly from the UK Government Police API ([data.police.uk](https://data.police.uk/data/)). 

To ensure a robust, cross-sectional analysis of the UK property market, forces were selected based on distinct demographic profiles:
* **Metropolitan Police:** High-density urban baseline.
* **Greater Manchester:** Secondary urban growth trends.
* **Thames Valley:** Affluent, high-value commuter belt.
* **Sussex:** Coastal dynamics and rural contrast.

*Result:* 96 individual CSV files were extracted for cleaning.

### Phase 2: Data Cleaning & Wrangling
The 96 fragmented datasets were ingested and standardised using Python (`pandas`). 
Key transformations included:
* Standardising column headers (snake_case).
* Dropping contextually blank columns to optimise memory.
* Parsing string-based 'Month' data into actionable `datetime` indices.
* Consolidating the files into a single, highly compressed `.parquet` master file.

> 🔗 **Technical Documentation:** For a detailed breakdown of the pandas vectorisation and missing-data imputation strategy, please refer to the cleaning script: [01_data_merging.ipynb](notebooks/01_data_merging.ipynb)

### Phase 3: Exploratory Data Analysis (EDA)
*(To be updated as the analysis progresses...)*