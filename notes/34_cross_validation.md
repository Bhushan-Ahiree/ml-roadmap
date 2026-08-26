# Cross-Validation & Model Comparison

## Why Do We Need Cross-Validation?

A single train/test split gives us one estimate of model performance.

The result can depend on which observations happened to be placed in the test set.

This makes it difficult to confidently compare models using only one split.

Cross-validation gives us a more reliable estimate by evaluating the model across multiple splits of the training data.

---

# K-Fold Cross-Validation

In K-fold cross-validation:

1. Divide the training data into K folds.
2. Train the model using K-1 folds.
3. Validate it using the remaining fold.
4. Repeat until every fold has been used for validation.
5. Calculate the average validation score.

For classification, scikit-learn uses stratified folds by default when an integer is supplied for `cv`.

---

# Why Keep a Test Set?

The test set should remain untouched during model selection.

Cross-validation is performed on the training data.

After selecting the model, the final model can be evaluated once on the held-out test set.

This helps prevent information from the test set influencing model selection.

---

# Mean and Standard Deviation

Cross-validation produces multiple scores.

We usually examine:

- Mean score → average performance.
- Standard deviation → variation across folds.

A model with a slightly lower mean but much more stable performance may sometimes be preferable to a model with a higher but highly variable score.

---

# Important Rule

Do not repeatedly change a model based on the test-set score.

Use cross-validation for model selection.

Use the test set for the final evaluation.