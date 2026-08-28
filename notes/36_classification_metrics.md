# Classification Metrics

## Why Accuracy Is Not Always Enough

Accuracy measures the proportion of predictions that are correct.

However, accuracy alone can be misleading, especially when classes are imbalanced or when different types of mistakes have different consequences.

For classification, we should also understand:

- Confusion Matrix
- Precision
- Recall
- F1-score

---

# Confusion Matrix

A confusion matrix compares:

- Actual classes
- Predicted classes

For binary classification, it contains:

- True Positive (TP)
- True Negative (TN)
- False Positive (FP)
- False Negative (FN)

For multi-class classification, the matrix contains one row and column for each class.

---

# Precision

Precision answers:

"Of the observations predicted as positive, how many were actually positive?"

High precision means relatively few false positives.

---

# Recall

Recall answers:

"Of the actual positive observations, how many did the model correctly identify?"

High recall means relatively few false negatives.

---

# F1-score

F1-score combines precision and recall using their harmonic mean.

It is useful when we want a balance between precision and recall.

---

# When Accuracy Can Be Misleading

Suppose 95% of observations belong to Class A and only 5% belong to Class B.

A model that always predicts Class A would achieve 95% accuracy while completely failing to identify Class B.

This is why accuracy should not automatically be treated as the best metric.

---

# Choosing a Metric

Accuracy:
- Useful when classes are reasonably balanced and prediction errors have similar importance.

Precision:
- Important when false positives are costly.

Recall:
- Important when false negatives are costly.

F1-score:
- Useful when both precision and recall matter.

---

# Interview Questions

### What is a confusion matrix?

A table comparing actual and predicted classes.

### What is precision?

The proportion of predicted positives that are actually positive.

### What is recall?

The proportion of actual positives that are correctly identified.

### What is F1-score?

A metric that combines precision and recall.

### Why can accuracy be misleading?

Because a high accuracy can hide poor performance on a minority class.