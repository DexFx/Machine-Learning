# Talabat-style Order Status Prediction

## Project Overview
This project focuses on **Feature Engineering** for a classification task. Using a simulated dataset of food delivery orders (similar to Talabat), we aim to predict the `Order_Status` (Delivered, Cancelled, or In Transit). 

The dataset was intentionally provided in a clean state to allow for deep exploration of how transforming raw data into meaningful features impacts model performance.

## Dataset Summary
- **Total Records:** 100,000
- **Features:** 23 (including timestamps, coordinates, and pricing)
- **Target Variable:** `Order_Status`
- **Class Distribution:**
  - Delivered: 85.2%
  - Cancelled: 9.8%
  - In Transit: 5.0%

## Feature Engineering Implementation

### 1. Time-Based Features
- **Temporal Extraction:** Extracted `order_hour` and `order_dayofweek` from timestamps.
- **Is_Weekend:** Binary flag for Saturday/Sunday.
- **Peak Hour Logic:** Categorized orders during lunch (12-15) and dinner (19-23) as peak periods.
- **Breakfast Rush (Updated):** Added a specific rule for morning peaks (7-9 AM) to capture time-sensitive work-commute orders.

### 2. Spatial & Interaction Features
- **Haversine Distance:** Calculated the Great-Circle distance (km) between restaurant and customer coordinates.
- **Price per Item:** Normalizing the total price by quantity.
- **Quantity-Price Interaction:** Created an interaction term (`Quantity * Total_Price`) to identify high-complexity/bulk orders.

### 3. Categorical Handling
- **Cardinality Reduction:** Handled high-cardinality features like `Item_Name` by grouping all items outside the Top-K frequency into an "Other" category.
- **Price Binning:** Segmented orders into tiers (Low, Medium, High, Very High) to capture non-linear relationships with delivery success.

## Model & Evaluation
- **Algorithm:** Random Forest Classifier (300 estimators).
- **Handling Imbalance:** Utilized `class_weight="balanced_subsample"`.
- **Feature Selection:** Implemented `SelectFromModel` using median importance thresholds to streamline the model for production efficiency.

## Key Findings
- **Most Important Features:** Pricing metrics and delivery distance were the strongest predictors of order status.
- **Efficiency:** Feature selection allowed us to reduce the feature space by ~50% with negligible loss in accuracy, improving inference speed.

## How to Run
1. Ensure `talabat_enhanced_orders.csv` is in the root directory.
2. Run the Jupyter Notebook `ARTI308 Lab5.ipynb`.
3. The pipeline includes preprocessing, feature engineering, and model evaluation steps.
