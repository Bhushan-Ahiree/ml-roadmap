# Exploratory Data Analysis (EDA)

## What is EDA?

EDA is the process of understanding a dataset before building a machine learning model.

The goal is to discover:

- Data types
- Missing values
- Duplicate data
- Outliers
- Relationships
- Patterns

---

## Typical EDA Workflow

1. Load dataset

2. Check shape

3. Check info()

4. Check missing values

5. Check statistics

6. Check unique values

7. Visualize data

---

## Useful Functions

df.head()

df.shape

df.info()

df.describe()

df.isnull().sum()

df.nunique()

df.value_counts()

---

## Why EDA?

Good EDA

↓

Better Features

↓

Better Model

---

## Key Takeaways

- Always explore a dataset before building a model.
- EDA reveals missing values, outliers, distributions, and relationships.
- Good EDA leads to better features and better models.

---

# Interview Questions

### What is EDA?

Exploratory Data Analysis. The process of understanding a dataset systematically before building a model.

---

### Why do we perform EDA before modelling?

To understand data types, detect missing values, find outliers, and discover patterns that guide feature engineering decisions.

---

### Name three common EDA functions in Pandas.

`df.info()`, `df.describe()`, `df.isnull().sum()`