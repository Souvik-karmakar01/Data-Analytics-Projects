# 📦 Vendor Performance Analysis

A full end-to-end data analytics project focused on evaluating vendor performance in a supply chain/procurement context. Built using Python, SQLite, and Power BI — covering data ingestion, metric engineering, statistical analysis, and interactive dashboard delivery.

---

## 🛠️ Tools & Technologies
- **Python** — Pandas, NumPy, Matplotlib, Seaborn, SciPy, SQLAlchemy
- **Database** — SQLite (`inventory.db`)
- **Visualization** — Power BI
- **Statistics** — T-Test, 95% Confidence Intervals

---

## 📁 Project Structure
```
Vendor-Performance-Analysis/
│
├── Vendor_Project.ipynb                 # Data ingestion & SQL pipeline
├── Vendor_Performance_Analysis.ipynb   # EDA, analysis & statistics
├── Vendor_Performance.pbix             # Power BI dashboard
└── README.md
```

---

## 🔄 Project Workflow

### 1. Data Ingestion Pipeline
- Loaded raw CSV files (purchases, sales, vendor invoices) into a SQLite database using **SQLAlchemy**
- Set up logging for the ingestion pipeline (`ingestion_db.log`)
- Queried tables using `pandas.read_sql_query()` for exploration

### 2. Feature Engineering
Created the following metrics for each vendor:
| Metric | Formula |
|--------|---------|
| Gross Profit | Total Sales Dollars − Total Purchase Dollars |
| Profit Margin | (Gross Profit / Total Sales Dollars) × 100 |
| Stock Turnover | Total Sales Quantity / Total Purchase Quantity |
| Sales-to-Purchase Ratio | Total Sales Dollars / Total Purchase Dollars |
| Unsold Inventory Value | (Purchase Qty − Sales Qty) × Purchase Price |
| Unit Purchase Price | Total Purchase Dollars / Total Purchase Quantity |

### 3. Exploratory Data Analysis
- Distribution plots and boxplots for all numerical columns
- Outlier detection and data cleaning (removed rows with negative profit/margins)
- Correlation heatmap across all key metrics
- Top 10 vendors by total sales and purchase contribution

### 4. Business Analysis
- **Procurement Concentration** — Top 10 vendors account for the majority of total procurement spend
- **Bulk Purchasing Impact** — Segmented orders into Small / Medium / Large using `pd.qcut()` and analyzed unit price impact
- **Slow-Moving Inventory** — Flagged vendors with Stock Turnover < 1 (excess stock risk)
- **Locked Capital** — Quantified unsold inventory value per vendor to surface overstocking risks

### 5. Statistical Analysis
- Computed **95% Confidence Intervals** for profit margins of top vs. low-performing vendors
- Ran a **two-sample T-Test** (Welch's) to determine if the difference in profit margins is statistically significant
- Result: Rejected H₀ — significant difference exists between top and low-performing vendor margins

---

## 📊 Power BI Dashboard
The interactive dashboard covers:
- Vendor KPIs (Sales, Profit Margin, Stock Turnover)
- Procurement concentration (Donut chart — top 10 vs others)
- Bulk purchasing impact on unit price
- Slow-moving and unsold inventory flags

---

## 💡 Key Business Insights
- Top 10 vendors drive the majority of procurement — high dependency risk
- Bulk orders lead to lower unit purchase prices, confirming economies of scale
- Several vendors have Stock Turnover < 1, indicating excess inventory and capital lockup
- Statistically significant margin gap between top and low performers — vendor tiering strategy recommended

---

## 🔧 How to Run
```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn scipy sqlalchemy

# Run notebooks in order
1. Vendor_Project.ipynb          # Sets up DB and ingests data
2. Vendor_Performance_Analysis.ipynb  # EDA + analysis
```
> Power BI file requires **Microsoft Power BI Desktop** to open.
