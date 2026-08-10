# Decision Tree Classification

## What is a Decision Tree?

A Decision Tree is a supervised Machine Learning algorithm that makes predictions by learning a sequence of decision rules from the training data.

For classification, each final leaf represents a predicted class.

A simple example:

If petal length < X
→ Class A

Otherwise
→ Class B

The tree continues creating rules until it reaches a prediction.

---

# How Does a Decision Tree Work?

A tree consists of:

- Root node
- Decision nodes
- Branches
- Leaf nodes

At each decision node, the algorithm chooses a feature and split that helps separate the classes.

---

# Why Decision Trees Are Useful

Decision Trees can model non-linear relationships.

Unlike Logistic Regression, they do not require the relationship between features and the target to be approximately linear.

---

# Feature Scaling

Decision Trees do not require feature scaling.

This is different from algorithms such as KNN, where distance calculations make scaling important.

---

# Overfitting

A Decision Tree can become very deep and learn very specific patterns from the training data.

This can cause overfitting.

Important parameters such as `max_depth`, `min_samples_split`, and `min_samples_leaf` can control tree complexity.

---

# Advantages

- Easy to understand.
- Can model non-linear relationships.
- Does not require feature scaling.
- Can provide feature importance.
- Works for both classification and regression.

# Limitations

- Can overfit easily.
- Small changes in training data can produce a different tree.
- A single tree may generalize worse than ensemble methods such as Random Forest.

---

# Interview Questions

### Does a Decision Tree require feature scaling?

No.

### Can Decision Trees model non-linear relationships?

Yes.

### What is overfitting in a Decision Tree?

When the tree becomes too complex and learns noise or very specific patterns from the training data.

### How can tree complexity be controlled?

Parameters such as `max_depth`, `min_samples_split`, and `min_samples_leaf` can be used.

### What is a leaf?

A final node of the tree where a prediction is made.