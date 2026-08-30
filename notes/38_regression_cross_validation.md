# Regression Cross-Validation & Model Comparison

## Why Cross-Validation for Regression?

A single train/test split gives us only one estimate of model performance.

The result can depend on which observations happen to be placed in the test set.

Cross-validation allows us to evaluate a regression model across multiple validation folds.

---

# Regression Cross-Validation

For regression, K-Fold cross-validation is commonly used.

With 5-fold cross-validation:

1. The training data is divided into five folds.
2. Four folds are used for training.
3. One fold is used for validation.
4. This is repeated until every fold has been used for validation.
5. The validation scores are averaged.

---

# Choosing a Regression Metric

Unlike classification, regression does not use accuracy.

We can evaluate regression models using metrics such as:

- MAE
- RMSE
- R²

In this notebook, we'll use MAE for model comparison.

Lower MAE is better.

---

# Important Rule

The final test set remains untouched during model comparison.

Cross-validation is performed only on the training data.

After selecting a model, we evaluate it once on the final test set.

---

# Why Use a Single Metric for Comparison?

Using one primary metric makes model comparison straightforward.

The choice should depend on the real problem.

Here we use MAE because it is easy to interpret as average absolute prediction error.

Other metrics can still be reported when evaluating the final model.