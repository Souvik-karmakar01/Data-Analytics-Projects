# 🛒 Customer Shopping Behavior Analysis

An end-to-end data analytics project analyzing e-commerce customer behavior using Python for data cleaning and EDA, SQL for business querying, and Power BI for dashboard delivery. Built on a dataset of 3,900 transactions across 18 features.

---

## 🛠️ Tools & Technologies
- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **SQL** — MySQL, PostgreSQL
- **Database Integration** — Python → PostgreSQL pipeline
- **Visualization** — Power BI

---

## 📁 Project Structure
```
Customer-Shopping-Behavior/
│
├── Customer_Shopping_Behavior_Analysis.pdf   # Full project report
└── README.md
```

---

## 📊 Dataset Overview
| Property | Value |
|----------|-------|
| Rows | 3,900 |
| Columns | 18 |
| Missing Values | 37 (Review Rating column) |

**Key Features:**
- **Demographics** — Age, Gender, Location, Subscription Status
- **Purchase Details** — Item, Category, Amount (USD), Season, Size, Color
- **Behavior** — Discount Applied, Previous Purchases, Frequency, Review Rating, Shipping Type

---

## 🔄 Project Workflow

### 1. Data Cleaning & Preparation (Python)
- Loaded dataset using Pandas; explored with `df.info()` and `.describe()`
- Imputed 37 missing Review Ratings using **category-wise median**
- Renamed columns to snake_case for consistency
- Verified redundancy between `discount_applied` and `promo_code_used` — dropped the latter
- Engineered `age_group` (binned) and `purchase_frequency_days` columns
- Loaded cleaned DataFrame into **PostgreSQL** for SQL analysis

### 2. SQL Business Analysis (10 Questions Answered)

| # | Business Question | Key Finding |
|---|------------------|-------------|
| i | Revenue by Gender | Male: $157,890 vs Female: $75,191 |
| ii | High-Spending Discount Users | Customers spending above average even with discounts |
| iii | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| iv | Shipping Type Comparison | Express: $60.48 avg vs Standard: $58.46 avg |
| v | Subscribers vs Non-Subscribers | Non-sub: 2,847 customers, $170,436 revenue |
| vi | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| vii | Customer Segmentation | Loyal: 3,116 \| Returning: 701 \| New: 83 |
| viii | Top 3 Products per Category | Jewelry, Blouse, Sandals, Jacket top their categories |
| ix | Repeat Buyers & Subscriptions | 958 repeat buyers subscribed vs 2,518 who didn't |
| x | Revenue by Age Group | Young Adult: $62K \| Middle-aged: $59K |

### 3. Power BI Dashboard
Interactive dashboard with filters for Gender, Category, Subscription Status, and Shipping Type — visualizing revenue, sales, and customer segments.

---

## 💡 Key Business Recommendations
1. **Boost Subscriptions** — Promote exclusive benefits; subscriber base is underpenetrated
2. **Customer Loyalty Programs** — Reward repeat buyers to shift them into the "Loyal" segment
3. **Review Discount Policy** — High discount dependency on key products risks margin erosion
4. **Product Positioning** — Highlight Gloves, Sandals, and Boots (top-rated) in marketing campaigns
5. **Targeted Marketing** — Focus on Young Adults (highest revenue) and Express-shipping users

---

## 🔧 How to Run
```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn psycopg2

# Step 1 — Run Python cleaning script and load to PostgreSQL
# Step 2 — Run SQL queries in MySQL/PostgreSQL
# Step 3 — Open Power BI file for dashboard
```
