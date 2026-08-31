# Pipelines & Data Leakage

## Why This Matters

A Machine Learning model can appear to perform very well while actually being built incorrectly.

One major cause is data leakage.

Data leakage happens when information that should not be available during training is used while building the model.

This can produce overly optimistic evaluation results.

---

# A Common Leakage Problem

Suppose we want to standardize features.

Incorrect approach:

1. Use the entire dataset to fit the scaler.
2. Split the data.
3. Train the model.

The scaler has now learned information from the future test data.

Correct approach:

1. Split the data.
2. Fit the scaler only on the training data.
3. Transform the training data.
4. Transform the test data using the already-fitted scaler.
5. Train the model.

---

# Why Pipelines Help

A Pipeline combines preprocessing and the model into one object.

For example:

StandardScaler → LogisticRegression

When the pipeline is used with cross-validation, the preprocessing step is fitted separately inside each training fold.

This helps prevent information from the validation fold from leaking into preprocessing.

---

# Core Rule

Never use test data to:

- Fit preprocessing
- Select features
- Tune hyperparameters
- Select a model
- Make modeling decisions

The test set should remain unseen until final evaluation.

---

# Pipeline Structure

A typical workflow is:

Raw Features
↓
Preprocessing
↓
Model
↓
Prediction

The preprocessing and model can be stored together inside one Pipeline.

---

# Key Takeaways

- Data leakage produces overly optimistic results.
- Preprocessing must be learned from training data only.
- Test data should only be transformed using preprocessing already fitted on training data.
- Pipelines help enforce this workflow.
- Pipelines are especially important when using cross-validation and hyperparameter tuning.