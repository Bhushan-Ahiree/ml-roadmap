# Feature Engineering

## What is Feature Engineering?

Feature Engineering is the process of creating, transforming, or selecting features (columns) to improve model performance.

Good features → Better model.

---

## Why is it Important?

Raw data is often not suitable for machine learning.

We need to prepare it before training.

---

## Common Feature Engineering Tasks

- Create new features
- Encode categorical data
- Handle missing values
- Scale numerical data
- Select useful features

---

## Creating a New Feature

Example

Age

22

35

18

Create

Adult

True

True

False

---

Example

```python
df["FamilySize"] = df["SibSp"] + df["Parch"]
```

---

## Dropping Unnecessary Columns

```python
df.drop(columns=["Ticket"])
```

---

## Renaming Columns

```python
df.rename(columns={"Sex":"Gender"})
```

---

⭐ Gold Insight (Industry)

Feature engineering is where business understanding meets machine learning.

Example:

In real estate, instead of just using:

Area

You might create:

Price per square foot
Property age
Distance to city center

These new features often help the model learn better patterns.

---

## Key Takeaways

- Better features usually improve models.
- Not every column should be used.
- Domain knowledge helps create useful features.