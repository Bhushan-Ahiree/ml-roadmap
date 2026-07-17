# NumPy Vectorization

## What is Vectorization?

Vectorization means performing operations on an entire array without writing loops.

Instead of processing one element at a time, NumPy processes the whole array efficiently.

---

## Python Example

```python
numbers = [1,2,3,4]

result = []

for num in numbers:
    result.append(num*2)
```

---

## NumPy Example

```python
arr = np.array([1,2,3,4])

result = arr * 2
```

No loop required.

---

## Common Operations

Addition

```python
arr + 10
```

Multiplication

```python
arr * 2
```

Division

```python
arr / 2
```

Power

```python
arr ** 2
```

---

## Advantages

- Faster
- Cleaner
- Less code
- Optimized in C

---

## Key Takeaways

Vectorization replaces loops with array operations.