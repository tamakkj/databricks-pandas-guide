# Databricks & Pandas Data Manipulation Guide

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=Databricks&logoColor=white)](https://databricks.com/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/datasets/nosbielcs/brazilian-delivery-center)

A practical guide showcasing essential data manipulation, cleaning, and transformation workflows using **Pandas** inside the **Databricks** Lakehouse platform.

---

## 📌 Project Overview

This repository demonstrates how to perform end-to-end exploratory data analysis and data preparation techniques on order and store datasets. It covers common data engineering tasks such as handling missing values, type casting, feature engineering, and table merges using Pandas with Databricks Volumes / Unity Catalog integration. The datasets used in this project are based on the **Brazilian Delivery Center** public dataset available on Kaggle:
* **Source:** [Kaggle - Brazilian Delivery Center Dataset](https://www.kaggle.com/datasets/nosbielcs/brazilian-delivery-center)

---

## 🛠️ Key Topics & Code Workflows

The notebook covers the following data processing steps:

1. **Data Ingestion & Inspection**
   * Reading CSV datasets directly from Databricks Volumes (`/Volumes/...`).
   * Initial structure and schema verification using `.columns`, `.head()`, and `.info()`.

2. **Data Cleaning & Preprocessing**
   * Identifying and filtering missing values (`isnull`, `fillna`).
   * Dropping irrelevant columns and removing duplicate records (`drop_duplicates`).
   * Standardizing categorical values using conditional selection (`.loc`).

3. **Data Type Casting & Anomaly Detection**
   * Converting string columns to numerical types (`int`, `float`) via `.astype()`.
   * Analyzing numerical distributions (`.describe()`) and filtering extreme outliers.

4. **Date Handling & Feature Engineering**
   * Parsing timestamp strings into date objects (`pd.to_datetime().dt.date`).
   * Calculating operational metrics (e.g., total product lead time by combining production and collection times).

5. **Aggregation & Table Merges**
   * Joining orders and stores data using `merge` (LEFT JOIN).
   * Grouping and aggregating total sales per store and date (`groupby` + `.agg()`).
   * Exporting a new table with all the processed data back to Databricks Volumes and displaying results.

---

## 📁 Repository Structure

```text
.
├── data/                            # Sample CSV datasets
│   ├── orders.csv
│   └── stores.csv
├── notebooks/                       # Databricks notebooks
│   └── Python_para_eng_de_dados.ipynb
├── .gitignore
└── README.md
