# Regression Algorithms

## Why Different Regression Algorithms?

No single algorithm performs best on every dataset.

Different algorithms make different assumptions and have different strengths.

Choosing the right algorithm depends on the problem and the data.

---

# Linear Regression

Linear Regression models a linear relationship between features and the target.

Advantages

- Simple
- Fast
- Easy to interpret

Limitations

- Assumes a linear relationship
- Sensitive to outliers
- May underfit complex data

---

# Ridge Regression

Ridge Regression is an extension of Linear Regression.

It reduces overfitting by penalizing large model coefficients.

Advantages

- Reduces overfitting
- Handles multicollinearity better
- Usually more stable than Linear Regression

---

# Lasso Regression

Lasso Regression also applies regularization.

Unlike Ridge, it can reduce some feature coefficients to zero.

Advantages

- Performs feature selection
- Produces simpler models

---

# ElasticNet

ElasticNet combines Ridge and Lasso.

Advantages

- Performs regularization
- Can perform feature selection
- Useful when many features are correlated

---

# Decision Tree Regressor

Decision Trees learn decision rules by repeatedly splitting the data.

Advantages

- Captures non-linear relationships
- Easy to visualize
- No feature scaling required

Limitations

- Can overfit easily

---

# Random Forest Regressor

Random Forest combines many Decision Trees.

Final prediction = Average prediction from all trees.

Advantages

- Better generalization
- Lower overfitting risk
- Handles complex patterns

Limitations

- Slower than a single Decision Tree
- Less interpretable

---

# Algorithm Comparison

| Algorithm | Scaling | Feature Selection | Overfitting Risk |
|-----------|---------|-------------------|------------------|
| Linear Regression | Often Helpful | No | Low |
| Ridge | Often Helpful | No | Low |
| Lasso | Often Helpful | Yes | Low |
| ElasticNet | Often Helpful | Partial | Low |
| Decision Tree | No | No | High |
| Random Forest | No | No | Low |

---

# Interview Questions

### Which regression algorithm is the simplest?

Linear Regression.

---

### Which algorithm performs feature selection?

Lasso Regression.

---

### Which algorithms usually require feature scaling?

Linear Regression, Ridge, Lasso and ElasticNet.

---

### Which tree-based algorithms usually do not require scaling?

Decision Tree and Random Forest.

---

### Why is Random Forest usually better than a Decision Tree?

Because it averages predictions from multiple trees, reducing overfitting.

---

# Summary

In this chapter, we learned:

- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Decision Tree Regressor
- Random Forest Regressor
- Choosing the right regression algorithm