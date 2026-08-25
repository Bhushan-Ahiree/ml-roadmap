# Support Vector Machine (SVM)

## What is SVM?

Support Vector Machine (SVM) is a supervised Machine Learning algorithm used for classification and regression.

For classification, SVM tries to find a decision boundary that separates different classes.

The algorithm aims to find a boundary with a large margin between the classes.

---

# What is the Margin?

The margin is the distance between the decision boundary and the closest observations from each class.

SVM tries to find a boundary that maximizes this margin.

---

# Support Vectors

The observations closest to the decision boundary are called support vectors.

They are important because they strongly influence the position of the decision boundary.

---

# Linear vs Non-Linear Separation

Some datasets can be separated using a straight decision boundary.

Other datasets require a more complex boundary.

SVM can use kernels to handle non-linear relationships.

Common kernels include:

- Linear
- Polynomial
- RBF

For practical work, the RBF kernel is a common starting point for non-linear classification.

---

# Feature Scaling

SVM is sensitive to feature scales.

Features with very different scales can affect the model's objective and kernel calculations.

Therefore, feature scaling should generally be used with SVM.

A Pipeline is a good way to combine scaling and the model.

---

# Important Parameter: C

`C` controls the trade-off between:

- A wider margin with some classification errors.
- A narrower margin with fewer training errors.

A larger `C` places more emphasis on correctly classifying training observations.

A smaller `C` allows more training errors in exchange for stronger regularization.

---

# Advantages

- Effective for many classification problems.
- Can model non-linear relationships using kernels.
- Works well in high-dimensional feature spaces.
- Can handle binary and multi-class classification.

# Limitations

- Requires feature scaling.
- Can be computationally expensive for large datasets.
- Kernel and parameter choices can strongly affect performance.

---

# Interview Questions

### What is the main idea behind SVM?

Find a decision boundary that separates classes while maximizing the margin.

### What are support vectors?

Training observations closest to the decision boundary that strongly influence it.

### Why is scaling important for SVM?

Because SVM is sensitive to feature scales.

### What does C control?

The trade-off between a wider margin and training classification errors.

### What is a kernel?

A method that allows SVM to model relationships that are not easily separated by a simple linear boundary.