# Naive Bayes

## What is Naive Bayes?

Naive Bayes is a supervised Machine Learning algorithm based on Bayes' theorem.

It predicts the class of an observation by estimating how likely the observed features are for each possible class.

The "naive" assumption is that the features are conditionally independent given the class.

---

# Gaussian Naive Bayes

Naive Bayes has different variants depending on the type of data.

For continuous numerical features, we can use:

GaussianNB

It assumes that each feature follows a Gaussian (normal) distribution within each class.

---

# How It Works

For a new observation, Naive Bayes:

1. Considers each possible class.
2. Estimates how likely the observed features are for that class.
3. Combines these probabilities.
4. Predicts the class with the highest resulting probability.

---

# Why "Naive"?

The algorithm makes a strong simplifying assumption:

The features are conditionally independent given the class.

This assumption is often not completely true in real datasets.

Despite this simplification, Naive Bayes can work well in practice.

---

# Advantages

- Simple and fast.
- Works well with relatively small datasets.
- Can work well with high-dimensional data.
- Useful for classification problems such as text classification.

# Limitations

- The independence assumption can be unrealistic.
- Performance can suffer when features are strongly dependent.
- Probability estimates should not automatically be interpreted as highly accurate probabilities.

---

# When Should You Use It?

Naive Bayes is especially useful when:

- Fast training and prediction are important.
- The dataset is relatively small or high-dimensional.
- Features provide useful independent evidence about the class.
- Working with text classification.

---

# Interview Questions

### What is Naive Bayes?

A supervised classification algorithm based on Bayes' theorem with a conditional-independence assumption.

### Why is it called "naive"?

Because it assumes that features are conditionally independent given the class.

### What is GaussianNB?

A Naive Bayes classifier designed for continuous features whose likelihood is modeled using Gaussian distributions.

### Is feature scaling required for GaussianNB?

No. GaussianNB does not require feature scaling in the same way distance-based algorithms such as KNN do.

---

# Summary

In this chapter, we learned:

- Naive Bayes
- The naive independence assumption
- Gaussian Naive Bayes
- How Naive Bayes makes predictions
- Advantages and limitations
- When Naive Bayes is useful