# Missing Values

## What are Missing Values?

Missing values are cells that contain no data.

Example

| Name | Age |
|------|----|
| John | 22 |
| Alice | NaN |
| Bob | 25 |

NaN = Not a Number (missing value)

---

## Why are Missing Values Important?

Most ML models cannot train with missing values.

We must either:

- Remove them
- Fill them

---

## Check Missing Values

```python
df.isnull()
```

Returns True where data is missing.

---

## Count Missing Values

```python
df.isnull().sum()
```

---

## Remove Missing Values

```python
df.dropna()
```

---

## Fill Missing Values

```python
df.fillna(value)
```

Example

```python
df["Age"].fillna(df["Age"].mean())
```

---

## Key Takeaways

- Check missing values first.
- Don't blindly delete rows.
- Choose an appropriate filling strategy.