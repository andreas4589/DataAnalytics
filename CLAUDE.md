# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a data analytics project focused on mammographic masses data analysis. The main work is done in Jupyter notebooks with Python using pandas for data manipulation and plotly for visualization.

## Key Files
- `PA1.ipynb` - Main analysis notebook containing data exploration, preprocessing, and visualization tasks
- `mammographic_masses_data.csv` - Dataset with attributes: BA, Age, Shape, Margin, Density, Severity (target variable)
- `PA1_DataUnderstandingPreprocessing.pdf` - Assignment documentation

## Development Environment
- Python 3.8.10 strictly
- Jupyter Lab 4.4.7
- Key libraries: pandas, plotly.express

## Common Commands
```bash
# Start Jupyter Lab
jupyter lab

# Run notebook from command line
jupyter nbconvert --execute PA1.ipynb

# Convert notebook to other formats
jupyter nbconvert --to html PA1.ipynb
jupyter nbconvert --to pdf PA1.ipynb
```

## Data Structure
The mammographic masses dataset contains 961 records with missing values:
- BA: BI-RADS assessment (959 non-null)
- Age: Patient age (956 non-null) 
- Shape: Mass shape (930 non-null)
- Margin: Mass margin (913 non-null)
- Density: Breast density (885 non-null)
- Severity: Binary target variable (0/1, 961 non-null)

## Analysis Patterns
- Uses `df.copy()` for preprocessing to preserve original data
- Implements data binning with `pd.cut()` for age analysis
- Creates interactive visualizations with plotly.express
- Handles missing values represented as NULL in CSV and NaN in pandas
- Uses `df.loc[]` for conditional data selection