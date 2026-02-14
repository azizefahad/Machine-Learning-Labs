<div align="center">

# Lab 2: Machine Learning Problem Definition

**Defining the Mobile Price Classification Problem**

[![Dataset](https://img.shields.io/badge/Dataset-Mobile%20Price%20Classification-red)](https://www.kaggle.com/iabhishekofficial/mobile-price-classification)
[![Problem](https://img.shields.io/badge/Problem-Multiclass%20Classification-blue)](#)
[![Samples](https://img.shields.io/badge/Samples-2000-green)](#)
[![Features](https://img.shields.io/badge/Features-21-orange)](#)

</div>

---

## Machine Learning Problem

**Problem Type:** Classification (Multiclass)

The objective of this project is to analyze mobile hardware specifications to predict which of the four price categories a device belongs to. This allows manufacturers to price their products competitively based on technical features.

- **Target Variable:** `price_range`
- **Classes:** - `0`: Low Cost
  - `1`: Medium Cost
  - `2`: High Cost
  - `3`: Very High Cost

---

## Dataset Description

The dataset (`submission.csv`) contains **2,000 mobile device records** with **21 different columns**. The features are categorized as follows:

| Category | Features Included |
|:---|:---|
| **Hardware Specs** | `battery_power`, `clock_speed`, `ram`, `int_memory`, `n_cores` |
| **Connectivity** | `three_g`, `four_g`, `blue` (Bluetooth), `wifi`, `dual_sim` |
| **Physical Specs** | `mobile_wt`, `px_height`, `px_width`, `sc_h`, `sc_w`, `m_dep` |

---

## Files Included

| File Name | Description |
|:---|:---|
| `Lab2.ipynb` | The Jupyter Notebook containing data loading, inspection, and problem definition. |
| `submission.csv` | The raw dataset used for training and analysis. |
| `Methodology Diagram.png` | A flowchart illustrating the proposed Machine Learning pipeline. |

---

## Libraries Used

- **Pandas:** For loading and inspecting the dataset (`df.info()`).
- **Numpy:** For numerical analysis.
