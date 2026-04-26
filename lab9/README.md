# Loan Data Analysis: EDA, Decision Tree, and Random Forest

This project explores a public lending dataset to predict whether a borrower will pay back their loan in full. It involves comprehensive Exploratory Data Analysis (EDA) and the implementation of machine learning models to classify loan repayment status.

## Project Overview

The analysis follows a standard data science workflow:
1.  **Data Loading**: Importing the loan dataset and inspecting its structure.
2.  **Exploratory Data Analysis (EDA)**: Visualizing distributions and relationships between variables like FICO scores, interest rates, and loan purposes.
3.  **Data Preparation**: Handling categorical variables using dummy encoding and splitting the data into training and testing sets.
4.  **Modeling**:
    * **Decision Tree Classifier**: A baseline model for classification.
    * **Random Forest Classifier**: An ensemble method to improve predictive performance.
5.  **Evaluation**: Comparing models using Confusion Matrices and Classification Reports.

## Dataset Features

The dataset (`loan_data.csv`) contains the following key attributes:
* **credit.policy**: 1 if the customer meets the credit underwriting criteria, 0 otherwise.
* **purpose**: The purpose of the loan (e.g., debt_consolidation, credit_card, etc.).
* **int.rate**: The interest rate of the loan.
* **fico**: The FICO credit score of the borrower.
* **not.fully.paid**: The target variable (1 if not fully paid, 0 if paid in full).

## Key Visualizations

The script generates several plots to understand the data:
* **FICO Distributions**: Compared across credit policy and repayment status.
* **Purpose vs. Payment Status**: A count plot showing loan counts by category.
* **FICO vs. Interest Rate**: Analyzed via jointplots and linear models.

## Results Summary

Based on the latest execution:
* **Decision Tree**: Achieved an accuracy of approximately 73%.
* **Random Forest**: Achieved a higher overall accuracy of 85%, though it showed a lower recall for the minority class (not fully paid).

## Dependencies

To run the notebook, you need the following Python libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

## Usage

1.  Ensure `loan_data.csv` is in the same directory as the notebook.
2.  Run all cells in `lab9.ipynb` to generate the EDA figures and train the models.
3.  The results and figures (e.g., `fico_credit_policy.png`) will be saved to your local directory.
