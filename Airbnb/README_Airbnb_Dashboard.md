# 🏠 Global Airbnb Performance Dashboard

A Power BI project analyzing Airbnb's global performance across 10 major cities — covering listing trends, market share, pricing, ratings, seasonality, and host trust metrics. Built on a dataset of 2,79,712 listings and 5.37M reviews spanning 2008–2021.

---

## 🛠️ Tools & Technologies
- **Power BI** — DAX, Interactive Dashboards, Slicers, Custom Visuals

---

## 📁 Project Structure
```
Airbnb-Dashboard/
│
├── Airbnb_Dashboard.pbix    # Power BI dashboard file
└── README.md
```

---

## 📊 Dataset Overview

| Metric | Value |
|--------|-------|
| Total Listings | 2,79,712 |
| Total Cities | 10 |
| Total Hosts | 1,82,024 |
| Property Types | 144 |
| Total Reviews | 5.37 Million |

**Cities Covered:** Paris, New York, Sydney, Rome, Rio de Janeiro, Istanbul, Mexico City, Bangkok, Cape Town, Hong Kong

---

## 📋 Dashboard Pages

### Page 1 — New Listings Trend (2008–2021)
Mapped Airbnb's full business lifecycle across phases:

| Phase | Period | Key Event |
|-------|--------|-----------|
| Introduction | 2008–2010 | Platform launch, slow growth |
| Growth | 2010–2013 | Rapid listing expansion (Take-Off Point) |
| Maturity | 2013–2015 | Peak listings reached in **2015** |
| Decline | 2016–2017 | Tightening local regulations |
| Reinvention | 2017–2019 | First full profitable year in 2017 |
| COVID-19 | 2020–2021 | Sharp drop in new listings |

### Page 2 — Market Share & Pricing by City
- **Paris leads** with the most listings and reviews (23.1% of total)
- Paris, NYC, and Sydney combined account for ~48% of all reviews
- Paris hotel rooms are priced 2x higher than Airbnb — key driver of Airbnb's dominance there
- Average prices by room type: Hotel ($800) > Entire Place ($673) > Shared ($580) > Private ($462)

**City Ratings (Accuracy / Cleanliness / Location / Value):**
- 🏆 Best Overall: **Mexico City** and **Rio de Janeiro**
- ⚠️ Lowest Rated: **Hong Kong** and **Istanbul**
- Cleanliness and Value for Money score lowest across all cities

### Page 3 — Review Frequency, Seasonality & Trust
- **86.3%** of customers wrote only 1 review; 98.8% wrote 3 or fewer
- Paris and Rome dominate review share from **April to August** (peak European summer travel)
- New York peaks in **November–December** (holiday season)
- **Trust metrics:** 66.9% of hosts are identity-verified with a profile picture; only 0.1% are anonymous and unverified

---

## 💡 Key Business Insights
- 2015 was Airbnb's peak year for new listings — plateau driven by regulatory tightening
- Paris is the single most dominant market; hotel price premium makes Airbnb highly competitive there
- Seasonality patterns are strongly geographic — targeting marketing by city + season can boost occupancy
- High host verification rates (66.9%) signal strong platform trust — a key retention and acquisition lever
- Low review frequency (most users review only once) suggests review incentive programs could improve data quality

---

## 🔧 How to Open
> Requires **Microsoft Power BI Desktop** (free download from Microsoft).
> Open `Airbnb_Dashboard.pbix` directly in Power BI Desktop.
