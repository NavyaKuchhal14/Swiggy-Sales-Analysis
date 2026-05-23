# Swiggy Food Delivery — Sales & Demand Analysis | Python

## Project Overview

India's food delivery market is worth $12 billion. But most restaurants on Swiggy have no idea when their orders peak, which dishes actually drive revenue, or whether their ratings are helping or hurting them.

I analyzed 197,430 food delivery records across 28 Indian cities, 993 restaurants, and 4,972 dish categories to uncover ordering patterns, revenue drivers, and demand trends that can inform real operational and marketing decisions.

## The Business Problem

Swiggy (or any food delivery aggregator) needs answers to five questions:
1. When do orders peak — by month, week, and day?
2. Which cities and states drive the most revenue?
3. Does Veg or Non-Veg food generate more revenue?
4. Which restaurants and dishes are top performers vs. underperformers?
5. Is there a correlation between ratings and sales volume?

## Dataset

- **Records:** 197,430 orders
- **Columns:** 10 (State, City, Order Date, Restaurant Name, Location, Category, Dish Name, Price, Rating, Rating Count)
- **Cities covered:** 28 across India
- **States covered:** 28
- **Restaurants:** 993 unique
- **Dish categories:** 4,972
- **Price range:** ₹0.95 – ₹8,000
- **Rating range:** 1.5 – 5.0

## KPIs Calculated

| KPI | Value |
|-----|-------|
| Total Revenue | ₹5.30 Crore |
| Average Rating | 4.34 / 5.0 |
| Average Order Value | ₹268.51 |
| Total Orders | 197,430 |

## Key Insights

→ **Bengaluru dominates revenue** at ₹54.5 Lakhs — nearly 75% more than the #2 city (Lucknow at ₹31.1L). Hyderabad, Mumbai, and New Delhi round out the top 5.

→ **Weekend evenings show significantly higher order volumes** vs weekdays — confirming that demand-based staffing and promotional timing should target Friday–Sunday dinner windows.

→ **Veg food generates the majority of revenue** — challenging the assumption that non-veg items carry higher ticket sizes. The keyword-based classification (chicken, egg, fish, mutton, biryani) reveals Veg dominance across most Indian cities.

→ **"Recommended" category drives 24,100 orders** — more than 8x the next category (Main Course at 2,959). Swiggy's recommendation algorithm is the single most powerful sales channel for restaurants.

→ **Average rating of 4.34 suggests rating inflation** — most restaurants cluster between 4.0–4.8, making differentiation by rating nearly meaningless for consumers.

→ **Weekly revenue shows significant volatility** — identifying consistent vs. inconsistent weeks helps forecast demand for delivery fleet planning.

## Visualizations Built

1. **Monthly Sales Trend** — Line chart showing revenue fluctuation month over month
2. **Daily Sales Trend** — Bar chart showing Mon–Sun revenue distribution
3. **Veg vs Non-Veg Revenue Split** — Donut chart with percentage breakdown
4. **Revenue by State** — Horizontal bar chart ranking all 28 states
5. **Quarterly Performance Summary** — Combined Sales, Ratings, and Orders by quarter
6. **Top 5 Cities by Sales** — Horizontal bar chart identifying leading revenue cities
7. **Weekly Trend Analysis** — Bar chart monitoring weekly revenue fluctuations

## Approach

1. **Data Loading & Inspection:** Loaded 197,430 records from Excel using Pandas. Inspected shape, data types, null values, and descriptive statistics.

2. **Data Cleaning & Feature Engineering:** Converted Order Date to datetime. Created derived columns — YearMonth, DayName, Quarter, Week Number. Built a keyword-based food classification system (Veg vs Non-Veg) using NumPy's `np.where` with pattern matching.

3. **KPI Calculation:** Computed Total Sales, Average Rating, Average Order Value, Ratings Count, and Total Orders using Pandas aggregation.

4. **Visualization:** Built 7 charts using Matplotlib, Seaborn, and Plotly — covering time series, categorical comparison, geographic distribution, and proportional analysis.

5. **Insight Generation:** Translated each visualization into a plain-language business insight with specific recommendations.

## Tools & Technologies

- **Python** — Core analysis language
- **Pandas** — Data manipulation and aggregation
- **NumPy** — Conditional logic and array operations
- **Matplotlib** — Static charts (line, bar)
- **Seaborn** — Statistical visualization
- **Plotly** — Interactive charts (pie, bar, treemap)
- **Jupyter Notebook** — Analysis environment

## Files in This Repository

| File | Description |
|------|-------------|
| `Swiggy_Sales_Analysis.ipynb` | Complete Jupyter Notebook with code and outputs |
| `swiggy_data.xlsx` | Raw dataset (197,430 records) |
| `Swiggy_PPT.pptx` | Presentation with problem statement and BRD |
| `screenshots/` | Chart screenshots for portfolio |

## How to Run

1. Clone this repo: `git clone https://github.com/navya-kuchhal/Swiggy-Sales-Analysis-Python.git`
2. Install dependencies: `pip install pandas numpy matplotlib seaborn plotly openpyxl`
3. Open the notebook: `jupyter notebook Swiggy_Sales_Analysis.ipynb`
4. Run all cells

## Screenshots

![Monthly Sales Trend] 
<img width="426" height="281" alt="Swiggy1" src="https://github.com/user-attachments/assets/4a26f41a-4f45-4dd6-b112-08fe0bb7ef35" />

![Top 5 Cities](screenshots/top-cities.png)
<img width="1199" height="525" alt="newplot (1)" src="https://github.com/user-attachments/assets/a0f1d6e2-be34-4175-98da-12c2a2642881" />

![Veg vs Non-Veg](screenshots/veg-nonveg.png)
<img width="1199" height="500" alt="newplot (2)" src="https://github.com/user-attachments/assets/2323aa02-99c6-46f5-b108-a2aeff12172d" />

