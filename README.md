# Retail Executive Summary Dashboard
An executive-level retail analytics project built with **Databricks SQL** and **Power BI**. It turns transaction-level sales data into summary tables and a one-page dashboard.

## Business Objective
Give C-suite executives a quick, non-technical view of business health across sales, customers, loyalty, geography and products, so they can make data-driven decisions.

## Tools Used
- Databricks (Silver and Gold layers, SQL)
- Power BI Desktop (DAX, dashboards)
- Jupyter/Databricks Notebook (documentation)

## Data Model
| Layer | Table | Purpose |
|---|---|---|
| Silver | `workspace.silver.sales` | Line-item sales data (source) |
| Gold | `workspace.gold.tbl_exec_sum_kpi_met` | KPIs with 3M and 6M comparisons |
| Gold | `workspace.gold.tbl_exec_sum_attributes_agg` | Sales by product, region, city, tier, payment |
| Gold | `workspace.gold.tbl_exec_sum_monthly_agg` | Monthly trend (12 months x loyalty segment) |

## Dashboard Highlights (Last 12 Months)
- **Total sales:** 895.29M, up 36.8% (last 3M vs previous 3M)
- **Loyalty sales:** 497.34M, about 55.5% of total sales
- **Top region:** North (27% of sales)
- **Top store format:** Supermarket (71.4% of sales)
- **Top payment method:** UPI (46.4%)
- **Top loyalty tier:** Silver (74.8% of loyalty sales)
- **Category insight:** 16 categories drive ~80% of sales

## Key Techniques
`COUNT(DISTINCT)`, `try_divide()`, `date_trunc()`, `add_months()`, `GROUP BY ALL`, `CASE WHEN`, DAX (MoM % and YoY %)

## Repository Structure
```
docs/        -> Business Requirements Document (notebook)
dashboard/   -> Power BI executive summary (PDF)
images/      -> Dashboard preview screenshot
sql/         -> Gold table SQL (coming soon)
```
## How to View
1. Open `docs/01_executive_summary_brd.ipynb` for requirements and table specs.
2. Open `dashboard/executive_summary_dashboard.pdf` for the final report.

## Data Notice
Data shown is for portfolio/demo purposes. No confidential or personal data is included

## Author
Nishant Pal
