# 🏦 Banking Risk Analytics Dashboard – Power BI Project

## 📌 Overview

This project demonstrates the use of Power BI to build a dynamic and interactive **Banking Risk Analytics Dashboard**. It aims to help banking institutions reduce financial risk through data-driven decision-making regarding client loans, deposits, credit, and overall engagement.

---

## 📂 Contents

- Power BI Dashboard File (.pbix)
- Cleaned & Processed Datasets (Client-Banking, Gender, Period, etc.)
- Calculated Columns & DAX Measures
- Multiple Linked Dashboards
- README Documentation

---

## 🧠 Problem Statement

Develop a basic understanding of risk analytics in banking and financial services, and analyze how data can be used to **minimize loan defaults** and **identify client engagement** patterns.

---

## 📊 Dataset Information

The dataset includes information on:

- Client details (ID, age, location, gender, etc.)
- Account information (credit card balance, loans, deposits)
- Fee structure (High, Mid, Low)
- Banking relationships (joining date, engagement length)
- Advisor & Periodic data

---

## 🧹 Data Cleaning & Engineering

- Created **Engagement Days** using `DATEDIFF(Joined Bank, TODAY(), DAY)`
- Created **Income Band** using bins (< ₹100K = Low, < ₹300K = Mid)
- Created **Processing Fee** column based on Fee Structure:
  - High = 5%
  - Mid = 3%
  - Low = 1%

---

## 📈 Key DAX Measures

- `Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID])`
- `Total Loan = [Bank Loans] + [Business Lending] + [Credit Cards Balance]`
- `Total Deposit = [Bank Deposits] + [Saving Accounts] + [Checking Accounts] + [Foreign Currency Account]`
- `Total Fees = SUMX('Clients - Banking', [Total Loan] * [Processing Fees])`
- `Engagement Length = SUM('Clients - Banking'[Engagement Days])`

---

## 📌 Dashboards

- **Home Page**
- **Loan Analysis**
- **Deposit Analysis**
- **Client Summary Dashboard**

---

## ✅ KPIs Tracked

- Total Clients
- Total Loans
- Total Deposits
- Total Processing Fees
- Engagement Duration
- Credit Card Balances
- Account-specific holdings

---

## 🧾 Conclusion

With the power of DAX and data modeling, this project presents an effective dashboard to analyze banking risks and client behavior. It enables banks to strategize loan approvals, fee allocations, and customer retention efforts more efficiently.

---

## 🚀 Future Work

- Integrate predictive models (e.g., loan default probability)
- Include real-time data ingestion from databases
- Enhance dashboard with ML-driven segmentation


