# K-Nearest Neighbors (KNN)

## What is KNN?

K-Nearest Neighbors (KNN) is a supervised Machine Learning algorithm that makes predictions based on the similarity between observations.

For classification, KNN looks at the `k` closest training observations and assigns the class that receives the majority vote.

---

# How KNN Works

For a new observation:

1. Calculate its distance from training observations.
2. Find the `k` nearest observations.
3. Look at their classes.
4. Choose the class with the majority vote.

The value of `k` controls how many neighbors participate in the prediction.

---

# Example

Suppose `k = 5`.

Among the five nearest observations:

- Class A → 3
- Class B → 2

The model predicts:

Class A

---

# Why Feature Scaling Matters

KNN relies on distances between observations.

If one feature has a much larger numerical scale than another, it can dominate the distance calculation.

Therefore, feature scaling is generally important before using KNN.

A Pipeline is a good way to ensure scaling is applied consistently.

---

# Choosing K

Small `k`:

- More sensitive to individual observations.
- Can produce a more complex decision boundary.
- Can be sensitive to noise.

Large `k`:

- Considers more observations.
- Produces smoother decision boundaries.
- Can become too general.

The best value of `k` depends on the dataset.

---

# Advantages

- Simple to understand.
- Can model non-linear decision boundaries.
- Can naturally handle multi-class classification.

# Limitations

- Prediction can become expensive as the dataset grows.
- Sensitive to feature scaling.
- Sensitive to the choice of `k`.
- Performance can degrade with many irrelevant or high-dimensional features.

---

# Interview Questions

### What is KNN?

A supervised learning algorithm that predicts using the nearest training observations.

### What does K represent?

The number of nearest neighbors considered for making a prediction.

### Why is feature scaling important for KNN?

Because KNN relies on distance calculations.

### What happens when K is very small?

The model becomes more sensitive to individual observations and noise.

### What happens when K is very large?

The model becomes smoother and may lose important local patterns.

### Does KNN require training?

KNN does not learn a traditional parameterized model like Linear Regression. It largely stores the training observations and uses them when making predictions.

---

# Summary

In this chapter, we learned:

- K-Nearest Neighbors
- How KNN makes predictions
- The role of K
- Why feature scaling matters
- Advantages and limitations