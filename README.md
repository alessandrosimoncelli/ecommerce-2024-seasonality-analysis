# 2024 E-Commerce Performance Analysis: Seasonality & Margin Erosion

Executive data visualization project analyzing 2024 e-commerce performance for a nationally recognized retailer, built for a five-slide executive presentation backed by an interactive Tableau dashboard.

**Assignment:** A1, Executive Presentation: Data-Driven e-Commerce Strategy & Recommendations
**Institution:** Hult International Business School
**Author:** Alessandro Simoncelli

## The Brief

Acting as the executive overseeing e-Commerce, the task was to analyze the retailer's 2024 performance and deliver 3 to 4 data-backed recommendations to drive sales and profitability, communicated through:
- A 5-slide executive presentation, plus an appendix of dashboard screenshots
- An interactive Tableau dashboard using at least two linked actions (filter, hover, or interactive reference lines)

## Key Findings

| Metric | Value |
|---|---|
| Total 2024 sales | $64M |
| Overall profit margin | 29% |
| Revenue share from November | 32% |
| Technology dept. share of total sales | 27% |
| Greenery/Naturals margin | 35%+ |
| November median price drop | -41% ($14.30 to $8.50) |
| November margin (Technology) | 15-20% down to -4% |
| Share of total losses from Provocraft | 78% |

## Analysis Walkthrough

### 1. The headline number hides a concentration risk
2024 closed at $64M in sales and a healthy 29% overall margin, but 32% of annual revenue lands in a single month, November. That concentration is already a real operational and financial risk, and it looks worse up close: profit margin actually falls as sales spike in November. The business is trading margin for volume through aggressive Black Friday discounting, and that trade-off is eroding profitability rather than just shifting it across the calendar.

### 2. Where the November dependency comes from: department positioning
Each department was mapped on margin versus sales volatility (standard deviation of monthly sales, used as a seasonality proxy), with bubble size representing 2024 sales volume.
- Technology is the largest department, 27% of total sales, sitting in low-volatility, modest-margin territory (around 10%).
- Greenery/Naturals delivers margins above 35% but with sales heavily concentrated in Q4. It's a genuine profit engine, but one that needs precise inventory timing to execute well.
- Seasonal departments in general are what drive the November peak.

### 3. Where to focus: vendor portfolio action plan
The same framework applied at vendor level, filtered to vendors selling at least one unit every month, splits the portfolio into four groups:
- Evergreen performers (Unique, Macarons) run around 45% margins, stable year-round. Action: scale with continuous marketing and negotiate exclusive SKUs. Target is +20 to 25% evergreen sales, reducing Q4 dependency.
- Seasonal profit engines (Mr. Christmas, National Tree) also run around 45% margins but are concentrated in Q4. Action: secure inventory 8 to 10 weeks before November, negotiate early-order discounts, run concentrated campaigns.
- Low-margin, consistent vendors (Provocraft) need a different approach: test price increases on low-elasticity items, or renegotiate terms.
- High-risk seasonal vendors: none identified, which points to good existing portfolio discipline.

### 4. What went wrong: negative-margin SKUs
Losses are concentrated in November, exactly when discounting is heaviest. The critical finding is that 78% of total annual losses trace back to a single vendor, Provocraft, which makes up the majority of the Technology department. A SKU-level treemap, color-coded by margin, isolates the worst offenders. SKU D204420S alone lost $170,000, and D036142S lost $48,000 at a less severe margin.

### 5. Root cause: the November pricing collapse
Within Technology, median price held near $14 from January to October, then fell 41% to $8.50 in November. Margin followed the same path: a healthy 15-20% all year, collapsing to -4% in November. An interactive tooltip in the Tableau dashboard drills into individual SKUs to show exactly when losses occurred and how far price dropped.

The findings: many November negative-margin SKUs were already near 0% margin before Black Friday even started. The extra discount is what pushes those already weak products into outright losses.

Recommended action: delist chronically low-margin SKUs unless they are proven loss leaders (a SKU sold deliberately at a loss to drive profitable companion purchases, acceptable only if overall basket profitability stays positive).

## Recommendations Summary

| Focus Area | Action | Expected Impact |
|---|---|---|
| Evergreen vendors | Scale via continuous marketing, negotiate exclusive SKUs | Evergreen sales +20-25%, reducing Q4 dependency |
| Seasonal vendors | Secure inventory 8-10 weeks before November, early-order discounts, concentrated campaigns | Maximized Q4 margin contribution without tying up capital early |
| Low-margin vendors (Provocraft) | Test price increases on low-elasticity SKUs, renegotiate terms | Margin improvement of 2-4 percentage points |
| SKU discipline | Delist chronically low-margin SKUs unless proven loss leaders | Protects November margins while keeping the volume that's actually profitable |

## Data Source

Data covers full-year 2024 across three linked tables:

| Table | Grain | Key fields |
|---|---|---|
| Sales by Vendor and Dept by Day | Daily, by department and vendor | Date, Department, Vendor Name, Total Sales Demand, Total Margin Demand, Total Sales Units Demand, Average Order Value |
| Sales by SKU by Day | Daily, by individual SKU | SKU Desc, SKU ID, Date, Department, Vendor Name, Total Sales Demand, Total Margin Demand, Total Sales Units Demand, Average Order Value |
| Additional Sales and Margin | Daily, by department | Department, Date, Sales, Margin |

## Dashboard Interactivity

The Tableau workbook (.twbx) uses linked actions across its dashboards, including:
- Filter actions connecting the department and vendor bubble charts to detail views
- Hover actions on the price-vs-margin trend line, surfacing SKU-level tooltips with the loss period and price change

## Repository Contents

| File | Description |
|---|---|
| `ecommerce-2024-executive-presentation.pptx` | 5-slide executive presentation (overview, department strategy, vendor action plan, loss analysis, pricing collapse) plus an appendix of dashboard screenshots |
| `ecommerce-2024-seasonality-dashboard.twbx` | Tableau Packaged Workbook with the interactive dashboards and embedded data extract; includes filter and hover actions across department, vendor, and SKU views |
| `README.md` | Project summary, analysis walkthrough, and data documentation |

## How to Explore

1. Open `ecommerce-2024-seasonality-dashboard.twbx` in Tableau Desktop or the free Tableau Reader to interact with the dashboards (filter by vendor, department, or month; hover for SKU detail).
2. Open `ecommerce-2024-executive-presentation.pptx` for the full executive narrative and appendix.

## Author

Alessandro Simoncelli
