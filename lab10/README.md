# SVM Assignment – Iris Flower Classification

A Support Vector Machine (SVM) classifier built on the classic Iris flower dataset, covering exploratory data analysis, model training, evaluation, and hyperparameter tuning with GridSearchCV.

## Overview

The Iris dataset contains 150 samples from three species of Iris flowers (*setosa*, *versicolor*, *virginica*), each described by four features: sepal length, sepal width, petal length, and petal width. The goal is to train an SVM classifier to correctly identify the species.

## Project Structure

```
02-SVM_Assignment_completed.ipynb   # Main notebook with all completed code
README.md                           # This file
```

## Notebook Walkthrough

### 1. Data Loading
The Iris dataset is loaded via `sklearn.datasets.load_iris` and converted into a pandas DataFrame.

### 2. Exploratory Data Analysis
- **Pairplot** – visualizes pairwise relationships across all four features, colored by species. *Iris setosa* is the most separable species.
- **KDE Plot** – shows the joint distribution of sepal length vs. sepal width for the setosa species.

### 3. Train/Test Split
The data is split 70/30 into training and test sets using `train_test_split` with `random_state=101`.

### 4. Model Training
An SVM classifier (`SVC`) from scikit-learn is trained on the training set using default parameters (RBF kernel).

### 5. Model Evaluation
The model is evaluated using a confusion matrix and classification report, achieving **~98% accuracy** on the test set.

### 6. GridSearchCV Hyperparameter Tuning
A grid search is performed over:
- `C`: [0.1, 1, 10, 100]
- `gamma`: [1, 0.1, 0.01, 0.001]

The tuned model yields the same ~98% accuracy, confirming the default parameters are already near-optimal for this dataset.

## Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter
```

Install with:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

## Usage

```bash
jupyter notebook 02-SVM_Assignment_completed.ipynb
```

## Results

| Metric    | Score |
|-----------|-------|
| Accuracy  | 98%   |
| Precision | 0.98  |
| Recall    | 0.98  |
| F1-Score  | 0.98  |
