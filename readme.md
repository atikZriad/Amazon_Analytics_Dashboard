# Amazon Operations & Sales Analytics Dashboard

An Excel-based analysis of Amazon sales, product performance, order status, and fulfillment data. The project uses PivotTables, PivotCharts, slicers, and KPI calculations to turn transaction-level records into a practical business overview.

> **Business objective:** Understand where revenue is concentrated, how sales change over time, and what the order and fulfillment data can tell us about operational performance.

## Dashboard Preview

![Amazon sales and operations dashboard](screenshots/dashboard_overview.png)

Additional views:
- [Revenue by category](screenshots/revenue_category_analysis.png)
- [Cancelled orders by fulfillment](screenshots/cancellation_analysis.png)
- [Revenue by state](screenshots/top_states_analysis.png)

## Project at a Glance

| Item | Details |
|---|---|
| Tool | Microsoft Excel |
| Analysis | Sales revenue, product categories, geography, order status, fulfillment |
| Techniques | Data checks, PivotTables, PivotCharts, slicers, KPI calculations |
| Currency | Indian rupees (INR) |
| Main deliverable | Interactive Excel dashboard |

## Business Questions

- Which product categories contribute the most revenue?
- How does recorded revenue vary across the months represented in the dataset?
- Which shipping states contribute the most revenue?
- Which sizes and SKUs account for the most recorded sales or quantity?
- How many unique orders are represented, and what share have a cancelled status?
- How are cancelled orders distributed between Amazon and Merchant fulfillment?

## Key Metrics

The current dashboard reports the following figures for the workbook's current data and filter state:

| KPI | Value | Definition |
|---|---:|---|
| Total revenue | ₹76,034,406 | Sum of quantity multiplied by amount |
| Total orders | 120,378 | Distinct, nonblank Order IDs |
| Cancellation rate | 14.28% | Distinct cancelled Order IDs divided by distinct Order IDs |
| Average order value | ₹631.63 | Total revenue divided by distinct Order IDs |

## Findings

### Revenue is concentrated in a few categories
**Set** is the leading revenue category, followed by **Kurta**. This concentration is useful for prioritizing further investigation into product mix, availability, and campaign performance.

### Revenue varies across the observed months
The monthly PivotTable shows March as a partial month in the dataset, followed by higher recorded revenue in April, May, and June.

### A small group of states contributes substantial revenue
**Maharashtra** and **Karnataka** are among the leading states by recorded revenue. This pattern can inform further regional analysis, but the dashboard alone does not establish why these states perform strongly.

### Fulfillment and cancellations can be examined together
The cancellation pie chart shows the distribution of cancelled orders between Amazon and Merchant fulfillment. It describes each method's share of cancellations—not each method's cancellation rate.

### Product-level views support inventory questions
The workbook includes category, SKU, and size views. These can help identify where sales and quantities are concentrated and guide follow-up analysis of inventory allocation.

## Recommendations

1. **Review category concentration.** Investigate demand, margins, stock availability, and promotional activity for leading categories before making inventory or marketing changes.
2. **Investigate regional performance.** Examine order counts, product mix, and fulfillment patterns in leading states before allocating additional budget.
3. **Monitor cancellation patterns.** Separate cancellation counts, cancellation shares, and cancellation rates so each metric answers a clearly defined question.
4. **Use size and SKU views for follow-up analysis.** Combine quantity and revenue with stock and margin data if available before making replenishment decisions.

## Data

The repository contains:
- `Amazon Sale Report.csv` — source CSV dataset.
- `Amazon_Analytics_Dashboard.xlsx.xlsx` — Excel workbook containing the data sheet, PivotTables/charts, dashboard, and KPI helper sheet.
- `screenshots/` — dashboard and analysis screenshots.

### Method notes
- The dashboard's revenue KPI is calculated from quantity multiplied by amount; summing the raw Amount field alone gives a different total because some rows have a quantity of zero.
- Total orders are counted using distinct Order IDs rather than counting every product-level row.
- Repeated Order IDs can represent multiple product lines; they are not automatically duplicate records.
- Interpret results in light of the dataset's coverage and the workbook's active filters. Findings are descriptive and should not be treated as proof of causation.


## Repository Structure

```text
Amazon_Analytics_Dashboard/
├── Amazon Sale Report.csv
├── Amazon_Analytics_Dashboard.xlsx.xlsx
├── readme.md
└── screenshots/
    ├── cancellation_analysis.png
    ├── dashboard_overview.png
    ├── revenue_category_analysis.png
    └── top_states_analysis.png
```

## Author

**Atik Riad**  
Email: [azrofficial20@gmail.com](mailto:azrofficial20@gmail.com)  
LinkedIn: [Atik Zaman Riad](https://www.linkedin.com/in/atikzamanriad/)
