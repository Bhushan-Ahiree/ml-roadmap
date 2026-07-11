# NumPy Shapes & Dimensions

## Dimension

Dimension tells us how many axes an array has.

Examples

0D → Single Number

5

1D → One Axis

[10,20,30]

2D → Rows and Columns

[
 [1,2,3],
 [4,5,6]
]

3D → Multiple Tables

[
 [
  [1,2],
  [3,4]
 ],

 [
  [5,6],
  [7,8]
 ]
]

---

## Shape

Shape tells us the size of every dimension.

Examples

[10,20,30]

Shape

(3,)

Three elements.

---

[
 [1,2,3],
 [4,5,6]
]

Shape

(2,3)

2 rows

3 columns

---

## ndim

Returns the number of dimensions.

```python
arr.ndim
```

---

## shape

Returns the size of each dimension.

```python
arr.shape
```

---

## size

Returns total elements.

```python
arr.size
```

---

## dtype

Returns the data type.

```python
arr.dtype
```

---

## Key Takeaways

Dimension → Number of axes

Shape → Size of each axis

Size → Total elements

dtype → Data type