# K-Nearest Neighbors (KNN) Classification Project

## Project Overview
This project implements a **K-Nearest Neighbors (KNN)** classifier to predict a binary `TARGET CLASS` based on a set of anonymized numerical features. The workflow includes data preprocessing (scaling), exploratory data analysis, model training, and hyperparameter tuning using the "Elbow Method" to find the optimal number of neighbors ($k$).

## Dataset Description
The dataset used is `KNN_Project_Data`. It contains 1000 observations with 10 hidden features.

- **Features:** XVPM, GWYH, TRAT, TLLZ, IGGA, HYKR, EDFS, GUUB, MGJM, JHZC
- **Target:** `TARGET CLASS` (Binary: 0 or 1)

Since the features are anonymized and on different scales, **Standardization** is a critical step in this pipeline to ensure the distance-based KNN algorithm performs correctly.

## Project Structure
1.  **Exploratory Data Analysis (EDA):** Visualizing feature distributions and class separations using Seaborn pairplots.
2.  **Data Preprocessing:** Standardizing features using `StandardScaler` from Scikit-Learn.
3.  **Train-Test Split:** Dividing the data into training (70%) and testing (30%) sets.
4.  **Baseline Model:** Training an initial KNN model with $k=1$.
5.  **Hyperparameter Tuning:** Iterating through $k$ values (1–40) to minimize the error rate.
6.  **Final Evaluation:** Retraining the model with the optimal $k$ and generating a Confusion Matrix and Classification Report.

## Requirements
To run the notebook, you need the following Python libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Key Findings
- **Feature Scaling:** Essential for this dataset as unit differences in features would otherwise bias the distance calculation.
- **Optimal K:** The elbow plot suggests that as $k$ increases, the error rate drops significantly before stabilizing, typically providing an accuracy boost compared to $k=1$.

## Usage
1. Ensure `KNN_Project_Data` is in the same directory as the notebook.
2. Run the cells in `02-K Nearest Neighbors Assignment.ipynb`.
3. Follow the "Elbow Method" visualization to verify the choice of $k$.

---
*This project is part of a machine learning assignment focused on distance-based classification.*
