# 22. Statistics for Machine Learning

## What is Statistics?

Statistics is the branch of mathematics that helps us collect, summarize, analyze, and interpret data.

In Machine Learning, statistics helps us understand our data before building a model.

Without statistics, we cannot answer questions like:

- What is the average value?
- How spread out is the data?
- Are there any unusual values?
- Are two features related?
- Is the data balanced?

Statistics is one of the core foundations of Machine Learning.

---

# Why Statistics Matters in Machine Learning

Almost every ML project begins with understanding the dataset.

Statistics helps us:

- Summarize large datasets
- Detect outliers
- Understand feature distributions
- Compare variables
- Improve data quality
- Make better modeling decisions

Statistics is used during:

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Model Evaluation

---

# Population vs Sample

## Population

A population is the complete collection of all possible observations we are interested in.

Examples:

- Every house in India
- Every customer of a company
- Every student in a university

In practice, populations are usually too large to collect completely.

---

## Sample

A sample is a smaller subset selected from the population.

Examples:

- 10,000 house listings
- 500 customers
- 200 students

Machine Learning models are almost always trained using samples rather than entire populations.

---

## Why We Use Samples

Collecting an entire population is often:

- Expensive
- Time-consuming
- Sometimes impossible

Instead, we use a representative sample that reflects the population as closely as possible.

A good sample leads to better models.

---

# Descriptive vs Inferential Statistics

## Descriptive Statistics

Descriptive statistics summarizes the available data.

Examples:

- Mean
- Median
- Standard Deviation
- Minimum
- Maximum

Example:

"The average house price is ₹75 Lakhs."

---

## Inferential Statistics

Inferential statistics uses a sample to draw conclusions about the entire population.

Example:

"We estimate the average house price in India based on 10,000 sampled properties."

Machine Learning mostly begins with descriptive statistics, while many advanced ML concepts use inferential statistics.

---

# Key Takeaways

- Statistics helps us understand data before modeling.
- Machine Learning relies heavily on statistical thinking.
- Population represents the complete dataset.
- Sample represents a subset of the population.
- Most ML datasets are samples.
- Descriptive statistics summarizes data.
- Inferential statistics makes conclusions about populations using samples.

---

# Interview Questions

### What is the difference between mean and median?

Mean is the average of all values. Median is the middle value when data is sorted.

---

### When should you use the median instead of the mean?

When the data contains outliers. The median is resistant to extreme values, whereas the mean is sensitive to them.

---

### What does standard deviation measure?

How spread out the values are from the mean. A low standard deviation means values cluster close together.

---

### What is the IQR and why is it used?

The Interquartile Range (Q3 - Q1). Used to measure the spread of the middle 50% of data and to detect outliers.

---

### What is the difference between covariance and correlation?

Covariance measures the direction of the relationship between two variables.
Correlation normalises it to a scale of -1 to 1, measuring both direction and strength.

---

### What does a correlation of 0 mean?

No linear relationship between the two variables.
