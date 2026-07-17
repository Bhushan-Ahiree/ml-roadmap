# NumPy Reshape

## What is Reshape?

Reshape changes the shape of an array without changing its data.

Example

```python
arr = np.array([1,2,3,4,5,6])

arr.reshape(2,3)
```

Output

```
[[1 2 3]
 [4 5 6]]
```

---

## Another Example

```python
arr.reshape(3,2)
```

Output

```
[[1 2]
 [3 4]
 [5 6]]
```

---

## Important Rule

The total number of elements must remain the same.

Example

```
6 elements

(2,3)

2 × 3 = 6 ✅

(3,2)

3 × 2 = 6 ✅

(4,2)

4 × 2 = 8 ❌
```

---

## Automatic Dimension

Use -1 when NumPy should calculate one dimension.

```python
arr.reshape(2,-1)
```

Output

```
[[1 2 3]
 [4 5 6]]
```

NumPy automatically computes the missing dimension.

---

## Flatten

Convert a multi-dimensional array into a 1D array.

```python
matrix.flatten()
```

---

## Key Takeaways

- reshape() changes shape only.
- Total elements must remain the same.
- -1 lets NumPy infer one dimension.
- flatten() converts arrays back to 1D.