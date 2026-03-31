# 🏦 Banking Risk & Loan Analysis Dashboard

A Power BI project focused on risk analytics in banking — helping financial institutions make data-driven loan approval decisions based on applicant profiles. Covers relational data modeling, DAX measure engineering, and a 4-page interactive dashboard.

---

## 🛠️ Tools & Technologies
- **Power BI** — DAX, Data Modeling, Interactive Dashboards, Slicers
- **Python** — EDA and data preparation
- **SQL** — Relational database queries

---

## 📁 Project Structure
```
Banking-Dashboard/
│
├── Banking_Dashboard.pbix     # Power BI dashboard file
├── Banking_Report.docx        # Project report with methodology
└── README.md
```

---

## 🗄️ Dataset Overview
A relational banking database with **5 interconnected tables** linked via primary and foreign keys:

| Table | Description |
|-------|-------------|
| Clients - Banking | Core client financials (loans, deposits, accounts) |
| Banking Relationship | Client-advisor relationship mapping |
| Gender | Gender lookup table |
| Investment Advisor | Advisor details |
| Period | Time dimension table |

---

## 🔧 Data Preparation

### Feature Engineering
- **Income Band** — Binned Estimated Income into `Low` (<₹1,00,000) and `Mid` (<₹3,00,000)
- **Processing Fees** — Created dynamic fee column using SWITCH logic: High fee structure → 5% processing fee

---

## 📐 DAX Measures Built

| Measure | Formula Logic |
|---------|--------------|
| Bank Loan | `SUM(Clients-Banking[Bank Loans])` |
| Business Lending | `SUM(Clients-Banking[Business Lending])` |
| Total Loan | Bank Loan + Business Lending + Credit Cards Balance |
| Total Deposit | Bank Deposit + Savings + Foreign Currency + Checking Accounts |
| Total Fees | `SUMX(Clients-Banking, [Total Loan] * Processing Fees)` |
| Engagement Length | `SUM(Clients-Banking[Engagement Days])` |
| Total CC Amount | `SUM(Clients-Banking[Amount of Credit Cards])` |

---

## 📊 Dashboard Pages

### 1. Home
Overview KPIs — Total Loans, Total Deposits, Client Count, Engagement metrics

### 2. Loan Analysis
- Loan breakdown by bank type, nationality, gender, and advisor
- Helps identify high-risk loan segments

### 3. Deposit Analysis
- Deposit distribution across account types
- Savings vs. Foreign Currency vs. Checking account trends

### 4. Summary Dashboard
- Holistic view combining loan and deposit KPIs
- Designed for executive-level decision making

---

## 💡 Key Business Insights
- **Private banks attract more clients** than public banks — strategic insight for competitor benchmarking
- Income Band segmentation reveals distinct borrowing patterns between Low and Mid income groups
- High fee structure clients generate disproportionately higher processing fee revenue
- Dashboard enables real-time loan approval/rejection decisions based on live applicant profiles

---

## 🔧 How to Open
> Requires **Microsoft Power BI Desktop** (free download from Microsoft).
> Open `Banking_Dashboard.pbix` directly in Power BI Desktop.
