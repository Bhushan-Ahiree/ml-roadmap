# Regression Cross-Validation

## Why Regression Needs Cross-Validation

We already learned cross-validation for classification.

The same principle applies to regression.

The difference is the evaluation metric.

For regression we can evaluate models using:

- MAE
- RMSE
- R²

Cross-validation lets us evaluate a regression model across multiple validation folds instead of relying on one split.

---

# K-Fold Cross-Validation

For regression, K-Fold cross-validation is commonly used.

With 5-fold cross-validation:

1. The training data is divided into 5 folds.
2. Four folds are used for training.
3. One fold is used for validation.
4. The process is repeated five times.
5. The scores are summarized.

---

# Regression Scoring in scikit-learn

Some regression metrics are losses where lower values are better.

However, scikit-learn's scoring system follows a "higher is better" convention.

Therefore:

- `neg_mean_absolute_error`
- `neg_root_mean_squared_error`

return negative values.

For example:

`-0.50` means an actual MAE of `0.50`.

When interpreting these metrics, we convert them back to positive error values.

---

# Important Rule

Cross-validation should be performed on the training data when a final test set has been reserved.

The final test set should remain untouched during model comparison.

---

# Key Takeaway

Cross-validation works for both classification and regression.

The main difference is the scoring metric used to evaluate the predictions.