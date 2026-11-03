# Obesity Risk: Tree-Based Methods (Assignment 6)

Amari Ware · DDS-8555 Predictive Analysis · National University

`Ware_Assignment6.ipynb` (executed on Kaggle) contains:
- ISLP Ch. 8, Conceptual Question 1: a seven-region recursive binary partition and its decision tree
- ISLP Ch. 8, Applied Question 12 (`Carseats`): bagging, random forest, boosting and BART vs. linear, ridge and lasso regression
- Kaggle Playground Series S4E2: decision tree, bagging, random forest and gradient boosting, with an L2-regularized logistic regression baseline and assumption checks

`figures/` holds the plots exported from the notebook and a screenshot of the Kaggle submissions.

## Kaggle results (accuracy, late submissions)

| Model | 5-fold CV | Public | Private |
|---|---|---|---|
| Gradient boosting (histogram-based, tuned) | 0.9048 | 0.90751 | 0.90426 |
| Random forest (500 trees, max_features = sqrt) | 0.9017 | 0.90065 | 0.89956 |
| Bagging (300 trees) | 0.8912 | 0.89234 | 0.89243 |
| Decision tree (max_depth = 10, min_samples_leaf = 5) | 0.8763 | 0.88403 | 0.88141 |
| Regularized logistic regression (baseline, not submitted) | 0.8669 | - | - |

Note: the bagging file was accidentally submitted twice (once labeled "Boosting"); the corrected boosting submission is the one scoring 0.90751 public.

## Applied Question 12 (`Carseats`, test MSE, 50/50 split)

| Model | Test MSE |
|---|---|
| Lasso (CV) | 1.107 |
| Ridge (CV) | 1.112 |
| Linear regression (OLS) | 1.125 |
| BART | 1.561 |
| Boosting | 1.942 |
| Bagging | 2.677 |
| Random forest | 2.983 |

## Data
Competition data: https://www.kaggle.com/competitions/playground-series-s4e2 (not redistributed; see the competition rules).
To reproduce, open the notebook in a Kaggle notebook attached to the competition, turn Internet on, and choose Save Version → Save & Run All.
