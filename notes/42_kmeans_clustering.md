# 42 — K-Means Clustering

## 1. What Is K-Means?

K-Means is an unsupervised clustering algorithm.

Its goal is to divide observations into `K` clusters such that observations within a cluster are relatively close to their cluster center.

The algorithm represents each cluster using a **centroid**.

```text
Data
 ↓
Choose K
 ↓
Initialize centroids
 ↓
Assign observations to nearest centroid
 ↓
Recalculate centroids
 ↓
Repeat
 ↓
Final clusters
```

---

# 2. What Is K?

`K` represents the number of clusters we want.

Example:

```python
KMeans(n_clusters=3)
```

means:

> Create 3 clusters.

K-Means does not automatically know the correct number of clusters.

Choosing `K` is part of the modeling process.

---

# 3. What Is a Centroid?

A centroid is the mean position of the observations belonging to a cluster.

For a two-dimensional cluster:

```text
(x₁, y₁)
(x₂, y₂)
(x₃, y₃)
```

the centroid is:

```text
x̄ = (x₁ + x₂ + x₃) / 3

ȳ = (y₁ + y₂ + y₃) / 3
```

So the centroid represents the center of the cluster.

---

# 4. How K-Means Works

K-Means repeatedly performs two main operations.

## Step 1 — Initialize Centroids

Choose `K` initial centroids.

Modern scikit-learn uses `k-means++` by default, which provides a smarter initialization than simply choosing random points.

---

## Step 2 — Assign Points

Each observation is assigned to the nearest centroid.

Conceptually:

```text
Point
 ↓
Calculate distance to each centroid
 ↓
Choose nearest centroid
```

---

## Step 3 — Recalculate Centroids

After assigning observations to clusters, calculate the mean of each cluster.

These means become the new centroids.

---

## Step 4 — Repeat

The assignment and centroid-update steps continue until the algorithm converges or reaches the iteration limit.

---

# 5. K-Means Objective

K-Means attempts to minimize the total squared distance between observations and their assigned cluster centroids.

This quantity is called **inertia**.

Conceptually:

```text
Inertia
=
sum of squared distances
between each observation
and its assigned centroid
```

Lower inertia means observations are closer to their assigned centroids.

However:

> Lower inertia alone does not mean a better clustering solution.

Increasing `K` normally reduces inertia.

---

# 6. Important Parameters

A typical model:

```python
from sklearn.cluster import KMeans

model = KMeans(
    n_clusters=3,
    random_state=42,
    n_init="auto"
)
```

## `n_clusters`

Number of clusters.

```python
n_clusters=3
```

---

## `random_state`

Controls randomness so results can be reproduced.

```python
random_state=42
```

---

## `n_init`

Controls how many initial centroid configurations are tried.

K-Means can produce different results depending on initialization.

Multiple initializations reduce the chance of ending with a poor local solution.

Current scikit-learn supports `n_init="auto"`. With the default `k-means++` initialization, this currently means one run; explicit multiple initializations can also be specified when desired.

For learning and reproducibility, explicitly understanding `n_init` is more important than memorizing the default.

---

## `max_iter`

Maximum number of iterations for one run.

```python
max_iter=300
```

Usually the default is sufficient unless convergence is problematic.

---

# 7. Why Scaling Matters

K-Means is distance-based.

Suppose features have very different scales:

```text
Age       → 18–80
Income    → 20,000–500,000
```

Income can dominate the distance calculation.

Therefore, scaling is commonly applied before K-Means.

A standard approach is:

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_scaled = scaler.fit_transform(X)
```

The Wine dataset is a good example because its numeric features have different scales. Scikit-learn specifically demonstrates the importance of feature scaling on this dataset.

---

# 8. Why We Must Not Use the Target

The Wine dataset contains a known classification target.

For this clustering experiment:

```python
X = wine.data
```

We intentionally do not use:

```python
y = wine.target
```

The clustering algorithm must discover structure from the features alone.

The target can later be used for analysis, but it must not be used to train the unsupervised model.

---

# 9. Choosing K — Elbow Method

We can train K-Means for several values of `K`.

Example:

```text
K = 2
K = 3
K = 4
K = 5
...
```

For each value, calculate inertia.

Then plot:

```text
K → inertia
```

Typically inertia decreases as `K` increases.

We look for an **elbow**, where increasing `K` further gives diminishing improvement.

The elbow is a heuristic, not a mathematical guarantee of the correct number of clusters.

---

# 10. Choosing K — Silhouette Score

The silhouette score measures how well observations fit their assigned cluster compared with neighboring clusters.

Range:

```text
-1 to +1
```

Interpretation:

```text
near +1 → strong separation
near 0  → overlapping/boundary observations
negative → potentially poor assignment
```

Scikit-learn uses silhouette analysis as one approach for investigating the choice of `n_clusters`.

A higher average silhouette score generally indicates better-separated clusters, but domain interpretation is still required.

---

# 11. Elbow vs Silhouette

They answer slightly different questions.

### Elbow

Looks at:

```text
How much does increasing K reduce inertia?
```

### Silhouette

Looks at:

```text
How well separated are the resulting clusters?
```

Use both rather than blindly selecting the value with the lowest inertia.

---

# 12. Cluster Labels

After fitting:

```python
labels = model.labels_
```

we obtain a cluster label for every observation.

Example:

```text
0
2
1
0
0
2
...
```

These numbers are identifiers.

They do not mean:

```text
0 = bad
1 = average
2 = good
```

unless we explicitly interpret the cluster characteristics that way.

---

# 13. Cluster Centers

K-Means stores the learned centroids:

```python
model.cluster_centers_
```

The shape is:

```text
(number_of_clusters, number_of_features)
```

For:

```text
K = 3
13 features
```

the shape is:

```text
(3, 13)
```

Each row represents one cluster centroid.

---

# 14. Important Limitation of K-Means

K-Means works best when clusters can reasonably be represented by their centers.

It can perform poorly when clusters have:

* highly irregular shapes
* very different densities
* extreme outliers
* complex structures

Other algorithms may be more appropriate in those situations.

Examples:

* DBSCAN
* Hierarchical clustering
* Gaussian Mixture Models

Therefore:

> K-Means is useful, but it is not a universal clustering algorithm.

---

# 15. Practical K-Means Workflow

```text
Understand problem
       ↓
Select features
       ↓
Clean data
       ↓
Scale features when appropriate
       ↓
Try reasonable K values
       ↓
Fit K-Means
       ↓
Evaluate inertia
       ↓
Evaluate silhouette score
       ↓
Inspect cluster sizes
       ↓
Profile cluster characteristics
       ↓
Validate usefulness
```

---

# 16. Key Takeaways

* K-Means is an unsupervised clustering algorithm.
* `K` is the number of clusters.
* A centroid represents the center of a cluster.
* K-Means alternates between assignment and centroid updates.
* Inertia measures within-cluster squared distances.
* Scaling matters because K-Means uses distances.
* `n_init` helps reduce sensitivity to initialization.
* The elbow method can help investigate `K`.
* Silhouette score helps evaluate cluster separation.
* Cluster labels are identifiers, not inherent meanings.
* Lower inertia alone does not prove a better model.
* K-Means has important limitations.
