# 📞 Telecom Customer Churn Analysis

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://www.python.org/) 
[![SQL Server](https://img.shields.io/badge/SQL%20Server-2019-blue?logo=microsoftsqlserver)](https://www.microsoft.com/en-us/sql-server) 
[![Power BI](https://img.shields.io/badge/PowerBI-Desktop-yellow?logo=microsoftpowerbi&logoColor=white)](https://powerbi.microsoft.com/)

---

## 📝 Project Overview
This **Telecom Customer Churn Analysis** project is an end-to-end data analytics workflow aimed at **analyzing customer churn patterns** and **predicting future churners**. It combines **ETL**, **Power BI visualizations**, and **machine learning** for actionable business insights.

**Objective:**  
Understand churn behavior using demographic, geographic, account, and service data, and predict customers likely to churn.

---

## 🔹 Key Features
- ETL process with **SQL Server** to clean and structure raw data
- Data visualization dashboards in **Power BI** for insights
- Machine learning-based churn prediction using **Random Forest**
- Interactive prediction dashboard with drill-through capabilities
- Full pipeline from raw CSV data to actionable business insights

---

## 📊 Power BI Dashboards
### Summary Dashboard
- Total Customers, New Joiners, Total Churn, Churn Rate%
- Demographics: Gender, Age Group
- Account Info: Payment Method, Contract Type, Tenure
- Geography: Top 5 States by Churn
- Services: Internet Type & Churn %

### Churn Reason Page
- Drill-through: See churn reason-wise counts per customer

### Prediction Dashboard
- Customer ID, Monthly Charge, Total Revenue, Refunds, Referrals
- Demographics: Gender, Age Group, Marital Status
- Account Info: Payment Method, Contract, Tenure Group
- Geography: State-wise churn predictions

![Churn Dashboard Preview]
<img width="492" height="240" alt="image" src="https://github.com/user-attachments/assets/ab6a5312-7a16-4040-a1ab-a62dd654d468" />


---

## 🛠️ Tools & Technologies
| Tool | Purpose |
|------|---------|
| SQL Server | Data ETL & storage |
| Power BI Desktop | Data visualization & dashboards |
| Python (Jupyter Notebook) | Data preprocessing & machine learning |
| scikit-learn | Random Forest model training |
| Excel | Data preparation & prediction outputs |

---

## 💡 Workflow Overview

### 1️⃣ ETL & SQL
- Loaded CSVs into `stg_Churn` staging table
- Cleaned null values using `ISNULL()`
- Created production table `prod_Churn`
- Built SQL Views: `vw_ChurnData` (Churned/Stayed) & `vw_JoinData` (Joined)

### 2️⃣ Power BI Transformations
- Added `Churn Status` column (1 = Churned, 0 = Stayed)
- Binned `Monthly Charges` & created Age/Tenure groups
- Unpivoted service columns for analysis

### 3️⃣ Power BI Measures
```DAX
Total Customers = COUNT(prod_Churn[Customer_ID])
New Joiners = CALCULATE(COUNT(prod_Churn[Customer_ID]), prod_Churn[Customer_Status]="Joined")
Total Churn = SUM(prod_Churn[Churn Status])
Churn Rate = [Total Churn] / [Total Customers]
````

### 4️⃣ Machine Learning (Python)

* Dropped irrelevant columns
* Label encoded categorical features
* Split data: 80% training / 20% testing
* Trained Random Forest Classifier
* Evaluated using Confusion Matrix & Classification Report
* Predicted churners on new customers

---

## 🚀 Results

* Clear **churn insights** by demographics, geography, services, and tenure
* Identified **top churn reasons**
* Successfully predicted potential churners for proactive retention strategies

---

## 👨‍💻 Author

**Praneeth Kumar Reddy**
Data Analyst | Miami, FL
[LinkedIn](https://www.linkedin.com/in/praneethreddy)

```

This is fully copy-paste-ready for GitHub.  

If you want, I can also create a **slightly shorter version optimized for GitHub portfolio look**, which highlights key visuals and results even more. Do you want me to do that?
```
