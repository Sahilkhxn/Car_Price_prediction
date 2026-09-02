# 🚗 Car Price Analysis - Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a car price dataset using Python.

The main objective of this project is to analyze different factors related to car prices, such as:

* Car Brand
* Fuel Type
* Price
* Minimum and Maximum Price
* Average Car Price
* Distribution of Cars
* Correlation between numerical features

---

## 🎯 Objectives

The main objectives of this project are:

* Understand the structure of the dataset
* Check for missing values
* Check for duplicate records
* Analyze different car brands
* Analyze different fuel types
* Compare car prices based on fuel type
* Compare average car prices based on brand
* Find minimum and maximum car prices
* Identify relationships between numerical features using correlation analysis

---

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## 📊 Analysis Performed

### 1. Data Exploration

The dataset was explored using:

```python
df.head()
df.info()
df.describe()
```

This helps in understanding:

* Dataset structure
* Column names
* Data types
* Statistical summary

---

### 2. Missing Values Analysis

Missing values were checked to identify incomplete data.

```python
df.isnull().sum()
```

---

### 3. Duplicate Values Analysis

Duplicate records were checked using:

```python
df.duplicated().sum()
```

---

### 4. Fuel Type Analysis

Car prices were analyzed based on different fuel types.

The following metrics were calculated:

* Number of Cars
* Average Price
* Minimum Price
* Maximum Price

```python
df.groupby("Fuel Type")["Price"].agg(
    ["count", "mean", "min", "max"]
)
```

---

### 5. Brand-wise Price Analysis

Car prices were also analyzed according to different brands.

```python
df.groupby("Brand")["Price"].agg(
    ["count", "mean", "min", "max"]
).sort_values(by="mean", ascending=False)
```

This analysis helps identify brands with higher and lower average car prices.

---

### 6. Correlation Analysis

A correlation matrix was created to understand the relationship between numerical variables.

```python
df.corr(numeric_only=True)
```

A heatmap was also used for better visualization of correlations.

---

## 📈 Key Insights

The analysis can help answer questions such as:

* Which fuel type has the highest average price?
* Which fuel type has the lowest average price?
* Which brand has the highest average car price?
* Which brand has the most cars in the dataset?
* What are the minimum and maximum car prices?
* Which numerical features are most related to car price?

---

## 📂 Project Structure

```text
Car-Price-Analysis/
│
├── Car_Price_Analysis.ipynb
├── README.md
└── dataset.csv
```

---

## 🚀 How to Run the Project

1. Clone the repository.

```bash
git clone <repository-url>
```

2. Open the project folder.

3. Install the required libraries.

```bash
pip install pandas numpy matplotlib seaborn
```

4. Open the Jupyter Notebook.

```bash
jupyter notebook
```

5. Run the notebook cells.

---

## 👨‍💻 Author
**Sahil Khan**

---

## ⭐ Conclusion

This project demonstrates the use of Python and data analysis libraries to perform Exploratory Data Analysis on a car price dataset.

The analysis provides insights into how factors such as **Brand** and **Fuel Type** are associated with car prices.
