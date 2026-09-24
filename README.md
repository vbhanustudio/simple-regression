# Simple Linear Regression (Salary Prediction)

A professional machine learning project demonstrating a complete Simple Linear Regression pipeline to analyze and predict employee salaries based on years of experience.

---

## 📌 Project Overview

This repository demonstrates an end-to-end Machine Learning pipeline using Python, Pandas, Matplotlib, and NumPy. The goal is to establish a linear relationship between an employee's years of experience and their corresponding salary.

### Key Features
- **Data Preprocessing**: Handling index columns, missing values, and duplicate checks.
- **Exploratory Data Analysis (EDA)**: Data structure inspection and feature visualization using scatter plots.
- **Model Development**: Data splitting, training a Simple Linear Regression model, and performance evaluation.

---

## ⚙️ Machine Learning Pipeline

1. **Data Collection**: Loading raw dataset containing historical experience and salary records.
2. **Data Preparation**:
   - Inspecting dataset structure and data types.
   - Checking for null values and duplicated entries.
   - Dropping redundant/unnecessary index columns.
3. **Data Splitting**: Partitioning data into feature ($X$) and target ($y$) variables, followed by train/test splits.
4. **Model Building**: Fitting a Linear Regression algorithm to the training dataset.
5. **Model Evaluation**: Testing predictions and analyzing accuracy metrics.

---

## 📊 Dataset Summary

The dataset consists of salary records categorized by years of experience.

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `YearsExperience` | Float / Numeric | Total years of professional experience |
| `Salary` | Float / Numeric | Annual salary amount |

### Dataset Characteristics
- **Total Records**: 30 rows
- **Missing Values**: 0
- **Duplicates**: 0

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.x installed along with the required libraries:

```bash
pip install numpy pandas matplotlib scikit-learn
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# 1. Load the dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Clean data
if "Unnamed: 0" in df.columns:
    df.drop(columns=["Unnamed: 0"], inplace=True)

# 3. Visualize data distribution
plt.scatter(df['YearsExperience'], df['Salary'], color='blue', label='Data Points')
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Salary vs Experience")
plt.legend()
plt.show()
# simple-regression# simple-regression
