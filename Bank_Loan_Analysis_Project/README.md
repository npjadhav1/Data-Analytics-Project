# 🏦 Bank Loan Application Dashboard

An **advanced and interactive Power BI dashboard** that delivers deep insights into bank loan applications, loan performance, and borrower behaviors. Combined with robust **SQL queries** for backend validation, this project helps identify trends, monitor KPIs, and make strategic decisions regarding loan issuance and repayment.

---

## 📌 Project Overview

This dashboard visualizes and analyzes bank loan data using a variety of **KPIs** such as:

- Total loan applications
- Funded & received amounts
- Interest rates & DTI (Debt-to-Income)
- Loan quality (**Good vs Bad**)
- Loan status performance

It allows **interactive filtering and slicing** for a better understanding of patterns across demographics, time, and financial indicators.

---

## 🛠 Tools & Technologies Used

| Tool        | Purpose                                |
|-------------|----------------------------------------|
| **Power BI**  | Dashboard creation, visual reports     |
| **SQL**       | Backend data extraction, testing, validation |
| **DAX**       | KPI measures and logic               |
| **Power Query** | Data transformation                  |

---

## 🗂 Dashboard Pages

### 1️⃣ Landing Page – Navigation & Overview
**Purpose:**  
Acts as the starting page, giving users a visual summary of:
- **What to expect:** MTD, PMTD, MoM trends
- Breakdown of **Good vs Bad Loans**
- Navigation icons to **Summary**, **Overview**, and **Detail** pages

🎨 **Dark UI** with high visual clarity and icon-based navigation.

---

### 2️⃣ Summary Page – Key Metrics & Loan Quality
**Purpose:**  
High-level insights on loan volume and financial performance.

**KPIs:**
- Total Loan Applications
- Total Funded Amount
- Total Received Amount
- Average Interest Rate
- Average DTI

**Breakdown:**
- ✅ **Good Loans:** 86.2%, ~$370M funded
- ❌ **Bad Loans:** 13.8%, ~$65.5M funded

**Loan Status:**  
Fully Paid, Charged Off, Current with respective amounts, rates, and DTI.

---

### 3️⃣ Overview Page – Trend and Demographics Analysis
**Visual Components:**
- 📈 Monthly Trend Line
- 🗺 State-wise Choropleth Map
- 🍩 Loan Term Distribution (36 vs 60 months)
- 📊 Bar Charts: By Employee Length, Loan Purpose, Home Ownership

**Filters:**  
State, Grade, Purpose, Loan Status, Term

**📍 Insights:**
- Seasonal trends in loan applications
- Loan risk by purpose and state
- Home ownership & employment length impacts

---

### 4️⃣ Details Page – Record-Level Insights
**Purpose:**  
Raw data view at individual loan level for auditing or export.

**Fields:**  
Loan ID, Issue Date, Purpose, Home Ownership, Interest Rate, Installment, Funded/Received Amount, Grade, DTI

🔍 **Use for:**
- Subset exports
- Audits
- Customer-specific drilldowns

---

## 🧪 SQL Integration – Backend Validation

SQL was used extensively to **validate dashboard KPIs**, segments, and filters.

**SQL tasks included:**
- ✅ Data extraction from tables
- ✅ Loan type, status, and amount aggregation
- ✅ Cross-checking Power BI visual values

---

## ❓ Problem Solved by the Dashboard

**"Loan departments often struggle to track performance, identify risky applicants, and monitor repayment trends—especially when data is spread across thousands of loan applications."**

This **Power BI Dashboard** addresses multiple business and data analysis challenges in the banking and loan sector:

### 🔧 1. Lack of Centralized Insight into Loan Applications
✅ **Solution:** Aggregates all loan-related KPIs into one interactive view.

### 🔧 2. Difficulty in Identifying Good vs Bad Loans
✅ **Solution:** Separates **Good Loans** (Fully Paid, Current) from **Bad Loans** (Charged Off).

### 🔧 3. No Trend Tracking or Monthly Monitoring
✅ **Solution:** Uses MTD, PMTD, and MoM KPIs to show performance trends.

### 🔧 4. Poor Visibility into Regional and Demographic Behavior
✅ **Solution:** State-wise maps, charts by home ownership, employment length, and purpose.

### 🔧 5. Limited Ability to Audit or Review Individual Loans
✅ **Solution:** Detailed page with full record-level data.

### 🔧 6. Gap Between Raw Data and Dashboard Insights
✅ **Solution:** SQL query logic used to validate and verify backend metrics.

---

## 💡 Business Impact

🎯 Improves **strategic decision-making** based on real-time insights  
🔍 Helps reduce **loan defaults** by identifying risky patterns early  
📈 Supports smarter and **data-driven lending and recovery policies**

> _“With this dashboard, data isn't just numbers — it's actionable intelligence.”_

---

## 📊 Key Insights

- ✅ **86% of loans are Good Loans**
- 🔁 Fully Paid loans dominate, indicating good recovery
- ⚠️ Purposes like Debt Consolidation show higher risk
- 🕒 Long loan terms and state-level data offer segmentation value

---

## 👤 About Me

**Nikita Pralhad Jadhav**  
🎓 **B.Tech – Computer Science**  
📧 developer.nikita1011@gmail.com

Passionate about **data analysis**, **visualization**,**Data Cleaning**, and **impactful Data analytics solutions**.
