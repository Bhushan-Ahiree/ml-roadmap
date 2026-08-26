# Hyperparameter Tuning

## What is a Hyperparameter?

A hyperparameter is a setting chosen before training the model.

Examples:

- KNN → `n_neighbors`
- Decision Tree → `max_depth`
- Random Forest → `n_estimators`
- SVM → `C`, `kernel`

These values are not learned directly from the training data.

---

# Why Tune Hyperparameters?

Different hyperparameter values can produce different model performance.

Instead of manually guessing a value, we can evaluate several possible values using cross-validation.

---

# GridSearchCV

`GridSearchCV` combines:

1. A set of candidate hyperparameter values.
2. Cross-validation.
3. Model evaluation.
4. Selection of the best parameter combination.

For each combination, the model is evaluated using cross-validation.

---

# Important Rule

The final test set must remain untouched during hyperparameter tuning.

GridSearchCV operates on the training data.

After selecting the best configuration, the final model is evaluated on the held-out test set.

---

# Important Terms

### `param_grid`

The hyperparameter values we want to test.

### `cv`

The number of cross-validation folds.

### `best_params_`

The parameter combination that produced the best CV score.

### `best_score_`

The best mean cross-validation score found during the search.

### `best_estimator_`

The model using the best hyperparameter combination.

---

# Summary

In this chapter, we learned:

- What hyperparameters are.
- Why hyperparameters are tuned.
- How GridSearchCV works.
- How GridSearchCV uses cross-validation.
- Why the test set must remain untouched.