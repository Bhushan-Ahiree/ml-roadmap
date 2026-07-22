# Model Evaluation

## Why Evaluate a Model?

After training a model, we need to know how well it performs on unseen data.

A model that performs well on training data but poorly on new data is not useful.

---

## Mean Absolute Error (MAE)

Measures the average absolute difference between actual and predicted values.

Formula

Average of |Actual − Predicted|

Lower MAE = Better model

---

## Mean Squared Error (MSE)

Squares the errors before averaging.

Large errors are penalized more.

Lower MSE = Better model

---

## Root Mean Squared Error (RMSE)

Square root of MSE.

RMSE is easier to interpret because it has the same unit as the target.

Lower RMSE = Better model

---

## R² Score

Measures how well the model explains the variation in the data.

Range

0 → Poor

1 → Perfect

Higher R² = Better model

---

## Key Takeaways

MAE → Average error

MSE → Penalizes large errors

RMSE → Error in original units

R² → Goodness of fit