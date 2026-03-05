# KFC Sales Data Preprocessing & Analysis

## Project Overview

This project adapts a machine learning preprocessing pipeline to a specific retail dataset (KFC Past Sales). The goal is to transform raw sales data into a clean, normalized format suitable for machine learning models by addressing data quality issues, handling outliers, and reducing dimensionality.

## Dataset Description

The dataset used is `KFC_Past_Sales_Dataset.csv`, which contains the following features:

* **Year/Month**: Temporal data for sales tracking.
* **Country/Branch_ID**: Categorical location data.
* **Sales**: The target numerical value representing total revenue.
* **Customers**: Numerical count of store visitors.
* **Marketing_Spend**: Numerical value of advertising investment.

## Preprocessing Pipeline

The project is structured into five core sections based on standard data science practices:

### 1. Data Quality Assessment

* **Type Checking**: Verifying that numerical and categorical data are correctly identified by the environment.
* **Conversion**: Transforming string-based date components into `datetime` objects to enable time-series analysis.

### 2. Handling Missing Values

* **Detection**: Identifying null or "Not a Number" (NaN) values within the dataset.
* **Imputation Strategies**: Implementation of Mean and Median imputation to fill gaps in data without significantly biasing the distribution.

### 3. Outlier Management

* **IQR Method**: Utilizing the Interquartile Range (Q3 - Q1) to define statistical boundaries for "normal" data.
* **Capping & Removal**: Demonstrating how to either remove extreme values or "cap" them at specific percentiles to reduce model distortion.

### 4. Data Transformation (Normalization)

To ensure features with larger scales (like Sales) do not dominate the model, two scaling techniques are applied:

* **Min-Max Scaling**: Rescaling data to a fixed range between 0 and 1.
* **Z-Score Normalization (Standardization)**: Rescaling data to have a mean of 0 and a standard deviation of 1.

### 5. Dimensionality Reduction (PCA)

* **Correlation Analysis**: Checking for linear relationships between features using heatmaps.
* **Principal Component Analysis**: Reducing the feature set into Principal Components (PC1, PC2) that capture the maximum variance of the data, visualized via scatter plots.

## Requirements

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Usage

1. Ensure `KFC_Past_Sales_Dataset.csv` is in the working directory.
2. Run the provided `.ipynb` notebook cells sequentially.
3. Observe the visualizations (boxplots, heatmaps, and PCA projections) to verify the impact of each preprocessing step.
