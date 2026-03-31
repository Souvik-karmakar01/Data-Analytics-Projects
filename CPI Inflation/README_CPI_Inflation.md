# 📈 CPI Inflation Case Study – India (Jan 2013 – May 2023)

An Excel-based analytical project investigating India's Consumer Price Index (CPI) inflation trends over 10 years across Rural, Urban, and combined sectors. Covers category contribution analysis, Y-o-Y trend tracking, COVID-19 impact, and oil price correlation.

---

## 🛠️ Tools & Technologies
- **MS Excel** — Pivot Tables, Charts, VLOOKUP, =CORREL, Data Validation, Conditional Formatting

---

## 📁 Project Structure
```
CPI-Inflation/
│
├── CPI_CaseStudy_v1.xlsx    # Main project file (all sheets)
└── README.md
```

### Excel Sheets Overview
| Sheet | Description |
|-------|-------------|
| Raw Data | Original CPI data (Jan 2013 – May 2023), 373 rows × 30 columns |
| Notes | Data dictionary, valuable points, password info |
| Main Data | Cleaned data with 5 engineered broader category buckets |
| EDA & Analysis | Objective-wise analysis outputs |
| Communication | Visualizations and charts for stakeholder presentation |
| Sample Size Analysis | Sample summary (Jan 2013 – May 2023) |
| Objectives | Problem statements for all 5 objectives |

---

## 🎯 Objectives & Analysis

### Objective 1 — Category Contribution to CPI
- Grouped 30 raw columns into 5 broader buckets: **Edible Items, Clothing & Footwear, Household & Living Expenses, Self-Development & Well-Being, Sins & Others**
- Calculated each bucket's % contribution to the CPI basket
- Identified the highest-contributing category

### Objective 2 — Year-on-Year Inflation Trend (2017 onwards)
- Computed Y-o-Y growth rates for the combined Rural+Urban CPI
- Plotted a trend chart highlighting the peak inflation year
- Researched and documented the economic reason behind the spike

### Objective 3 — Food Inflation Analysis (12 Months ending May 2023)
- Investigated month-on-month changes in the Food & Beverages bucket
- Identified the month with highest and lowest food inflation
- Pinpointed the single biggest category contributor within food

### Objective 4 — COVID-19 Impact on Inflation
- Compared CPI trends before and after March 2020 (lockdown onset)
- Focused on Healthcare, Food, and Essential Services categories
- Highlighted structural shifts in spending post-pandemic

### Objective 5 — Crude Oil Price vs. Inflation Correlation
- Analyzed imported crude oil price fluctuations (2021–2023) month-on-month
- Used Excel's `=CORREL()` function to find correlation with each CPI category
- Identified the category most sensitive to oil price changes

---

## 💡 Key Insights
- Edible Items consistently hold the largest share of the CPI basket
- COVID-19 caused a visible spike in healthcare and essential goods inflation post-March 2020
- A strong positive correlation exists between crude oil prices and Transport & Communication inflation
- Food inflation peaked in specific months aligned with seasonal supply shocks

---

## 📌 Data Source
- CPI data sourced from the **Ministry of Statistics and Programme Implementation (MoSPI), Government of India**
- Coverage: January 2013 – May 2023
