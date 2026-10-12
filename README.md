# Ecommere-Dashbaord

An interactive **Power BI dashboard** for exploring ecommerce sales, profitability, product performance, and customer purchasing patterns. The report brings key metrics and visual breakdowns together on a single page, with quarter and state filters for focused analysis.

## Project Objectives

- Monitor sales amount, profit, and units sold.
- Explore monthly changes in profitability.
- Compare sales contributions across states and customers.
- Analyze product categories and sub-categories.
- Understand the distribution of units sold by payment method.

## Dashboard Features

### KPI Cards

| Metric | Current report calculation |
| --- | --- |
| Total Sales Amount | Sum of `Details[Amount]` |
| Total Profit | Sum of `Details[Profit]` |
| Total Quantity | Sum of `Details[Quantity]` |
| AOV Field Total | Sum of `Details[AOV]` |

> **Metric note:** The current AOV card sums the existing `AOV` field. It should not be interpreted as a validated average order value without reviewing the underlying calculation and order granularity.

### Visual Analysis

| Visual | Purpose |
| --- | --- |
| Profit by Month — column chart | Explore monthly profitability patterns. |
| Profit by Sub-Category — bar chart | Compare profit contributions across product sub-categories. |
| Quantity by Category — donut chart | Examine each product category’s share of units sold. |
| Quantity by Payment Mode — donut chart | Compare units sold across payment methods. |
| Amount by State — donut chart | Explore the geographic distribution of sales amount. |
| Top Customer — column chart | Compare sales amount by customer. |

### Interactive Filters

- **Quarter slicer:** Explore performance by order-date quarter.
- **State dropdown:** Focus the analysis on a selected state.

## Data Structure

The report visuals reference two main tables:

| Table | Fields referenced in the dashboard |
| --- | --- |
| `Orders` | `Order Date`, `State`, `CustomerName` |
| `Details` | `Amount`, `Profit`, `Quantity`, `AOV`, `Category`, `Sub-Category`, `PaymentMode` |

These fields support time-based, geographic, customer, and product analysis. Review the model in Power BI Desktop for the complete schema, relationships, and calculation definitions.

## Tools and Skills

- **Microsoft Power BI:** Report authoring and interactive visualization.
- **Analytical reporting:** Sales and profitability analysis across multiple business dimensions.
- **Dashboard design:** KPI cards, column charts, bar charts, donut charts, and slicers.

## Repository Structure

```text
.
├── Ecommerce Dashboard.pbix    # Power BI report
└── README.md                   # Project documentation
