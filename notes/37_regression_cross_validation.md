# Regression Cross-Validation

## Why Regression Needs Cross-Validation

We previously learned cross-validation for classification.

The same principle applies to regression, but the evaluation metrics are different.

Instead of accuracy, regression models can be evaluated using metrics such as:

- MAE
- RMSE
- R²

Cross-validation allows us to estimate how consistently a regression model performs across different training and validation splits.

---

# K-Fold Cross-Validation for Regression

For regression, standard K-Fold cross-validation is commonly used.

The data is divided into K folds.

For each iteration:

1. K-1 folds are used for training.
2. The remaining fold is used for validation.
3. The model is evaluated.
4. The process is repeated for every fold.

The final result is summarized across the folds.

---

# Regression Scoring in scikit-learn

Some regression metrics are losses where lower values are better.

However, scikit-learn's scoring system is designed so that higher scores are better.

Therefore, loss metrics such as MAE and RMSE are represented as negative scores during cross-validation.

For example:

`neg_mean_absolute_error`

A value of `-0.50` corresponds to an MAE of `0.50`.

When interpreting the result, take the absolute value.

---

# Important Rule

The final test set should remain untouched while comparing models using cross-validation.

Cross-validation is performed on the training data.

After selecting the model, the final model is evaluated on the held-out test set.

---

# Key Takeaway

Cross-validation is not limited to classification.

The same model-selection workflow can be used for regression by changing the evaluation metric.