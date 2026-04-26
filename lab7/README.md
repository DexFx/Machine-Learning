# Internet Advertisement Click Prediction

## Project Overview
This project focuses on building a **Logistic Regression** model to predict whether or not a particular internet user will click on an advertisement based on their demographics and browsing behavior. 

The project uses a synthetic advertising dataset provided for the ARTI308 - Machine Learning course.

## Dataset Description
The dataset `advertising.csv` contains the following features:
* **Daily Time Spent on Site**: Consumer time on site in minutes.
* **Age**: Customer age in years.
* **Area Income**: Average income of the geographical area of the consumer.
* **Daily Internet Usage**: Average minutes a day the consumer is on the internet.
* **Ad Topic Line**: Headline of the advertisement.
* **City**: City of the consumer.
* **Male**: Whether or not the consumer was male (binary).
* **Country**: Country of the consumer.
* **Timestamp**: Time at which the consumer clicked on the Ad or closed the window.
* **Clicked on Ad**: Target variable (0: No, 1: Yes).

## Project Structure
* `02-Logistic Regression Assignment.ipynb`: The primary Jupyter Notebook containing the data analysis, visualizations, and model implementation.
* `advertising.csv`: The dataset used for training and testing.
* `titanic_train.csv` / `titanic_test.csv`: Included datasets for additional practice (not used in the primary assignment).

## Key Steps
1. **Data Exploration (EDA)**: Utilizing `Seaborn` and `Matplotlib` to understand feature distributions and correlations.
    * Analyzed Age distribution.
    * Explored relationships between Income and Age.
    * Investigated Daily Internet Usage vs. Time Spent on Site.
2. **Data Preprocessing**: Selecting relevant numerical and categorical features for the model.
3. **Model Training**: Implementing a Logistic Regression model using `Scikit-Learn`.
4. **Evaluation**: Measuring performance using a Classification Report and Confusion Matrix.

## Results
The Logistic Regression model achieved high accuracy in predicting user behavior, demonstrating strong precision and recall for both classes (clicked vs. not clicked).

## Requirements
To run this project, you will need:
* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

## How to Run
1. Clone the repository or download the files.
2. Ensure `advertising.csv` is in the same directory as the notebook.
3. Run the cells in `02-Logistic Regression Assignment.ipynb` sequentially.
