# Regression Fundamentals

## What is Regression?

Regression is a supervised Machine Learning technique used to predict **continuous numerical values**.

Examples:

- House Price
- Salary
- Temperature
- Stock Price

---

# Regression vs Classification

Regression predicts numbers.

Examples:

- ₹75,00,000
- 32°C
- ₹8,50,000 Salary

Classification predicts categories.

Examples:

- Spam / Not Spam
- Fraud / Not Fraud
- Disease / No Disease

---

# Linear Regression

Linear Regression assumes a linear relationship between the input features and the target variable.

It tries to find the best-fit line that minimizes prediction errors.

---

# Best-Fit Line

The best-fit line is the line that produces the smallest overall prediction error for the training data.

The model learns this line during training.

---

# Residual (Error)

A residual is the difference between:

Actual Value − Predicted Value

Smaller residuals indicate better predictions.

---

# Cost Function

A cost function measures how well a model performs.

Large prediction errors produce a higher cost.

The objective of training is to minimize this cost.

---

# Underfitting

Underfitting occurs when the model is too simple to learn the underlying pattern.

Characteristics:

- High Training Error
- High Test Error

---

# Overfitting

Overfitting occurs when the model memorizes the training data instead of learning general patterns.

Characteristics:

- Very Low Training Error
- High Test Error

---

# Bias and Variance

High Bias

- Model is too simple.
- Often causes underfitting.

High Variance

- Model is too complex.
- Often causes overfitting.

A good model balances both.

---

# Regularization

Regularization helps reduce overfitting by limiting model complexity.

Common techniques:

- Ridge Regression
- Lasso Regression
- ElasticNet

---

# Interview Questions

### What is Regression?

A supervised learning technique used to predict continuous numerical values.

---

### What is Linear Regression?

A regression algorithm that models a linear relationship between input features and the target.

---

### What is a residual?

The difference between the actual value and the predicted value.

---

### What is underfitting?

A model that is too simple to learn the underlying pattern.

---

### What is overfitting?

A model that memorizes training data and performs poorly on unseen data.

---

### What is regularization?

A technique used to reduce overfitting by controlling model complexity.

---

# Summary

In this chapter, we learned:

- Regression
- Regression vs Classification
- Linear Regression
- Best-Fit Line
- Residual
- Cost Function
- Underfitting
- Overfitting
- Bias vs Variance
- Regularization