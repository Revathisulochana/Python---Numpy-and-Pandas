# 📊 NumPy & Pandas Data Analysis

Hands-on data analysis using **NumPy** for numerical computation and **Pandas** for structured data manipulation, built around temperature and transaction datasets.

> **Python DA Assignment 1 — Data Analytics (DA), Module 5**

---

## 📌 Objective

- Work with NumPy arrays for numerical computations
- Use Pandas Series and DataFrame for data manipulation and analysis
- Apply indexing, slicing, filtering, and aggregation techniques
- Understand real-world data handling through temperature and transaction datasets

---

## 🗂️ Project Structure

```text
numpy-pandas-analysis/
│
├── numpy_pandas_assignment.ipynb   # Notebook with all tasks (or .py script)
└── README.md                       # Project documentation
```

---

## 🧰 Requirements

- Python 3.x
- NumPy
- Pandas
- Jupyter Notebook (optional)

```bash
pip install numpy pandas
```
---

## 📋 Tasks Covered

### Part 1: NumPy Array Operations
**Scenario:** Analyse daily average temperatures (°C) recorded over two weeks.

| # | Task | Details |
|---|------|---------|
| 1 | Create 1D array | `temperatures_w1` = `[22.5, 25.3, 20.8, 23.4, 26.1, 24.8, 21.9]` |
| 2 | Inspect properties | Shape, data type, number of elements |
| 3 | Array operations | Celsius → Fahrenheit using `(C * 9/5) + 32`; max, min, mean |
| 4 | Slicing & indexing | First three days, weekend (last two days), middle three days |
| 5 | Create 2D array | `temperatures` with Week 1 and Week 2 as rows |
| 6 | Inspect & slice 2D | Shape, dtype, size; each week; weekend of both weeks |

### Part 2: Pandas Series
Series `marks` = `95, 92, 89, 85, 80` with index `Rank1` to `Rank5`.

| # | Task | Details |
|---|------|---------|
| 1 | Create Series | Custom index labels |
| 2 | Indexing & slicing | Integer position access, `loc` for top 3 ranks, `iloc` for 3rd rank, boolean mask for marks > 90 |
| 3 | Manipulating Series | Set Rank1 to 100, remove last rank, compute CGPA (marks / 10) |

### Part 3: Pandas DataFrame
DataFrame `transactions` with columns **TransactionID, ProductCategory, Region, Amount** (10 records).

| # | Task | Details |
|---|------|---------|
| 1 | Create DataFrame | 10 transactions (IDs 101 to 110) |
| 2 | Data exploration | `head`, `tail`, `shape`, columns, dtypes; select `ProductCategory` and `Amount`; last 3 columns via `iloc`/`loc`; filter North region with Amount > 200; `value_counts` on category; unique regions; mean amount by region using `groupby` |
| 3 | Manipulating DataFrame | Update Amount for ID 102 to 165; add `Discount` (10% of Amount); drop row with ID 109; delete `Discount` column |

---

## 💡 Key Concepts Demonstrated

- **NumPy:** `np.array`, `.shape`, `.dtype`, `.size`, `.max()`, `.min()`, `.mean()`, slicing, 2D indexing
- **Pandas Series:** custom index, `loc`, `iloc`, boolean masking, element assignment, `drop`, vectorised arithmetic
- **Pandas DataFrame:** `head`, `tail`, `info`, column selection, conditional filtering, `value_counts`, `unique`, `groupby`, adding/dropping columns and rows

---

## 📈 Sample Code Snippets

```python
import numpy as np
import pandas as pd

# NumPy: Celsius to Fahrenheit
temperatures_w1 = np.array([22.5, 25.3, 20.8, 23.4, 26.1, 24.8, 21.9])
fahrenheit = (temperatures_w1 * 9/5) + 32

# Pandas Series: marks above 90
marks = pd.Series([95, 92, 89, 85, 80],
                  index=['Rank1', 'Rank2', 'Rank3', 'Rank4', 'Rank5'])
top_ranks = marks[marks > 90]

# Pandas DataFrame: group by region
# transactions.groupby('Region')['Amount'].mean()
```

---

## 📝 Learning Outcomes

- Perform numerical analysis efficiently with NumPy arrays
- Select data using positional (`iloc`) and label-based (`loc`) indexing
- Filter and aggregate real-world style datasets with Pandas
- Modify, extend, and clean DataFrames and Series

---

## 👤 Author

**Revathi**

---

## 📄 License

This project is created for educational purposes as part of a Data Analytics course assignment.
