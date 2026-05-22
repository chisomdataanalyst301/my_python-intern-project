# my_python-intern-project

## 📉 Customer Churn Analysis & Prediction

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

---

## 📌 Project Overview

This project analyzes **customer churn** in a telecommunications company using Python. The goal is to understand why customers leave and build a machine learning model that **predicts which customers are likely to churn** — so the business can take action before they leave.

The final output is a CSV file with churn predictions that is exported to **Power BI** for dashboard visualization.

---

## ❓ Problem Statement

Customer churn is one of the biggest challenges in the telecom industry. Every customer that leaves costs the business money. This project answers the key question:

> **"Which customers are at risk of churning and what factors are driving it?"**

---

## 📂 Project Structure

```
customer-churn-analysis/
│
├── churn.ipynb                    # Main Jupyter Notebook (full analysis)
├── churn.csv                      # Raw dataset (input)
├── churn_with_predictions.csv     # Final output with predicted churn column
└── README.md                      # Project documentation (this file)
```

---

## 📊 Dataset

The dataset used is `churn.csv` — a telecom customer dataset containing information about:

| Column | Description |
|---|---|
| `State` | US state the customer is from |
| `International plan` | Whether the customer has an international plan (Yes/No) |
| `Voice mail plan` | Whether the customer has a voicemail plan (Yes/No) |
| `Total day minutes` | Total minutes used during the day |
| `Total day charge` | Total charge for day usage |
| `Churn` | Whether the customer churned (True/False) |

---

## 🔍 Analysis Workflow

The project follows a standard data analysis pipeline:

### 1. 📥 Data Loading
- Loaded the dataset using **Pandas**
- Previewed the first 20 rows with `churn.head(20)`

### 2. 🧹 Data Exploration & Cleaning
- Checked for missing values using `churn.isnull().sum()`
- Inspected data types using `churn.info()`
- Generated summary statistics using `churn.describe()`

### 3. 📈 Exploratory Data Analysis (EDA)
- Compared the **mean of every column** for churned vs non-churned customers using `groupby`
- Identified customers with **extremely high day minutes** (over 300) as potential churn risk
- Visualized correlations between all variables using a **Correlation Heatmap**
- Plotted the **distribution of Total Day Minutes** using a histogram
- Used a **scatter plot** to explore the relationship between Total Day Minutes and Total Day Charge, colored by churn status

### 4. ⚙️ Data Preprocessing
- Encoded binary categorical features (`International plan`, `Voice mail plan`) using **LabelEncoder**
- Converted `Churn` from True/False to 1/0
- Dropped the `State` column for simplicity
- Split the data into **80% training and 20% testing** sets
- Applied **StandardScaler** to normalize numerical features

### 5. 🤖 Machine Learning Model
- Trained a **Random Forest Classifier** using the best parameters:
  - `max_depth = 10`
  - `n_estimators = 200`
  - `random_state = 42`
- Added the predicted churn column back to the dataframe
- Exported the final file as `churn_with_predictions.csv` for Power BI

---

## 📉 Key Visualizations

### Correlation Heatmap
Shows how strongly each variable is related to another. Helps identify which features most influence churn.

### Distribution of Total Day Minutes
Shows the spread of day usage across all customers — customers with very high usage tend to churn more.

### Total Day Minutes vs Total Day Charge (by Churn)
Scatter plot showing that customers who churn tend to have higher day minutes and higher charges.

---

## 🛠️ Tools & Libraries Used

| Tool | Purpose |
|---|---|
| **Python** | Main programming language |
| **Pandas** | Data loading, cleaning and exploration |
| **Seaborn** | Data visualization (heatmap, histogram, scatter) |
| **Matplotlib** | Plotting charts |
| **Scikit-learn** | Machine learning — preprocessing, model training |
| **Random Forest** | Classification model for churn prediction |
| **Power BI** | Dashboard visualization of predictions |

---

## 🚀 How to Run This Project

**Step 1** — Clone this repository
```bash
git clone https://github.com/yourusername/customer-churn-analysis.git
```

**Step 2** — Install the required libraries
```bash
pip install pandas seaborn matplotlib scikit-learn
```

**Step 3** — Open the notebook
```bash
jupyter notebook churn.ipynb
```

**Step 4** — Update the file path in the notebook
Change this line to match where your `churn.csv` file is saved:
```python
churn = pd.read_csv(r"C:\Users\USER\Downloads\churn.csv")
```

**Step 5** — Run all cells from top to bottom

The final file `churn_with_predictions.csv` will be saved in your working directory, ready for Power BI.

---

## 💡 Key Findings

- Customers with **high total day minutes** are more likely to churn
- Customers on the **International plan** show a higher churn rate
- **Total day charge** is strongly correlated with total day minutes — meaning high usage leads to high bills which drives churn
- The **Random Forest model** successfully predicts churn with parameters tuned for best performance

---

## 🔮 Next Steps

- Evaluate model performance with accuracy, precision, recall and F1 score
- Try other models — Logistic Regression, XGBoost — and compare results
- Build a Power BI dashboard to visualize churn predictions interactively
- Include the `State` column to analyze churn by geography

---

## 👤 Author

**CHISOM PRECIOUS**
- GitHub: [https://github.com/chisomdataanalyst301/chisomdataanalyst301)
- LinkedIn: [https://www.linkedin.com/in/chisom-precious-8685b4282)

---

## 📅 Date

May 2026

---

*This project was completed as part of an internship program to apply data analysis and machine learning skills in a real-world business context — analyzing customer behaviour and building predictive models using Python.*
