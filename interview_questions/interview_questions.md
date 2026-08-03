## Interview Questions

---

## Types of Machine Learning

### Q1. Why is House Price Prediction supervised learning?

Answer:
Because the training dataset already contains the correct property prices
(labels), allowing the model to learn the relationship between features and price.

---

### Q2. What is the difference between supervised and unsupervised learning?

Answer:
Supervised learning uses labeled data to make predictions, while unsupervised
learning uses unlabeled data to discover hidden patterns or groups.

---

### Q3. Is Reinforcement Learning supervised?

Answer:
No. Reinforcement Learning learns through interaction with an environment using
rewards and penalties rather than labeled examples.

---

## NumPy Shapes & Dimensions

### Difference between shape and size?

Shape is the size of each dimension (e.g. (3, 4) means 3 rows and 4 columns).
Size is the total number of elements (e.g. 12).

---

### Difference between shape and ndim?

`ndim` returns the number of dimensions (axes).
`shape` returns the size of each dimension.

---

### What does (3, 4) mean?

A 2D array with 3 rows and 4 columns.

---

### What does (5,) mean?

A 1D array with 5 elements.

---

### Why are shapes important in Machine Learning?

Models expect input data in a specific shape. A shape mismatch will cause an error when calling fit() or predict().

---

## Filtering Data

### Why do we filter data?

To select only the rows that satisfy a condition, such as removing outliers or
selecting a specific group for analysis.

---

### Difference between & and |?

`&` means AND — both conditions must be true.
`|` means OR — either condition must be true.

---

### Why do we use parentheses with multiple conditions?

Without parentheses, Python evaluates operator precedence incorrectly and will raise an error or produce wrong results.

---

### How do you filter rows where Marks > 80?

```python
df[df["Marks"] > 80]
```

---

### Where is filtering used in ML?

When removing outliers, selecting subsets for analysis, and cleaning data before model training.

---

## Missing Values

### What is NaN?

Not a Number. It represents a missing or undefined value in a dataset.

---

### Why can't many ML models handle missing values directly?

Most algorithms expect a complete numeric input matrix. Missing values cause errors during training.

---

### Difference between dropna() and fillna()?

`dropna()` removes rows containing missing values.
`fillna()` replaces missing values with a specified value (e.g. the mean).

---

### Why is the mean often used for numeric columns?

It is a simple estimate of the expected value and preserves the overall column distribution.

---

### Would you always use the mean? Why or why not?

No. When a column contains outliers, the median is a better choice because it is
not affected by extreme values the way the mean is.

---

## Feature Engineering

### What is Feature Engineering?

The process of creating, transforming, or selecting features to improve model performance.

---

### Why is it important?

Raw data is often not suitable for Machine Learning. Better features help the model learn more accurate patterns.

---

### Give three examples of Feature Engineering.

1. Creating FamilySize = SibSp + Parch.
2. Creating IsChild = Age < 18.
3. Dropping irrelevant columns such as Ticket or Name.

---

### Why remove unnecessary columns?

Irrelevant features add noise and can reduce model accuracy or slow down training.

---

### Can Feature Engineering improve accuracy?

Yes. Better features often improve model performance more than changing the algorithm itself.

---

## First Machine Learning Model

### What is Scikit-learn?

The most popular Python library for traditional Machine Learning. It provides
ready-to-use implementations of ML algorithms.

---

### Difference between regression and classification?

Regression predicts continuous numbers (e.g. house price).
Classification predicts categories (e.g. spam or not spam).

---

### What are features (X)?

The input variables the model uses to make predictions.

---

### What is the target (y)?

The output variable the model is trained to predict.

---

### What does fit() do?

Trains the model by finding the relationship between X (features) and y (target)
in the training data.

---

## Statistics

### What is statistics?

Statistics is the science of collecting, analyzing, summarizing, and interpreting data.

---

### What is the difference between population and sample?

Population is the complete collection of observations.
Sample is a subset selected from the population.

---

### Why do we use samples instead of populations?

Because collecting the entire population is often expensive, time-consuming, or impossible.

---

### What is descriptive statistics?

Descriptive statistics summarizes the existing data using measures like mean, median, and standard deviation.

---

### What is inferential statistics?

Inferential statistics uses sample data to make conclusions about the entire population.
