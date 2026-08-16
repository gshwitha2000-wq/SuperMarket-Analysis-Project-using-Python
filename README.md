# 🛒 SuperMarket Sales Analysis

## 📌 Project Overview

This project performs an exploratory data analysis (EDA) on supermarket sales data using **Python, Pandas, NumPy, and Matplotlib**.

The objective is to analyze supermarket transactions and identify useful patterns related to:

* Customer demographics
* Customer types
* Product categories
* Sales performance
* Payment methods
* Gender-wise sales
* Customer ratings
* Branch and city distribution

The analysis is performed using a dataset containing **1,000 transactions and 17 columns**.

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand the structure of the supermarket sales dataset.
2. Perform data quality checks.
3. Analyze customer demographics.
4. Analyze sales across different product lines.
5. Identify popular payment methods.
6. Compare sales by gender.
7. Analyze customer ratings.
8. Visualize important business insights using charts.

---

## 📊 Dataset

The dataset contains **1,000 records and 17 attributes**.

### Dataset Columns

| Column                  | Description                            |
| ----------------------- | -------------------------------------- |
| Invoice ID              | Unique identifier for each transaction |
| Branch                  | Supermarket branch                     |
| City                    | City where the branch is located       |
| Customer type           | Member or Normal customer              |
| Gender                  | Customer gender                        |
| Product line            | Category of purchased products         |
| Unit price              | Price of one unit                      |
| Quantity                | Number of units purchased              |
| Tax 5%                  | 5% tax applied to the transaction      |
| Sales                   | Total transaction value including tax  |
| Date                    | Transaction date                       |
| Time                    | Transaction time                       |
| Payment                 | Payment method                         |
| COGS                    | Cost of goods sold                     |
| Gross margin percentage | Gross margin percentage                |
| Gross income            | Income generated from the transaction  |
| Rating                  | Customer rating                        |

The notebook confirms that all 17 columns contain 1,000 non-null values.

---

## 🧹 Data Cleaning & Quality Checks

The following data quality checks were performed:

### Missing Values

The project checks for missing values using:

```python
data.isnull().sum()
```

All columns returned **0 missing values**.

### Duplicate Records

Duplicate records were checked using:

```python
data.duplicated().sum()
```

The result was **0**, indicating that no duplicate rows were found.

### Descriptive Statistics

The project uses:

```python
data.describe()
```

to examine statistical measures such as:

* Mean
* Standard deviation
* Minimum
* Maximum
* Quartiles

For example, the average quantity per transaction is **5.51**, while the average sales value is approximately **322.97**.

---

## 🔍 Exploratory Data Analysis

### 1. Branch Analysis

The dataset contains three branches:

* Alex
* Giza
* Cairo

This was identified using:

```python
data.Branch.unique()
```

---

### 2. Product Line Analysis

The supermarket sells products across six product lines:

* Health and beauty
* Electronic accessories
* Home and lifestyle
* Sports and travel
* Food and beverages
* Fashion accessories

The project calculates total sales for each product line.

| Product Line           | Total Sales |
| ---------------------- | ----------: |
| Food and beverages     |   53,471.28 |
| Sports and travel      |   52,497.93 |
| Electronic accessories |   51,750.03 |
| Fashion accessories    |   51,719.90 |
| Home and lifestyle     |   51,297.06 |
| Health and beauty      |   46,851.18 |

Food and beverages generated the highest calculated sales in this analysis, while health and beauty generated the lowest.

A bar chart was also created to visualize product-wise sales.

---

### 3. Customer Type Analysis

Customers were divided into two categories:

* **Member:** 565
* **Normal:** 435

This shows that the dataset contains more member transactions than normal customer transactions.

---

### 4. Gender Analysis

The dataset contains:

* **Female:** 571 transactions
* **Male:** 429 transactions

The project also calculates total sales by gender:

| Gender |      Sales |
| ------ | ---------: |
| Female | 185,401.75 |
| Male   | 122,185.63 |

Female customers contributed higher total sales in this dataset.

---

### 5. Payment Method Analysis

Three payment methods are present:

| Payment Method | Transactions |
| -------------- | -----------: |
| E-wallet       |          345 |
| Cash           |          344 |
| Credit card    |          311 |

E-wallet was the most frequently used payment method, followed very closely by cash.

A pie chart was created to visualize the distribution of payment methods.

---

### 6. Customer Rating Analysis

Customer ratings range from **4.0 to 10.0**, with an average rating of approximately **6.97**.

The notebook also filters transactions where:

```python
data[data.Rating > 8]
```

to analyze highly rated transactions.

---

## 💰 Sales Calculation

The project creates a new `total` column using:

```python
data['total'] = data['Unit price'] * data['Quantity']
```

The calculated total before the 5% tax component is:

**307,587.38**

> **Note:** The notebook's `total` calculation is different from the existing `Sales` column, because `Sales` includes the 5% tax.

---

## 📈 Visualizations

The project uses **Matplotlib** to create visualizations such as:

* Product-wise sales bar chart
* Payment method pie chart
* Additional exploratory visualizations

## These visualizations make it easier to understand sales patterns and customer behavior.

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data loading, cleaning, filtering and aggregation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Jupyter Notebook** – Interactive analysis environment

The notebook imports Pandas, NumPy and Matplotlib and loads the supermarket CSV using `pd.read_csv()`.

---

## 📂 Project Structure

```text
SuperMarket-Analysis/
│
├── SuperMarket Analysis Project.ipynb
├── SuperMarket Analysis.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the project directory

```bash
cd SuperMarket-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

Open:

```text
SuperMarket Analysis Project.ipynb
```

Make sure the CSV file is present in the same directory as the notebook because the notebook loads it using:

```python
pd.read_csv('SuperMarket Analysis.csv')
```

---

## 💡 Key Insights

Based on the analysis performed in the notebook:

* The dataset contains **1,000 supermarket transactions**.
* There are **3 branches** and **6 product lines**.
* No missing values were identified.
* No duplicate records were identified.
* **565 transactions** were from members compared with **435 normal customer transactions**.
* Female customers accounted for **571 transactions** and generated higher calculated sales than male customers.
* **E-wallet** was the most frequently used payment method.
* **Food and beverages** had the highest calculated product-line sales.
* The average customer rating was approximately **6.97**.
* The calculated transaction total before tax was **307,587.38**.

---

## 📌 Skills Demonstrated

This project demonstrates practical skills in:

* Data loading
* Data exploration
* Data cleaning
* Missing-value analysis
* Duplicate detection
* Descriptive statistics
* Data filtering
* GroupBy aggregation
* Sales analysis
* Customer segmentation
* Exploratory Data Analysis
* Data visualization
* Business insight generation

---

## 👩‍💻 Author

**Ashwitha Gogikar**

Data Analytics | Python | Power BI | Machine Learning

### Connect With Me

* **GitHub:** https://github.com/gshwitha2000-wq
* **LinkedIn:** https://www.linkedin.com/in/ashwitha-gogikar-35839a1b5/

---

## ⭐ Project Purpose

This project was created as a practical **Data Analytics / Exploratory Data Analysis portfolio project** to demonstrate the ability to work with transactional data, identify patterns, perform aggregations, and communicate business insights through visualizations.
