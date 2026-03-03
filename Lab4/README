# Lab 4: Data Quality Assessment & Preprocessing

## 📱 Project Overview
This lab focuses on the critical second step of the Machine Learning pipeline: **Preprocessing**. In real-world scenarios, data is often incomplete, noisy, or inconsistent. Using a mobile phone price dataset (`submission.csv`), we apply various cleaning and transformation techniques to prepare the data for predictive modeling.



---

## 🛠️ Preprocessing Workflow

### 1. Data Quality Assessment
We performed an initial audit of the 2,000 records to identify structural or logical errors:
* **Data Types**: Verified that all 21 features were correctly identified as numeric (int64 or float64).
* **Logical Consistency**: Identified **180 records** with a screen width (`sc_w`) of 0 and **2 records** with a pixel height (`px_height`) of 0, representing noisy data.

### 2. Handling Missing Values
To demonstrate imputation techniques, we artificially removed data points:
* **Simulation**: 20 random values were removed from the `ram` column.
* **Strategy**: **Median Imputation** was used to fill these gaps.
* **Justification**: The median is the middle value of the ordered data and is more robust than the mean when dealing with skewed distributions or outliers.



### 3. Outlier Detection
Extreme values can significantly distort machine learning models.
* **Method**: Used the **Interquartile Range (IQR)** method on the `px_height` feature.
* **Threshold**: Values outside the range $[Q1 - 1.5 \times IQR, Q3 + 1.5 \times IQR]$ were flagged.
* **Result**: 2 extreme outliers were identified and removed to normalize the feature distribution.



### 4. Data Transformation (Normalization)
To ensure all features contribute equally to the model, we applied two scaling methods:
* **Min-Max Scaling**: Rescaled features (like `ram` and `battery_power`) to a fixed range of $[0, 1]$.
* **Z-Score Normalization**: Transformed data to have a **Mean of 0** and a **Standard Deviation of 1**.

 

### 5. Data Reduction (PCA)
We utilized **Principal Component Analysis** to reduce dimensionality while retaining maximum information:
* **Explained Variance**: The first Principal Component (PC1) alone captured **30.1%** of the total variance in the mobile specifications.
* **Components**: These new uncorrelated components help simplify future model training and reduce computational costs.

---

## 🚀 Key Results
| Metric | Value |
| :--- | :--- |
| **Total Samples** | 2,000 |
| **Outliers Removed** | 2 |
| **Imputation Method** | Median |
| **PC1 Variance** | 30.1% |

---

## 📂 Files Included
* `4- Data Quality Assessment & Preprocessing.ipynb`: The complete Python implementation.
* `submission.csv`: The mobile phone specifications dataset.
* `README.md`: Documentation of the lab workflow.
