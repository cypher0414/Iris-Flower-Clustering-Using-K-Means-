# Iris Flower Clustering Using K-Means (Unsupervised Machine Learning)

This project applies **K-Means clustering**, an **unsupervised learning algorithm**, to the classic **Iris flower dataset**.  
The goal is to group flowers into clusters based solely on their sepal and petal measurements — without using the species labels — and evaluate how well the clusters align with the true species.

---

## Project Overview
- **Type:** Unsupervised Machine Learning  
- **Algorithm:** K-Means Clustering  
- **Dataset:** Iris Dataset (from Kaggle)  
- **Goal:** Identify natural groupings of Iris flowers and compare them to actual species labels.

---

## Objectives
- Load and explore the Iris dataset.  
- Clean and preprocess the data.  
- Scale features for fair distance-based clustering.  
- Determine the optimal number of clusters using the **Elbow Method**.  
- Apply **K-Means clustering** with `k = 3`.  
- Visualize clusters using **PCA (Principal Component Analysis)**.  
- Evaluate and interpret clustering results.

---

## Dataset Information

| Column | Description |
|--------|--------------|
| SepalLengthCm | Length of the sepal in cm |
| SepalWidthCm  | Width of the sepal in cm |
| PetalLengthCm | Length of the petal in cm |
| PetalWidthCm  | Width of the petal in cm |
| Species       | Iris species (Setosa, Versicolor, Virginica) |

- **Total samples:** 150  
- **Classes:** 3 (Iris-setosa, Iris-versicolor, Iris-virginica)  
- **Source:** [Kaggle - Iris Dataset](https://www.kaggle.com/uciml/iris)

---

## Technologies Used
- Python 3  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn  
- Google Colab

---

## Project Workflow

### 1. Load and Explore the Data
Loaded the Iris dataset and verified data integrity (no missing or invalid values).

### 2. Preprocessing
- Removed the unnecessary `Id` column.  
- Scaled numerical features using **StandardScaler** to ensure balanced influence across dimensions.

### 3. Determine Optimal Clusters
- Applied the **Elbow Method** to plot inertia for k = 1–10.  
- Selected **k = 3** as the optimal number of clusters.

### 4. Apply K-Means Clustering
- Trained the **K-Means** algorithm with `k = 3`.  
- Added the predicted cluster labels to the dataset.

### 5. Evaluation
- Calculated **Silhouette Score** to assess cluster separation.  
- Calculated **Adjusted Rand Index (ARI)** to measure agreement with true species labels.

### 6. Visualization
- Used **PCA** to reduce data to two dimensions for visualization.  
- Plotted 2D scatter plots of clusters and true species.  
- Created a **heatmap** showing mean feature values per cluster.

---

## Results Summary

| Metric | Description | Result (Approx.) |
|---------|--------------|------------------|
| Optimal Clusters (k) | Determined using Elbow Method | 3 |
| Silhouette Score | Measures cohesion/separation | ~0.6 |
| Adjusted Rand Index (ARI) | Alignment with true labels | ~0.9 |
| Accuracy (visual match) | Visual cluster accuracy | ~95% |

### Cluster Interpretation

| Cluster | Dominant Species | Characteristics |
|----------|------------------|-----------------|
| 0 | Iris-setosa | Small petals and sepals |
| 1 | Iris-versicolor | Medium-sized features |
| 2 | Iris-virginica | Large petals and sepals |

---

## Key Learnings
- Feature scaling significantly improves K-Means clustering performance.  
- PCA provides effective visualization of high-dimensional clusters.  
- K-Means can accurately uncover structure in unlabeled data.  
- Comparison with true labels validates the quality of unsupervised models.

---



## How to Run

1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/Iris-KMeans-Clustering.git

