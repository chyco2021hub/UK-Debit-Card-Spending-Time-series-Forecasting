# UK-Debit-Card-Spending-Time-series-Forecasting
This project analyses and forecasts debit card sspending patterns using time series analysis and forecasting models. The study incorporated macroeconomic variables (interest rates, inflation rates and unemployment rates) and demographic factors (age groups) to build predicitive models for future spending trends).

## Business Objective
To develop accurate forecasting models that can help financial institutions, retailers, and policymakers understand and predict debit card spending behavior under various economic conditions.

## Repository Structure
text
DAT7304-Business-Analytics/
├── DAT7304_CODE_10TH_MAY_2025.R    # Main R script with complete analysis
├── data/                           # Dataset directory (not included in repo)
│   ├── debit cards spending.csv
│   ├── interest rate dataset.csv
│   ├── inflation dataset2.csv
│   └── unemployment dataset.csv
├── outputs/                        # Generated outputs
│   ├── spending_dataframe.csv
│   ├── interest_dataframe.csv
│   ├── inflation_dataframe.csv
│   ├── unemploy_dataframe.csv
│   └── combined_table.csv
├── README.md                       # This file
└── requirements.txt               # Package dependencies

## Key Features
### Data Sources
#### Debit Card Spending: Daily transaction data by age groups (18-34, 35-54, 54+)

### Macroeconomic Indicators:

Interest Rates

Inflation Rates

Unemployment Rates

Time Period: January 2020 - February 2025

## Analytical Techniques
### Data Preprocessing

Missing value imputation using MICE

Outlier detection and treatment

Data transformation (logarithmic)

Time series decomposition

Statistical Analysis

Correlation analysis

Stationarity testing (ADF, KPSS)

Autocorrelation analysis (ACF/PACF)

Residual diagnostics

Forecasting Models

#### Univariate: ARIMA, ETS, Holt's Linear, Theta

#### Exogenous Variable Models: ARIMAX, Dynamic Regression

#### Multivariate: VAR, VARX

#### Machine Learning: Neural Network (NNETAR), Prophet

## Technical Implementation
Required R Packages
r
#### Data Manipulation
library(tidyverse)
library(lubridate)
library(dplyr)
library(naniar)
library(mice)
library(zoo)

#### Time Series Analysis
library(forecast)
library(tseries)
library(imputeTS)
library(ggfortify)

#### Statistical Testing
library(lmtest)
library(urca)
library(Metrics)

#### Visualization
library(ggplot2)
library(corrplot)
library(ggcorrplot)

#### Advanced Modeling
library(vars)
library(prophet)
Key Code Sections

### Data Loading & Cleaning: 
Comprehensive preprocessing pipeline

### Exploratory Analysis: 
Visualizations and correlation studies

### Model Development: 
Multiple forecasting approaches

### Model Evaluation: 
RMSE, MAE, MAPE metrics

### Forecast Generation: 
12-month future predictions

## Key Findings
Correlation Insights
Strong positive correlation among age group spending patterns

Moderate relationships between spending and macroeconomic factors

Online spending shows distinct seasonal patterns

## Model Performance
Best Univariate Model: ARIMA (lowest RMSE/MAE)

Best Exogenous Model: VAR with macroeconomic variables

Most Flexible: Prophet with custom seasonality

Business Insights
Age group 35-54 shows highest spending levels

Interest rates have significant inverse relationship with spending

Online spending continues growth trajectory despite economic fluctuations

## How to Run
Prerequisites
R (version 4.0+)

RStudio (recommended)

Required R packages (see installation below)

Installation & Setup
r
# Install required packages
install.packages(c("tidyverse", "forecast", "tseries", "prophet", 
                   "vars", "ggplot2", "lmtest", "Metrics"))

# Run the analysis
source("DAT7304_CODE_10TH_MAY_2025.R")
Data Preparation
Place CSV files in the data/ directory

Update file paths in the script if necessary

The script automatically handles data cleaning and transformation

## Outputs Generated
Data Files
Cleaned and merged datasets

Monthly aggregated spending data

Combined table with all variables

## Visualizations
Time series decomposition plots

Correlation matrices

Forecast comparison charts

Residual diagnostic plots

Forecast Results
12-month spending predictions

Model accuracy metrics

Confidence intervals for forecasts

## Future Enhancements
Potential Improvements
Incorporate additional economic indicators

Implement deep learning models (LSTM)

Real-time forecasting capabilities

Interactive dashboard development

Extension Opportunities
Regional spending analysis

Merchant category forecasting

Customer segmentation models

Anomaly detection for fraud analysis

## Methodology Details
Time Series Characteristics
Frequency: Monthly data

Seasonality: 12-month cycles

Trend: Overall growth pattern with economic fluctuations

Stationarity: Achieved through differencing and transformations

Model Selection Criteria
Accuracy: RMSE, MAE, MAPE

Residual Properties: White noise testing

Practicality: Interpretability and business relevance

Computational Efficiency: Training and prediction time

## Contributing
This project is part of academic research. For contributions or extensions, please follow standard GitHub collaboration protocols.

📄 License
This project is intended for academic and research purposes. Please cite appropriately if used for research or commercial applications.
