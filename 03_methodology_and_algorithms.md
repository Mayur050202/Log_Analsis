# Chapter 3: Methodology & Algorithmic Deep Dive

## 3.1 Architectural Pipeline Structure
The execution layout flows linearly across four custom in-memory memory phases to minimize processing latency layers:
1. **In-Memory Buffer Ingestion:** Flat log rows are mapped directly into streaming Pandas vector matrices inside volatile RAM.
2. **Structural Regular Expression Tokenizer:** Multi-pass string transformations strip away timestamps, process block IDs, hex nonces, and variable numeric sequences to reveal stable underlying template skeletons.
3. **High-Dimensional Text Vectorization:** Implements Term Frequency-Inverse Document Frequency (TF-IDF) feature matrix extraction bounded strictly at 100 maximum spatial layout features.
4. **Unsupervised Metric Partitioning Core:** Groups standard text templates via K-Means centroid clustering.

## 3.2 Core Algorithmic Formulations
### Term Frequency-Inverse Document Frequency (TF-IDF)
The textual character strings are transformed into numerical vector arrays using the standard TF-IDF scaling model:
$$TF-IDF(t, d, D) = TF(t, d) 	imes \log\left(\frac{1 + |D|}{1 + |\{d \in D : t \in d\}|}\right) + 1$$

### K-Means Centroid Minimization
The unsupervised mathematical clustering engine optimizes the spatial positioning of behavior centers by minimizing the standard Within-Cluster Sum of Squares (WCSS):
$$\text{ArgMin}_{S} \sum_{i=1}^{k} \sum_{x_p \in S_i} \Vert{}x_p - \mu_i\Vert{}^2$$

### Euclidean Distance Isolation Math
Spatial outlier evaluation metrics isolate anomalies by processing the straight-line coordinate distance of every input row relative to the nearest baseline behavior center:
$$\text{Distance}(x_p, \mu_i) = \sqrt{\sum_{j=1}^{n} (x_{p,j} - \mu_{i,j})^2}$$
A dynamic cutoff boundary is established at the strict **99.9th percentile**. Any vector index displaying a distance larger than this cutoff limit is automatically flagged as a system exploit.
