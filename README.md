# Toronto Public Access AED Data Analysis (2025)

**Python | Pandas | Data Cleaning | Exploratory Data Analysis**

## Project Overview

This project analyzes the City of Toronto's 2025 Automated External Defibrillator (AED) Locations dataset using Python and Pandas. The objective is to identify data quality issues, examine the distribution of AED records across organizations and locations, and explore patterns that may support improved equipment tracking and record management.

Completed as part of INF1340H – Programming for Data Science in the University of Toronto's Master of Information program.

## Dataset

**Source:** [City of Toronto Open Data – Automatic External Defibrillators (AED) Locations](https://open.toronto.ca/dataset/automatic-external-defibrillators-aed-locations/)

The dataset contains information about publicly accessible AEDs, including:

- Organization and division
- Site name and location
- City and postal code
- AED placement information
- AED manufacturer and model

## Tools & Skills

- **Python:** Data processing and analysis
- **Pandas:** Data cleaning, filtering, grouping, aggregation, and descriptive statistics
- **Google Colab:** Development and execution
- **Data Quality Assessment:** Handling missing values, inconsistent formatting, and duplicate-looking records

## Methodology

### 1. Data Inspection & Cleaning

The dataset was inspected for missing values, placeholder entries, inconsistent formatting, spelling errors, and duplicate-looking records.

Cleaning operations included:

- Standardizing missing and `TBD` values as `Not Provided`
- Removing extra spaces and standardizing city capitalization
- Correcting misspelled city names
- Adding sequential record identifiers while retaining potentially valid duplicate-looking records

### 2. Exploratory Data Analysis

Six analyses examined:

1. AED record counts by division
2. Cities with the fewest AED records
3. Most frequently recorded AED manufacturer
4. Unique AED manufacturers
5. Record counts by organization
6. Records with missing placement information

### 3. Higher-Level Analysis

Two additional analyses combined multiple Pandas operations:

- **Placement Data Completeness:** Calculated and compared the percentage of missing placement records across organizations.
- **Site-Level Distribution:** Calculated average AED records per site and identified locations with above-average counts.

## Key Findings

- **Equipment Distribution:** Zoll was the most frequently recorded AED manufacturer.
- **Data Completeness:** The Safe City Program had a higher proportion of records with missing placement information than the City of Toronto.
- **Site Concentration:** Certain locations, including TTC stations, had above-average AED record counts.
- **Data Integrity:** Identical records could not automatically be classified as duplicates because the dataset lacked official device identifiers.

## Limitations

The dataset contains incomplete placement and location information, and it does not provide unique identifiers for individual AED devices. As a result, AED record counts cannot always be interpreted as verified counts of unique devices.

Additionally, the dataset does not include maintenance history, inspection status, device condition, or usage frequency, limiting conclusions about operational needs or accessibility.

## Repository Contents

- `AED.csv` – Original dataset
- `AED_Cleaned.csv` – Cleaned dataset
- Jupyter Notebook (`.ipynb`) – Python code, analysis, and findings

## Data Source & Attribution

Data provided by the City of Toronto through its Open Data portal.

[View Original Dataset](https://open.toronto.ca/dataset/automatic-external-defibrillators-aed-locations/)
