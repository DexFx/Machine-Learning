# ARTI308 - Machine Learning: Linear Regression Project

This project focuses on implementing a **Linear Regression** model to predict the `Yearly Amount Spent` by customers of an Ecommerce platform. It is part of the ARTI308 Machine Learning curriculum, transitioning from a guided real estate pricing exercise to an independent analysis of customer behavior.

## Project Overview
The objective is to help an Ecommerce company decide whether to focus their efforts on their mobile app experience or their website. By analyzing customer data, we build a model that predicts the total yearly spend based on several usage metrics.

## Dataset: Ecommerce Customers
The dataset contains customer information including:
- **Avg. Session Length**: Average session of in-store style advice sessions.
- **Time on App**: Average time spent on the mobile app in minutes.
- **Time on Website**: Average time spent on the website in minutes.
- **Length of Membership**: How many years the customer has been a member.
- **Yearly Amount Spent**: The target variable (Total annual spend).

### Data Preview
|    | Email                         | Address                        | Avatar           |   Avg. Session Length |   Time on App |   Time on Website |   Length of Membership |   Yearly Amount Spent |
|---:|:------------------------------|:-------------------------------|:-----------------|----------------------:|--------------:|------------------:|-----------------------:|----------------------:|
|  0 | mstephenson@fernandez.com     | 835 Frank Tunnel               | Violet           |               34.4973 |       12.6557 |           39.5777 |                4.08262 |               587.951 |
|    |                               | Wrightmouth, MI 82180-9605     |                  |                       |               |                   |                        |                       |
|  1 | hduke@hotmail.com             | 4547 Archer Common             | DarkGreen        |               31.9263 |       11.1095 |           37.269  |                2.66403 |               392.205 |
|    |                               | Diazchester, CA 06566-8576     |                  |                       |               |                   |                        |                       |
|  2 | pallen@yahoo.com              | 24645 Valerie Unions Suite 582 | Bisque           |               33.0009 |       11.3303 |           37.1106 |                4.10454 |               487.548 |
|    |                               | Cobbborough, DC 99414-7564     |                  |                       |               |                   |                        |                       |
|  3 | riverarebecca@gmail.com       | 1414 David Throughway          | SaddleBrown      |               34.3056 |       13.7175 |           36.7213 |                3.12018 |               581.852 |
|    |                               | Port Jason, OH 22070-1220      |                  |                       |               |                   |                        |                       |
|  4 | mstephens@davidson-herman.com | 14023 Rodriguez Passage        | MediumAquaMarine |               33.3307 |       12.7952 |           37.5367 |                4.44631 |               599.406 |
|    |                               | Port Jacobville, PR 37242-1057 |                  |                       |               |                   |                        |                       |

### Statistical Summary
|       |   Avg. Session Length |   Time on App |   Time on Website |   Length of Membership |   Yearly Amount Spent |
|:------|----------------------:|--------------:|------------------:|-----------------------:|----------------------:|
| count |            500        |    500        |         500       |             500        |              500      |
| mean  |             33.0532   |     12.0525   |          37.0604  |               3.53346  |              499.314  |
| std   |              0.992563 |      0.994216 |           1.01049 |               0.999278 |               79.3148 |
| min   |             29.5324   |      8.50815  |          33.9138  |               0.269901 |              256.671  |
| 25%   |             32.3418   |     11.3882   |          36.3493  |               2.93045  |              445.038  |
| 50%   |             33.082    |     11.9832   |          37.0694  |               3.53398  |              498.888  |
| 75%   |             33.712    |     12.7538   |          37.7164  |               4.1265   |              549.314  |
| max   |             36.1397   |     15.127    |          40.0052  |               6.92269  |              765.518  |

## Workflow
1. **Data Loading**: Importing the `Ecommerce Customers` dataset using Pandas.
2. **Exploratory Data Analysis (EDA)**: Understanding relationships between features (e.g., Correlation between Length of Membership and Yearly Amount Spent).
3. **Data Preprocessing**: Separating numerical features from categorical identifiers (Email, Address, Avatar).
4. **Model Training**: 
   - Splitting data into Training (70%) and Testing (30%) sets.
   - Training a `LinearRegression` model from `scikit-learn`.
5. **Model Evaluation**: Using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).

## Requirements
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## How to Run
1. Open the `ARTI308 Lab6.ipynb` notebook.
2. Ensure the `Ecommerce Customers` file is in the same directory.
3. Run the cells sequentially to perform the analysis and train the model.

---
*Developed as part of ARTI308 Machine Learning Lab.*
