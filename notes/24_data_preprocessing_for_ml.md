# Data Preprocessing for Machine Learning

## Why Data Preprocessing?

Real-world data is rarely ready for Machine Learning.

It may contain:

- Missing values
- Categorical data
- Features with different scales
- Duplicate records
- Data leakage

Before training a model, we must prepare the data correctly.

This process is called **Data Preprocessing**.

---

# Types of Features

A feature is an input variable used by a Machine Learning model.

Features are broadly divided into two types.

## Numerical Features

Numerical features contain numbers and support mathematical operations.

Examples:

- Age
- Salary
- House Area
- House Price

Example:

Age = 25

Salary = ₹8,00,000

---

## Categorical Features

Categorical features represent labels or groups.

Examples:

- City
- Gender
- Property Type
- Color

Example:

Property Type

- Flat
- House
- Villa

Machine Learning models cannot directly understand text values.

These values must be converted into numbers.

---

# Types of Categorical Features

Categorical features are divided into two categories.

## Nominal Features

Nominal features have **no natural order**.

- Examples: City, Property Type, Color
- One category is not greater or smaller than another.

---

## Ordinal Features

Ordinal features have a **meaningful order**.

- Examples: Education Level, Customer Rating, T-Shirt Size
- The categories have an order (e.g. Small < Medium < Large).

---

# Encoding

Machine Learning models require numerical input.

Encoding converts categorical values into numerical representations.

Common encoding methods:

- One-Hot Encoding
- Label Encoding

---

# One-Hot Encoding

One-Hot Encoding creates a separate binary column for every category.

- Only one column contains 1 for each record.
- This is the preferred method for **Nominal Features**.

---

# Label Encoding

Label Encoding assigns an integer to every category.

- Suitable for **Ordinal Features** because the integer order preserves the natural order.
- Using Label Encoding for Nominal Features can incorrectly introduce an order where none exists.

---

# Feature Scaling

Different numerical features can have very different ranges.

Example:

Age

20–60

Salary

3,00,000–40,00,000

Large-scale features can dominate smaller-scale features.

Feature Scaling brings numerical features to comparable ranges.

Common methods:

- StandardScaler
- MinMaxScaler

---

# Train-Test Split

A Machine Learning model must be evaluated on unseen data.

The dataset is usually divided into:

- Training Set
- Test Set

The model learns from the training set and is evaluated on the test set.

This helps estimate how well it will perform on new data.

---

# Data Leakage

Data Leakage occurs when information from the test data is accidentally used during training.

This produces unrealistically good evaluation results.

Example:

Calculating scaling statistics using the entire dataset before splitting.

Correct approach:

Fit preprocessing only on the training data, then apply the same transformation to the test data.

---

# Pipeline

A Pipeline combines preprocessing and model training into a single workflow.

Benefits:

- Cleaner code
- Consistent preprocessing
- Easier deployment
- Reduced risk of data leakage

Scikit-learn provides the `Pipeline` class to build preprocessing and modeling workflows.

---

# Interview Questions

### What is data preprocessing?

Preparing raw data before training a Machine Learning model.

---

### What are numerical and categorical features?

Numerical features contain numbers.

Categorical features represent labels or groups.

---

### What is the difference between nominal and ordinal features?

Nominal features have no order.

Ordinal features have a meaningful order.

---

### When should One-Hot Encoding be used?

For nominal categorical features.

---

### When should Label Encoding be used?

For ordinal categorical features.

---

### What is feature scaling?

Transforming numerical features so they have comparable scales.

---

### What is data leakage?

Using information from the test data during training.

---

### Why are pipelines useful?

They keep preprocessing and model training together, making workflows more reliable and reducing the risk of data leakage.

---

# Summary

In this chapter, we learned:

- Data Preprocessing
- Numerical Features
- Categorical Features
- Nominal Features
- Ordinal Features
- One-Hot Encoding
- Label Encoding
- Feature Scaling
- Train-Test Split
- Data Leakage
- Pipeline