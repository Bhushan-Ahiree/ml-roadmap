# 41 — Unsupervised Learning

## 1. What Is Unsupervised Learning?

Unsupervised learning is a type of machine learning where the model receives input features but does not receive a target variable that tells it the correct answer.

### Supervised Learning

```text
X → model → y
```

The model learns from known target values.

Examples:

* Linear Regression
* Logistic Regression
* Decision Trees
* Random Forest
* SVM
* KNN

### Unsupervised Learning

```text
X → model → discovered structure
```

There is no target `y` used during learning.

The algorithm attempts to discover useful patterns or structure in the data.

---

# 2. Why Use Unsupervised Learning?

Real-world datasets often do not have labeled outcomes.

For example, a company may have thousands of customers with:

* age
* income
* purchase frequency
* total spending
* website activity

But there may be no predefined customer segment.

Unsupervised learning can help discover groups of customers with similar characteristics.

Common applications:

* Customer segmentation
* Market segmentation
* Property segmentation
* Document grouping
* Image analysis
* Anomaly detection
* Data exploration
* Feature representation

---

# 3. Main Areas of Unsupervised Learning

The most important areas for an ML engineer are:

## 3.1 Clustering

Groups similar observations together.

Important algorithms:

* K-Means
* Hierarchical/Agglomerative Clustering
* DBSCAN

## 3.2 Dimensionality Reduction

Reduces the number of features while attempting to preserve useful information.

Important technique:

* PCA

## 3.3 Distribution-Based Methods

Model the underlying distribution of observations.

Example:

* Gaussian Mixture Models

We do not need to learn every unsupervised algorithm.

The goal is to understand the important concepts and know when each major approach is useful.

---

# 4. Clustering

Clustering attempts to divide observations into groups called **clusters**.

Observations inside a cluster should generally be more similar to each other than to observations in other clusters.

For example:

```text
Customer data
      ↓
Clustering algorithm
      ↓
Cluster 0
Cluster 1
Cluster 2
```

The algorithm discovers the groups instead of being given the group labels beforehand.

---

# 5. Classification vs Clustering

These two concepts are easy to confuse.

## Classification

The classes already exist in the training data.

```text
Features → known class
```

Example:

```text
email features → spam
email features → not spam
```

The model learns to predict an existing class.

## Clustering

The groups are not provided.

```text
Features → discovered groups
```

Example:

```text
customer data → cluster 0
              → cluster 1
              → cluster 2
```

The cluster numbers do not automatically have business meanings.

---

# 6. Important Point: Cluster Labels Have No Inherent Meaning

Suppose an algorithm produces:

```text
Cluster 0
Cluster 1
Cluster 2
```

This does **not** mean:

```text
Cluster 0 = low-value customers
Cluster 1 = medium-value customers
Cluster 2 = high-value customers
```

The numbers are simply identifiers.

After clustering, we must inspect the characteristics of each group and determine whether they have useful meaning.

---

# 7. There Is No Target Variable

In supervised learning we normally have:

```python
X = features
y = target
```

In unsupervised learning:

```python
X = features
```

There is no target used to train the algorithm.

For example:

```python
X = df.drop(columns="target")
```

Even if the original dataset contains labels, an unsupervised experiment can intentionally ignore them.

This allows us to investigate whether meaningful structure can be discovered without using the known labels.

---

# 8. Similarity and Distance

Many clustering algorithms determine similarity using distance.

A common distance measure is Euclidean distance.

For two points:

```text
A = (x₁, y₁)
B = (x₂, y₂)
```

their Euclidean distance is:

```text
distance = √((x₂ - x₁)² + (y₂ - y₁)²)
```

Smaller distance generally means the observations are more similar under that representation.

The exact notion of similarity depends on the algorithm and feature representation.

---

# 9. Why Feature Scaling Matters

Suppose a dataset contains:

```text
Age       → 18 to 80
Income    → 20,000 to 500,000
```

Income has a much larger numerical scale.

For a distance-based algorithm, this can cause income to have a much larger influence on calculated distances.

Therefore, features may need to be scaled before clustering.

Common scaling techniques include:

* Standardization
* Min-Max scaling

For example:

```text
StandardScaler
```

The correct preprocessing depends on the algorithm and dataset.

---

# 10. Evaluation Is Different

Supervised learning usually has a known target, allowing metrics such as:

* MAE
* RMSE
* R²
* Accuracy
* Precision
* Recall
* F1

Unsupervised learning does not normally have a target to compare against.

Therefore, evaluation requires different approaches.

For clustering, useful measures include:

* Inertia
* Silhouette score
* Cluster stability
* Cluster separation
* Domain/business interpretation

No single metric automatically proves that a clustering solution is correct.

---

# 11. Inertia

Inertia is particularly important for K-Means.

It measures the sum of squared distances between observations and their assigned cluster centers.

Lower inertia means observations are, on average, closer to their assigned centroids.

However:

> Lower inertia by itself does not mean the clustering is better.

Increasing the number of clusters will generally reduce inertia.

Therefore, inertia is often examined across multiple values of `K`, rather than interpreted as a standalone score.

---

# 12. Silhouette Score

The silhouette score evaluates how well an observation fits within its assigned cluster compared with neighboring clusters.

Conceptually:

```text
high score
    ↓
well separated / appropriately grouped

low score
    ↓
observation may be close to another cluster
```

The score ranges approximately from:

```text
-1 to +1
```

Higher values generally indicate better-defined clustering structure.

However, the score should still be interpreted together with the problem and domain context.

---

# 13. Choosing the Number of Clusters

Some clustering algorithms require us to specify the number of clusters.

K-Means is one example.

```python
KMeans(n_clusters=3)
```

The difficult question is:

> Why 3?

Possible approaches include:

* Elbow method
* Silhouette score
* Domain knowledge
* Cluster stability
* Business usefulness

There is not always one objectively correct value of `K`.

---

# 14. Do Not Over-Interpret Clusters

This is one of the most important concepts in unsupervised learning.

A clustering algorithm finds mathematical structure in the representation we provide.

It does not automatically discover a true real-world classification.

For example:

```text
Algorithm → 3 clusters
```

does not prove:

```text
The business has exactly 3 customer types.
```

The result depends on:

* Selected features
* Feature scaling
* Distance measure
* Algorithm
* Hyperparameters
* Number of clusters
* Data quality
* Outliers

Therefore, clustering results require interpretation and validation.

---

# 15. Practical Unsupervised Learning Workflow

A practical workflow is:

```text
1. Define the problem
       ↓
2. Understand the data
       ↓
3. Select useful features
       ↓
4. Clean the data
       ↓
5. Handle missing values
       ↓
6. Transform / scale features when appropriate
       ↓
7. Apply an unsupervised algorithm
       ↓
8. Evaluate the discovered structure
       ↓
9. Profile the clusters
       ↓
10. Validate business usefulness
```

The algorithm is only one part of the workflow.

---

# 16. Important Algorithms to Know

## K-Means

Useful for:

* General-purpose clustering
* Large datasets
* Relatively compact clusters

Requires:

```text
number of clusters K
```

We will study this in detail next.

## Hierarchical / Agglomerative Clustering

Builds a hierarchy of clusters.

Useful when we want to examine relationships between groups at different levels.

## DBSCAN

Density-based clustering.

Useful when:

* Cluster shapes are irregular
* Noise/outliers matter
* We do not want to specify the number of clusters beforehand

## PCA

Not a clustering algorithm.

PCA is a dimensionality-reduction technique.

It is useful for:

* Reducing feature dimensions
* Visualization
* Compressing information
* Handling highly correlated features in some workflows

---

# 17. What We Need to Remember

### Core concepts

* Unsupervised learning does not require a target variable.
* Clustering discovers groups.
* Classification predicts known classes.
* Cluster labels have no inherent meaning.
* Feature scaling can strongly affect distance-based algorithms.
* Unsupervised models can still be evaluated.
* Inertia and silhouette score are useful clustering measures.
* The number of clusters may require experimentation.
* Domain knowledge is important when interpreting clusters.
* A clustering result is not automatically a real-world truth.

---

# 18. Next Topic

The next notebook is:

```text
42_kmeans_clustering.ipynb
```

It will cover K-Means practically using a real dataset.

Topics:

* K-Means intuition
* Centroids
* Distance
* Assignment
* Centroid update
* `n_clusters`
* `random_state`
* `n_init`
* Inertia
* Elbow method
* Silhouette score
* Feature scaling
* Cluster interpretation
* Practical limitations
