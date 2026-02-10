# Lab 2: Machine Learning Problem Definition

## Dataset Description
The dataset used for this lab is the **Mobile Price Classification** dataset (specifically the `submission.csv` feature set). It contains **1,000 mobile device records** with **21 different columns**:
* **Hardware Specs**: Battery power, clock speed, RAM, and internal memory.
* **Connectivity**: 3G, 4G, Bluetooth, and Wifi status.
* **Physical Specs**: Mobile weight, pixel height/width, and screen dimensions.

## Machine Learning Problem
* **Problem Type**: This is a **Classification** problem.
* **Target Variable**: The intended target variable is **`price_range`** (Categorical: 0, 1, 2, or 3).
* **Problem Statement**: The objective is to analyze mobile hardware specifications to predict which of the four price categories a device belongs to[cite: 2368, 2390]. This allows manufacturers to price their products competitively based on technical features.

##  Files Included
1. **`Lab2.ipynb`**: The Jupyter Notebook containing data loading, inspection (`df.info()`), and problem definition.
2. **`submission.csv`**: The raw dataset used for training.
3. **`Methodology DIagram.png`**: A flowchart illustrating the proposed ML pipeline.
