# 📊 Loan Dataset — Exploratory Data Analysis (EDA)

A beginner-friendly EDA project analysing a loan applicant dataset to uncover patterns in income distribution, loan allocation, and feature relationships.

---

## 📌 Objective

Perform end-to-end Exploratory Data Analysis on a loan dataset to:
- Understand the demographic and financial profile of applicants
- Detect missing values and handle them appropriately
- Identify income distribution patterns and outliers
- Explore the relationship between applicant income and loan amount
- Quantify correlations between numerical features

---

## 📁 Dataset

| Property | Detail |
|---|---|
| File | `test_Y3wMUE5_7gLdaTN.csv` |
| Source | Loan applicant records |
| Key Features | Gender, Married, Dependents, ApplicantIncome, CoapplicantIncome, LoanAmount, Credit_History, Property_Area |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading & manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualisations |
| Seaborn | Statistical plots & heatmap |
| Jupyter Notebook | Interactive analysis environment |

---

## 📂 Project Structure

```
loan-eda/
│
├── loan_eda_analysis.ipynb   # Main analysis notebook
├── test_Y3wMUE5_7gLdaTN.csv  # Dataset (not included in repo)
└── README.md
```

> ⚠️ The dataset file is not committed to this repository. Place it in the root directory before running the notebook.

---

## 🔍 Analysis Walkthrough

### 1. Data Loading & Inspection
- Loaded CSV using `pandas`
- Inspected shape, column names, and data types

### 2. Missing Value Treatment
- Identified nulls across all columns — `Credit_History` had the highest count
- Filled `LoanAmount` nulls with the **column mean**
- Filled `Credit_History` nulls with the **column mode**

### 3. Income Distribution
- Plotted a histogram of `ApplicantIncome`
- Compared mean vs. median to confirm **right skew**

### 4. Income vs. Loan Amount
- Scatter plot revealed a **moderate positive relationship**
- Not strictly proportional — other factors beyond income influence loan allocation

### 5. Correlation Heatmap
- Generated a heatmap of all numerical features
- Strongest correlation: `ApplicantIncome` ↔ `LoanAmount` at **0.49**

---

## 💡 Key Findings

- The dataset is dominated by **low to middle-income applicants**, with a few high-income outliers extending the right tail.
- **Applicant income is moderately correlated (0.49) with loan amount** — the strongest relationship in the dataset.
- **Coapplicant income** has minimal impact on loan amount.
- **Credit history shows surprisingly weak correlation** with loan amount, suggesting the column may require deeper analysis or feature engineering.
- Loan approval factors appear complex, with no single feature being a strong linear predictor.

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/loan-eda.git
cd loan-eda

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 3. Add the dataset to the project root
# (Place test_Y3wMUE5_7gLdaTN.csv here)

# 4. Launch Jupyter
jupyter notebook loan_eda_analysis.ipynb
```

---

## 🚀 Next Steps

- Handle remaining missing values (Gender, Self_Employed, Dependents)
- Encode categorical variables for modelling
- Build a baseline **Loan Default Prediction** classification model
- Deploy insights via a Streamlit dashboard

---

## 👤 Author

**Akash**  
Aspiring Machine Learning Engineer | Banking & Finance Domain  
[LinkedIn](https://www.linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)
