# Selecting Data with Pandas

## Selecting a Column

```python
df["Age"]
```

Returns a Series.

---

## Selecting Multiple Columns

```python
df[["Name", "Age"]]
```

Returns a DataFrame.

---

## Selecting Rows using loc

```python
df.loc[0]
```

Returns the first row using its label.

---

## Selecting Rows using iloc

```python
df.iloc[0]
```

Returns the first row using its position.

---

## Selecting Specific Rows

```python
df.iloc[1:4]
```

Returns rows 1 to 3.

---

## Selecting Specific Rows and Columns

```python
df.iloc[0:3,1:3]
```

Rows 0–2

Columns 1–2

---

⭐ Gold Insight (Very Important)

This line appears in almost every ML project:

X = df.drop("Price", axis=1)
y = df["Price"]

Why?

X = Features (all input columns)
y = Target (the column we want to predict)

---

## Key Takeaways

- Single column → Series
- Multiple columns → DataFrame
- loc → Label based
- iloc → Position based