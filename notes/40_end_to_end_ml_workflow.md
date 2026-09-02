# End-to-End Machine Learning Workflow

## Purpose

This notebook brings together the core Machine Learning workflow learned throughout the roadmap.

The goal is not to learn a new algorithm.

The goal is to understand how the individual steps fit together into a complete ML workflow.

---

# Complete Workflow

1. Define the problem.
2. Load the data.
3. Understand the data.
4. Split the data.
5. Perform prepr ocessing.
6. Build a baseline.
7. Train candidate models.
8. Evaluate models using cross-validation.
9. Tune important hyperparameters.
10. Select the final model.
11. Evaluate once on the untouched test set.
12. Save the trained model.

---

# Data Leakage Rule

The test set must remain separate from model selection.

It should not be used to:

- Fit preprocessing
- Select features
- Compare models
- Tune hyperparameters
- Make repeated modeling decisions

The test set is used for the final evaluation.

---

# Model Selection Workflow

Training data:

    Cross-validation
          ↓
    Model comparison
          ↓
    Hyperparameter tuning
          ↓
    Select final model

Then:

    Final model
          ↓
    Untouched test set
          ↓
    Final evaluation

---

# Reproducibility

A good ML workflow should be reproducible.

Important practices include:

- fixed random states where appropriate
- consistent preprocessing
- Pipelines
- clearly defined train/test splits
- saved model artifacts
- documented dependencies

---

# Production Perspective

A Machine Learning project does not end when a model achieves a good score.

A production workflow also needs:

- reproducible training
- model serialization
- input validation
- prediction interface
- monitoring and maintenance

These topics will be implemented later through projects rather than studied as isolated theory.

---

# Final Foundation Checkpoint

At this point we have covered the core workflow required for our first serious ML project.

We will now move from learning isolated concepts to applying them in a real project.