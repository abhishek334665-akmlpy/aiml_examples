# Wine Quality — Machine Learning Regression Pipeline

## Objective

Build a machine learning regression pipeline from scratch using the
UCI Wine Quality dataset.

The objective is to understand the complete machine learning workflow,
rather than simply train a model and obtain a prediction.

## Dataset

Wine Quality dataset from the UCI Machine Learning Repository.

The dataset contains physicochemical measurements of wine samples and
a sensory quality score.

Source:
https://archive.ics.uci.edu/dataset/186/wine+quality

Dataset citation:

Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009).
Wine Quality [Dataset]. UCI Machine Learning Repository.
https://doi.org/10.24432/C56S3T

License:
CC BY 4.0

## Current Pipeline

1. Load dataset
2. Initial data inspection
3. Check missing values
4. Check duplicate records
5. Remove exact duplicate records
6. Explore target distribution
7. Separate features and target
8. Train-test split
9. Train Linear Regression baseline
10. Evaluate predictions
11. Compare training and test performance
12. Experiment with feature scaling

## Dataset After Cleaning

Original rows: 1599

Exact duplicate rows: 240

Rows after removing duplicates: 1359

Features: 11

Target: `quality`

All features are numerical.

## Baseline Model

Linear Regression was used as the first baseline model.

### Test Results

- Mean Absolute Error (MAE): 0.5041
- Mean Squared Error (MSE): 0.4311
- Root Mean Squared Error (RMSE): 0.6565
- R-squared (R²): 0.3915

## Training vs Test

Training and test performance were compared to investigate
generalization and possible overfitting.

The results did not show a large training-test performance gap.

## Next Experiments

- Polynomial Regression
- Model complexity and overfitting
- Validation
- Additional regression algorithms
- Model comparison