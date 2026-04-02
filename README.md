# 📦 FMCG Supply Chain Analytics Project

An end-to-end supply chain analytics solution simulating a real-world FMCG environment — covering demand forecasting, inventory planning, bullwhip analysis, and S&OP planning — built entirely in Microsoft Excel with an interactive Power BI dashboard.

---

## 📌 Project Overview

| Attribute | Detail |
|---|---|
| **SKUs** | 15 products |
| **Regions** | North, South, West |
| **Warehouses** | Delhi, Mumbai, Bangalore |
| **Historical Data** | 24 months |
| **Tools** | Microsoft Excel, Power BI |

---

## 🔍 Key Modules

### 📊 Demand Forecasting
- Applied **Moving Average (MA-3 and MA-6)** and **Exponential Smoothing** methods
- Generated **6-month forward forecasts** per SKU per region
- Evaluated accuracy using **MAPE (Mean Absolute Percentage Error)**
- Selected the best-performing forecasting method per product per region

### 📦 Inventory Planning
Calculated the following metrics for each SKU across all three warehouses:
- **EOQ** (Economic Order Quantity)
- **Safety Stock** (using Z-score = 1.65 for 95% service level)
- **Reorder Point (ROP)**
- **Days of Cover**
- Flagged inventory status as **Critical** or **Reorder** for proactive decision-making

### 🔄 Bullwhip Effect Analysis
- Measured **CV of Orders vs CV of Demand** to quantify supply chain volatility
- Notable findings:
  - **SKU006 – Lifebuoy 125g**: Highest Bullwhip Ratio of **1.71**
  - **SKU014 – Close Up 80g**: Bullwhip Ratio of **1.65**
- Both SKUs flagged for demand amplification requiring urgent intervention

### 📋 S&OP Summary
- Compared **Total Supply** (Current Stock + Incoming POs) against 6-month forecast
- All 15 SKUs showed **shortage status**
- Average supply gap of **~75%** — highlighting the need for aggressive replenishment planning

---

## 📈 Power BI Dashboard

Interactive dashboard featuring:
- **KPI Cards** — key supply chain metrics at a glance
- **6 Charts** — forecasts, inventory status, bullwhip ratios, supply gaps
- **Region / Product Slicers** — dynamic filtering for drill-down analysis

---

## 🛠️ Tools & Techniques

**Microsoft Excel**
- `AVERAGEIFS`, `SUMIFS`, `VLOOKUP`
- Pivot Tables
- Array formulas
- Statistical calculations (MAPE, CV, Z-score based safety stock)

**Power BI**
- DAX measures
- Star schema data model
- Interactive slicers and KPI visuals

---

## 📁 Repository Structure

```
fmcg-supply-chain-analytics/
│
├── data/
│   └── raw_data.xlsx               # 24-month historical demand & inventory data
│
├── excel/
│   └── FMCG_Supply_Chain.xlsx      # Main workbook (all modules)
│
├── powerbi/
│   └── FMCG_Dashboard.pbix         # Power BI dashboard file
│
├── screenshots/
│   ├── dashboard_overview.png
│   ├── inventory_planning.png
│   └── bullwhip_analysis.png
│
└── README.md
```

---

## 💡 Key Insights

1. **Demand amplification** is concentrated in personal care SKUs (Lifebuoy, Close Up) — investigate ordering patterns upstream.
2. **Stockout risk is universal** — all 15 SKUs face a supply shortfall over the next 6 months; replenishment plans are critical.
3. **Exponential Smoothing** outperformed Moving Average for most SKUs with higher demand volatility.
4. Safety stock levels across warehouses are currently **insufficient** to buffer against demand variability at a 95% service level.

---

## 👤 Author

**Rishi Chandran**  
B.Tech Industrial Engineering | College of Engineering Trivandrum (CET)  
Specialization: Supply Chain Analytics  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/rishi-chandran-525970262)
[![Email](https://img.shields.io/badge/Email-rishichandran17%40gmail.com-red?logo=gmail)](mailto:rishichandran17@gmail.com)

---

## 🏷️ Tags

`Supply Chain` `FMCG` `Demand Forecasting` `Inventory Optimization` `Bullwhip Effect` `S&OP` `Power BI` `Excel` `Data Analytics` `Operations Research`
