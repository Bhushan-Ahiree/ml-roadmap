# GroupBy in Pandas

## What is GroupBy?

GroupBy groups rows that have the same value in a column and performs calculations on each group.

Think of it as:

Split → Apply → Combine

---

## Syntax

```python
df.groupby("Column")
```

---

## Example

Average salary by department

| Department | Salary |
|------------|---------|
| HR | 40000 |
| IT | 60000 |
| HR | 45000 |
| IT | 70000 |

```python
df.groupby("Department")["Salary"].mean()
```

Output

```
HR    42500
IT    65000
```

---

## Count

```python
df.groupby("Department").size()
```

---

## Maximum

```python
df.groupby("Department")["Salary"].max()
```

---

## Multiple Aggregations

```python
df.groupby("Department")["Salary"].agg(["mean","max","min"])
```

---

## Key Takeaways

- Group similar rows
- Perform calculations
- Used heavily during EDA