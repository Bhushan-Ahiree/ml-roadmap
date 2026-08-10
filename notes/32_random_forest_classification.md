# Random Forest Classification

## What is Random Forest?

Random Forest is an ensemble Machine Learning algorithm that combines multiple Decision Trees.

Instead of relying on one Decision Tree, Random Forest builds many trees and combines their predictions.

For classification, the forest uses the predictions from its trees to determine the final class.

---

# Why Use Multiple Trees?

A single Decision Tree can be sensitive to the training data and can overfit.

Random Forest reduces this problem by combining many different trees.

The trees are trained using randomized samples of the training data and randomized feature selection.

This creates a collection of different trees rather than identical copies.

---

# How Random Forest Works

A simplified process:

1. Create multiple training samples using random sampling.
2. Train a Decision Tree on each sample.
3. Randomly consider subsets of features when splitting trees.
4. Collect predictions from all trees.
5. Combine the predictions to produce the final prediction.

---

# Important Parameter: n_estimators

`n_estimators` controls the number of trees in the forest.

For example:

`n_estimators=100`

means the forest contains 100 trees.

More trees can generally make the model more stable, but they also require more computation.

---

# Feature Scaling

Random Forest does not require feature scaling.

This is because it is based on tree splits rather than distance calculations.

---

# Overfitting

Random Forest is generally more robust than a single Decision Tree, but it can still overfit depending on the data and model configuration.

Parameters such as:

- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

can control tree complexity.

---

# Advantages

- Usually more robust than a single Decision Tree.
- Can model non-linear relationships.
- Does not require feature scaling.
- Can provide feature importance.
- Works for classification and regression.

# Limitations

- Less interpretable than a single Decision Tree.
- Requires more computation than one tree.
- A large forest can consume more memory.

---

# Interview Questions

### What is Random Forest?

An ensemble of Decision Trees whose predictions are combined to produce a final prediction.

### Why is Random Forest usually more robust than one Decision Tree?

Because it combines predictions from many different trees instead of relying on one tree.

### What does `n_estimators` mean?

The number of trees in the forest.

### Does Random Forest require feature scaling?

No.

### Can Random Forest overfit?

Yes, although it is generally more robust than a single Decision Tree.

---

# Summary

In this chapter, we learned:

- Random Forest
- Why multiple trees are used
- How Random Forest combines trees
- `n_estimators`
- Feature scaling requirements
- Advantages and limitations