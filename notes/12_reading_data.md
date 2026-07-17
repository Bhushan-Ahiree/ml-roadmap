# Reading Data with Pandas

## Why?

Machine Learning starts with data.

Most datasets come in formats like:

- CSV
- Excel
- SQL
- JSON

The most common format is CSV.

---

## Read CSV

```python
import pandas as pd

df = pd.read_csv("students.csv")
```

---

## View First Rows

```python
df.head()
```

Default

First 5 rows.

---

## View Last Rows

```python
df.tail()
```

Default

Last 5 rows.

---

## Number of Rows & Columns

```python
df.shape
```

Example

```
(1000,8)
```

Means

1000 rows

8 columns

---

## Column Names

```python
df.columns
```

---

## Data Types

```python
df.dtypes
```

---

## Information

```python
df.info()
```

Shows

- rows
- columns
- missing values
- data types
- memory usage

---

## Summary Statistics

```python
df.describe()
```

Shows statistics for numeric columns.

---

## Key Takeaways

Every ML project starts by loading data and understanding it before building a model.