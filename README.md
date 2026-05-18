# 🏦 Bank Analytics Dashboard

A comprehensive data analysis project exploring banking customer behavior, loan patterns, and transaction insights using SQL, Power BI, Tableau, and Excel.

---

## 📌 Project Overview

This project analyzes banking data to understand customer segmentation, loan approval patterns, and transaction behavior — helping banks make smarter, data-driven decisions about their customers.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| SQL | Data querying & analysis |
| Power BI | Interactive dashboard |
| Tableau | Visual analytics |
| Excel | Data cleaning & exploration |

---

## 📊 Key Insights

- 👥 Identified **customer segments** based on age, income, and account activity
- 🏠 Analyzed key factors influencing **loan approvals and defaults**
- 💳 Observed **transaction patterns** and customer behavior trends
- 📊 High-income customers with long account history have the lowest default rates
- 🔍 Customers aged 30-45 represent the highest value segment

---

## 🖥️ Dashboard

[Click here to view Dashboard](https://drive.google.com/file/d/1apBhpKhe6TvJbC2s1HI1QNGyw3QIg7T2/view?usp=drive_link)

---

## 📁 Project Structure

```
Bank-Analytics-Dashboard/
│
├── data/                    ← Raw and cleaned banking data
├── sql/                     ← SQL queries for analysis
├── dashboard/               ← Power BI and Tableau files
└── README.md
```

---

## 🔄 Project Approach

### 1️⃣ Data Collection
- Banking dataset with customer demographics, account details, transactions, and loan information

### 2️⃣ Data Cleaning
- Handled missing values in income and transaction fields
- Standardized date formats and categorical variables
- Created derived features like customer age groups and transaction frequency

### 3️⃣ SQL Analysis
- Customer segmentation queries
- Loan approval rate by demographics
- Transaction pattern analysis
- Default risk identification

### 4️⃣ Dashboard
- Built Power BI dashboard with customer segment filters
- Tableau visualization for geographic and demographic analysis

---

## 📈 Dashboard Features

- 👥 Customer segmentation overview
- 💰 Loan approval and default rate analysis
- 💳 Transaction trend over time
- 🗺️ Geographic distribution of customers
- 📊 Income vs loan amount correlation
- 🔍 Interactive filters by age group, income, and region

---

## 🗄️ SQL Queries Used

```sql
-- Customer Segmentation
SELECT age_group, COUNT(*) as customers,
       AVG(balance) as avg_balance
FROM customers
GROUP BY age_group;

-- Loan Default Analysis
SELECT income_range,
       SUM(CASE WHEN loan_status = 'Default' THEN 1 ELSE 0 END) as defaults,
       COUNT(*) as total_loans,
       ROUND(SUM(CASE WHEN loan_status = 'Default' THEN 1 ELSE 0 END) * 100.0 / COUNT(*), 2) as default_rate
FROM loans
GROUP BY income_range;
```

---

## 🤝 Connect With Me

- 💼 LinkedIn: [Pooja Dudhal](https://www.linkedin.com/in/poojadudhal)
- 🐙 GitHub: [https://github.com/Poojadudhal-DA](https://github.com/Poojadudhal-DA)

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
