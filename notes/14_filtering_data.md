# Filtering Data with Pandas

## Why Filter Data?

Filtering helps us select only the rows that satisfy a condition.

Examples:

- Students with marks above 80
- Houses costing less than ₹50 lakh
- Employees with salary > ₹1,00,000

---

## Single Condition

```python
df[df["Marks"] > 80]
```

Returns all students with marks greater than 80.

---

## Less Than

```python
df[df["Age"] < 22]
```

---

## Equal To

```python
df[df["City"] == "Pune"]
```

---

## Multiple Conditions (AND)

```python
df[(df["Marks"] > 80) & (df["City"] == "Pune")]
```

---

## Multiple Conditions (OR)

```python
df[(df["Marks"] > 80) | (df["City"] == "Mumbai")]
```

---

## Key Takeaways

- > Greater than
- < Less than
- == Equal to
- & AND
- | OR