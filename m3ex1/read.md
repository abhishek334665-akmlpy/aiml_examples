# Student Performance — Linear Regression

## Objective

Build a simple Machine Learning regression pipeline from scratch using the Student Performance dataset.

The objective is to understand the complete workflow:

Dataset → Inspection → Feature/Target Selection → EDA → Train/Test Split → Model Training → Prediction → Evaluation → Feature Comparison

## Dataset

Student Performance dataset containing student demographic, social and academic information.

For this experiment, only numerical academic features are used:

- G1 — first-period grade
- G2 — second-period grade

Target:

- G3 — final grade

## Machine Learning Approach

This is a supervised learning regression problem because the target (`G3`) is a numerical value.

We use:

- Linear Regression
- Train/Test Split
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

## Experiments

Three Linear Regression models are compared:

1. G1 → G3
2. G2 → G3
3. G1 + G2 → G3

The same train/test methodology and evaluation metrics are used for each experiment.

## Learning Objectives

This example demonstrates:

- Initial dataset inspection
- Feature and target selection
- Basic Exploratory Data Analysis (EDA)
- Train/Test splitting
- Linear Regression
- Model coefficients and intercept
- Making predictions
- Regression model evaluation
- Comparing feature sets
- Understanding why model selection should be based on evidence rather than arbitrary metric cutoffs

## Project Structure

```text
/
├── Module3_Student_Performance_Regression.ipynb
└── student/
    └── student-mat.csv