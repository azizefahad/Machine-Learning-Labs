# Lab 11: Credit Card Customer Segmentation
**Unsupervised Learning with K-Means Clustering**
 
[![Problem](https://img.shields.io/badge/Problem-K--Means%20Clustering-blue)](#)
[![Samples](https://img.shields.io/badge/Samples-~8950-green)](#)
[![Features](https://img.shields.io/badge/Features-17-orange)](#)
 
---
 
## Problem Statement
 
The goal of this project is to use **K-Means Clustering** to segment credit card customers based on their usage behavior. This is an unsupervised learning problem because the dataset does not contain a target label. By grouping similar customers together, businesses can better understand different behavioral segments and design targeted marketing strategies.
 
- **Target Variable:** None (Unsupervised Learning)
- **Problem Type:** Clustering / Customer Segmentation
- **Dataset Size:** ~8,950 entries
---
 
## Dataset Features
 
| # | Feature | Description |
|:-:|---------|-------------|
| 1 | `CUST_ID` | Identification of credit card holder (Dropped before modeling) |
| 2 | `BALANCE` | Balance amount left in their account to make purchases |
| 3 | `BALANCE_FREQUENCY` | How frequently the balance is updated (score between 0 and 1) |
| 4 | `PURCHASES` | Amount of purchases made from account |
| 5 | `ONEOFF_PURCHASES` | Maximum purchase amount done in one-go |
| 6 | `INSTALLMENTS_PURCHASES` | Amount of purchase done in installments |
| 7 | `CASH_ADVANCE` | Cash in advance given by the user |
| 8 | `PURCHASES_FREQUENCY` | How frequently the purchases are being made (score between 0 and 1) |
| 9 | `CREDIT_LIMIT` | Limit of credit card for the user |
| 10 | `PAYMENTS` | Amount of payment done by user |
| 11 | `MINIMUM_PAYMENTS` | Minimum amount of payments made by user |
| 12 | `TENURE` | Tenure of credit card service for user |
*(Note: Table shows a representative selection of the 17 behavioral features).*
 
---
 
## Steps Performed
 
1. **Load the Data** — Read `CC_GENERAL.csv` into a DataFrame, inspected the structure, and dropped the non-behavioral `CUST_ID` column.
2. **Handle Missing Data** — Identified missing values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT` and applied mean/median imputation to retain the data without distortion.
3. **Exploratory Data Analysis (EDA)** — Visualized data distributions using histograms, explored feature relationships with scatter plots, and checked variable correlations using a heatmap.
4. **Feature Scaling** — Applied `StandardScaler` to ensure that features with large numerical ranges (like balances) didn't dominate features with small ranges (like frequency scores) in distance calculations.
5. **Determine Optimal Clusters** — Used the **Elbow Method** (tracking inertia) and calculated **Silhouette Scores** across different K values (1 to 10) to find the best number of clusters.
6. **Train K-Means Model** — Initialized and fitted the final `KMeans` algorithm with the optimal number of clusters based on the evaluation metrics.
7. **Cluster Analysis** — Appended the predicted cluster labels back to the DataFrame and used `groupby()` to analyze the mean feature characteristics of each customer segment.
8. **Dimensionality Reduction (PCA)** — Applied Principal Component Analysis (`PCA`) to compress the 17 features down to 2 principal components to visually plot and inspect the clusters in a 2D space.
---
 
## Key Findings
 
| Finding | Detail |
|---------|--------|
| **Unsupervised Approach** | Because there were no "correct answers" or target labels provided, the algorithm successfully discovered hidden behavioral groupings naturally. |
| **Scaling Necessity** | Distance-based algorithms like K-Means require scaling. Standardizing the features was critical to balance currency amounts and decimal frequencies. |
| **Optimal K Value** | The Elbow curve flattened out and Silhouette scores peaked around K=3/K=4, indicating distinct and well-separated customer profiles. |
| **Data Imputation** | Mean/Median imputation effectively resolved the missing data in `MINIMUM_PAYMENTS` (313 values) and `CREDIT_LIMIT` (1 value) without losing hundreds of rows. |
| **PCA Visualization** | Reducing the data to 2 principal components allowed for clear, 2D scatter plot visualization of the multidimensional customer segments. |
 
---
 
## Libraries Used
 
- **Pandas:** For loading the CSV, data manipulation, missing value imputation, and grouping cluster data.
- **NumPy:** For underlying array and numerical operations.
- **Matplotlib:** For plotting the elbow curve, silhouette scores, and feature histograms.
- **Seaborn:** For generating correlation heatmaps and colored scatter plots.
- **Scikit-learn:** For `StandardScaler` (preprocessing), `KMeans` (clustering algorithm), `silhouette_score` (evaluation), and `PCA` (dimensionality reduction).
