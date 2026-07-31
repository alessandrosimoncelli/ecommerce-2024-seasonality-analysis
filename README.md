# 2024 E-Commerce Performance Analysis — Seasonality & Margin Erosion

Executive data visualization project analyzing 2024 e-commerce performance for a nationally-recognized retailer, built for a five-slide executive presentation backed by an interactive Tableau dashboard.

**Assignment:** A1 — Executive Presentation: Data-Driven e-Commerce Strategy & Recommendations
**Institution:** Hult International Business School
**Author:** Alessandro Simoncelli

## The Brief

Acting as the executive overseeing e-Commerce, the task was to analyze the retailer's 2024 performance and deliver 3–4 data-backed recommendations to drive sales and profitability, communicated through:
- A 5-slide executive presentation (plus an appendix of dashboard screenshots)
- An interactive Tableau dashboard using at least two linked actions (filter, hover, or interactive reference lines)
- A short video walkthrough of the presentation

## Key Findings

| Metric | Value |
|---|---|
| Total 2024 sales | $64M |
| Overall profit margin | 29% |
| Revenue share from November | 32% |
| Technology dept. share of total sales | 27% |
| Greenery/Naturals margin | 35%+ |
| November median price drop | -41% ($14.30 → $8.50) |
| November margin (Technology) | 15–20% → **-4%** |
| Share of total losses from Provocraft | 78% |

## Analysis Walkthrough

### 1. The Headline Number Hides a Concentration Risk
2024 closed at $64M in sales and a healthy 29% overall margin — but 32% of annual revenue lands in a single month, November. That concentration is a real operational and financial risk on its own, and it gets worse on closer inspection: **profit margin actually falls as sales spike** in November. The business is trading margin for volume through aggressive Black Friday discounting, and that trade-off is eroding profitability rather than simply shifting it across the calendar.

### 2. Where the November Dependency Comes From: Department Positioning
Each department was mapped on margin vs. sales volatility (standard deviation of monthly sales, used as a seasonality proxy), with bubble size representing 2024 sales volume.
- **Technology** is the largest department (27% of total sales), sitting in low-volatility / modest-margin territory (~10%).
- **Greenery/Naturals** delivers 35%+ margins but with sales heavily concentrated in Q4 — a genuine profit engine, but one that requires precise inventory timing to execute well.
- Seasonal departments broadly are what drive the November peak.

### 3. Where to Focus: Vendor Portfolio Action Plan
The same framework applied at vendor level, filtered to vendors selling at least one unit every month, splits the portfolio into four groups:
- **Evergreen performers** (e.g., Unique, Macarons) — ~45% margins, stable year-round. *Action:* scale with continuous marketing, negotiate exclusive SKUs. Target: +20–25% evergreen sales, reducing Q4 dependency.
- **Seasonal profit engines** (e.g., Mr. Christmas, National Tree) — ~45% margins, concentrated in Q4. *Action:* secure inventory 8–10 weeks pre-November, negotiate early-order discounts, run concentrated campaigns.
- **Low-margin, consistent vendors** (e.g., Provocraft) — *Action:* test price increases on low-elasticity items, or renegotiate terms.
- **High-risk seasonal vendors** — none identified, indicating good existing portfolio discipline.

### 4. What Went Wrong: Negative-Margin SKUs
Losses are concentrated in November, exactly when discounting is heaviest. The critical finding: **78% of total annual losses trace back to a single vendor, Provocraft**, which makes up the majority of the Technology department. A SKU-level treemap, color-coded by margin, isolates the worst offenders — e.g., SKU D204420S alone lost $170,000, and D036142S lost $48,000 at a less severe margin.

### 5. Root Cause: The November Pricing Collapse
Within Technology, median price held near $14 from January to October, then fell 41% to $8.50 in November. Margin followed the same path — a healthy 15–20% all year, collapsing to **-4%** in November. An interactive tooltip in the Tableau dashboard drills into individual SKUs to show exactly when losses occurred and how far price dropped.

**Findings:** many November negative-margin SKUs were already near 0% margin *before* Black Friday; the extra discount is what pushes structurally weak products into outright losses.

**Recommended action:** delist chronically low-margin SKUs unless they are proven loss leaders (a SKU sold deliberately at a loss to drive profitable companion purchases — acceptable only if overall basket profitability stays positive).

## Recommendations Summary

| Focus Area | Action | Expected Impact |
|---|---|---|
| Evergreen vendors | Scale via continuous marketing; negotiate exclusive SKUs | Evergreen sales +20–25%, reducing Q4 dependency |
| Seasonal vendors | Secure inventory 8–10 weeks pre-November; early-order discounts; concentrated campaigns | Maximized Q4 margin contribution without early capital strain |
| Low-margin vendors (Provocraft) | Test price increases on low-elasticity SKUs; renegotiate terms | Margin improvement of 2–4 percentage points |
| SKU discipline | Delist chronically low-margin SKUs unless proven loss leaders | Protects November margins while preserving profitable volume |

## Data Source

Data covers full-year 2024 and is provided across three linked tables:

| Table | Grain | Key fields |
|---|---|---|
| `Sales by Vendor and Dept by Day` | Daily, by department & vendor | Date, Department, Vendor Name, Total Sales Demand, Total Margin Demand, Total Sales Units Demand, Average Order Value |
| `Sales by SKU by Day` | Daily, by individual SKU | SKU Desc, SKU ID, Date, Department, Vendor Name, Total Sales Demand, Total Margin Demand, Total Sales Units Demand, Average Order Value |
| `Additional Sales and Margin` | Daily, by department | Department, Date, Sales, Margin |

## Dashboard Interactivity

The Tableau workbook (`.twbx`) uses linked actions across its dashboards, including:
- **Filter actions** connecting the department/vendor bubble charts to detail views
- **Hover actions** on the price-vs-margin trend line, surfacing SKU-level tooltips (loss period and price change)

## Repository Contents

| File | Description |
|---|---|
| `A1_-_Data_Visualization--SimoncelliAlessandro.pptx` | 5-slide executive presentation plus appendix of dashboard screenshots |
| `A1_-_Data_Visualization_-_Simoncelli_Alessandro.twbx` | Tableau Packaged Workbook — interactive dashboards with the data extract embedded (open in Tableau Desktop or Tableau Reader) |
| `README.md` | This file — project summary, analysis walkthrough, and data documentation |

## How to Explore

1. Open the `.twbx` in [Tableau Desktop](https://www.tableau.com/products/desktop) or the free [Tableau Reader](https://www.tableau.com/products/reader) to interact with the dashboards (filter by vendor, department, or month; hover for SKU detail).
2. Open the `.pptx` for the full executive narrative and appendix.
3. *(Optional)* Add your video walkthrough link here once uploaded: `[Video presentation](your-youtube-link)`

## Author

**Alessandro Simoncelli**
Hult International Business School — Master in Management / Master in Finance
