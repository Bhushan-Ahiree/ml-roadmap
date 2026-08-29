# Regression Evaluation Metrics

## Why Regression Needs Different Metrics

Classification predicts classes.

Regression predicts continuous numerical values.

Therefore, regression needs metrics that measure the size of prediction errors.

The core metrics we need are:

- MAE
- MSE
- RMSE
- R²

---

# MAE — Mean Absolute Error

MAE measures the average absolute difference between actual and predicted values.

It is easy to interpret because it is expressed in the same units as the target.

Lower MAE is better.

---

# MSE — Mean Squared Error

MSE calculates the average squared prediction error.

Because errors are squared, larger errors receive greater weight.

Lower MSE is better.

---

# RMSE — Root Mean Squared Error

RMSE is the square root of MSE.

It is also expressed in the same units as the target.

RMSE penalizes larger errors more strongly than MAE.

Lower RMSE is better.

---

# R² — Coefficient of Determination

R² measures how much of the variation in the target is explained by the model relative to a baseline that predicts the mean.

A score of:

- 1.0 → perfect predictions
- 0.0 → equivalent to predicting the mean
- Less than 0 → worse than the mean baseline

Higher R² is better.

---

# Comparing Metrics

| Metric | Measures | Better |
|---|---|---|
| MAE | Average absolute error | Lower |
| MSE | Squared error | Lower |
| RMSE | Root of squared error | Lower |
| R² | Explained variance relative to mean baseline | Higher |

---

# Which Metric Should We Use?

There is no universally best regression metric.

Use the metric that matches the business problem.

MAE is useful when we want an easily interpretable average error.

RMSE is useful when larger errors should receive more penalty.

R² is useful for describing how much variation the model explains relative to a mean baseline.

In practice, it is often useful to report more than one metric.

---

# Important Rule

Never decide that a model is good or bad from R² alone.

Always consider the actual prediction error and the problem context.