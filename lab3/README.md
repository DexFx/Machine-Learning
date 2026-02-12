lab3

KFC Past Sales - Exploratory Data Analysis (EDA)

## Project Overview

This project performs a comprehensive Exploratory Data Analysis on a historical sales dataset for KFC. The goal is to identify sales trends, customer behavior, and the impact of marketing spend across various international branches (India, UK, USA, Canada, and Australia).

This analysis follows the framework provided in the ARTI308 Machine Learning Lab 3.

## Dataset Description

The dataset (KFC_Past_Sales_Dataset.csv) contains 8,000 records with the following features:

Year/Month: Timeframe of the recorded sales.

Country: The country where the branch is located.

Branch_ID: Unique identifier for specific KFC locations.

Sales: Total revenue generated (Target Variable).

Customers: Total footfall/number of customers.

Marketing_Spend: Amount spent on promotions and advertisements.

## Key Analysis Steps

Data Cleaning: Handled date formatting by merging Year and Month into a single datetime object. Verified that there are no missing values or duplicate entries.

Statistical Profiling: Generated descriptive statistics to understand the mean, standard deviation, and range of sales and customer counts.

Data Visualization:

Distributions: Analyzed the spread of Sales and Customers using Histograms.

Categorical Analysis: Compared total sales performance across different countries.

Correlation Analysis: Used a Heatmap to determine the relationship between Marketing Spend, Customers, and Sales.

Time Series: Plotted a Monthly Sales Trend to identify growth or seasonality.

## Requirements

To run the notebook, you will need the following Python libraries:

pandas

numpy

matplotlib

seaborn

How to Run
Ensure KFC_Past_Sales_Dataset.csv and KFC_Sales_Analysis.ipynb are in the same directory.

Open the notebook using Jupyter Notebook or Google Colab.

Run all cells to generate the analysis and visualizations.
