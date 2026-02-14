<div align="center">

# Lab 3: Exploratory Data Analysis (EDA)

**Applying EDA Techniques to the Mobile Price Classification Dataset**

[![Dataset](https://img.shields.io/badge/Dataset-Mobile%20Price%20Classification-red)](https://www.kaggle.com/iabhishekofficial/mobile-price-classification)
[![Problem](https://img.shields.io/badge/Problem-Multiclass%20Classification-blue)](#)
[![Samples](https://img.shields.io/badge/Samples-2000-green)](#)
[![Features](https://img.shields.io/badge/Features-21-orange)](#)

</div>

---

## Problem Statement

The goal of this lab is to perform **Exploratory Data Analysis (EDA)** to understand the factors that influence the price of mobile phones. 

Before building a machine learning model, we must visualize the relationships between hardware specifications (like RAM, Battery, and Camera) and the device's price range.

- **Target Variable:** `price_range` (0 = Low Cost, 1 = Medium Cost, 2 = High Cost, 3 = Very High Cost)
- **Problem Type:** Classification (Multiclass)
- **Dataset Size:** 2000 entries

---

## Dataset Features

The dataset contains 21 distinct features. Below are the most significant ones:

| # | Feature | Description | Type |
|:-:|---------|-------------|:----:|
| 1 | `ram` | Random Access Memory (Megabytes) | Numeric |
| 2 | `battery_power` | Total energy a battery can store (mAh) | Numeric |
| 3 | `px_height` | Pixel Resolution Height | Numeric |
| 4 | `px_width` | Pixel Resolution Width | Numeric |
| 5 | `mobile_wt` | Weight of mobile phone (grams) | Numeric |
| 6 | `int_memory` | Internal Memory (Gigabytes) | Numeric |
| 7 | `talk_time` | Longest time that a single battery charge will last | Numeric |
| 8 | `n_cores` | Number of processor cores | Categorical |
| 9 | `fc` | Front Camera megapixels | Numeric |
| 10 | `price_range` | **Target Variable** (0, 1, 2, 3) | Categorical |

---

## Steps Performed

### A. Data Integrity Check
We inspected the dataset for errors before analysis:
- **Missing Values:** Checked for null values (None found).
- **Duplicates:** Verified there were no duplicate rows (None found).
- **Data Types:** Confirmed all columns were numerical (int/float), requiring no encoding.

### B. Exploratory Data Analysis (EDA)
We used **Matplotlib** and **Seaborn** to visualize relationships:
1.  **Target Distribution:** Confirmed the dataset is perfectly balanced (500 samples per price class).
2.  **Correlation Matrix:** A heatmap to identify which features correlate most with price.
3.  **Feature Analysis:** Boxplots to visualize how RAM and Battery Power differ across price ranges.

---

## Key Findings

| Finding | Detail |
|---------|--------|
| **Dominant Feature** | **RAM** has the strongest correlation with Price Range (> 0.91). It is the primary predictor. |
| **Class Balance** | The dataset is perfectly balanced with **500** samples for each of the 4 price classes. |
| **Battery Power** | Shows a weak but positive correlation; higher battery capacity generally appears in higher price tiers. |
| **Data Quality** | The dataset is exceptionally clean with **0** missing values and **0** duplicates. |

---

## Libraries Used

- **Pandas:** For data loading and manipulation.
- **Seaborn:** For statistical data visualization (Heatmaps, Boxplots).
- **Matplotlib:** For plotting basic graphs.
- **NumPy:** For numerical operations.
