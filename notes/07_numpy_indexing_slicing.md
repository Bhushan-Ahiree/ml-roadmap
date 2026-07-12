# NumPy Indexing & Slicing

## What is Indexing?

Indexing is used to access a single element from an array.

Example

```python
arr = np.array([10,20,30,40,50])

arr[0]
```

Output

```
10
```

Negative indexing

```python
arr[-1]
```

Output

```
50
```

---

## What is Slicing?

Slicing is used to access multiple elements.

Syntax

```python
array[start:stop]
```

The stop index is NOT included.

Example

```python
arr[1:4]
```

Output

```
[20 30 40]
```

---

## Omitting Values

Beginning

```python
arr[:3]
```

Output

```
[10 20 30]
```

End

```python
arr[2:]
```

Output

```
[30 40 50]
```

Complete array

```python
arr[:]
```

---

## Step Size

```python
arr[::2]
```

Output

```
[10 30 50]
```

---

## 2D Indexing

```python
matrix[0,1]
```

First row

Second column

---

## 2D Slicing

```python
matrix[:,1]
```

Returns the second column.

---

## Key Takeaways

- Indexing returns one element.
- Slicing returns multiple elements.
- Stop index is excluded.
