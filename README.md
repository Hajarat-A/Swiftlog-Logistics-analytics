# SwiftLog Logistics Analytics & Business Intelligence

## Project Overview

**SwiftLog Logistics Analytics** is a business intelligence project developed as part of the **AnalystLab Africa Experience Lab**. Using Microsoft Power BI, the project analyses sales, customers, products, inventory, warehouses, returns, and shipment performance to turn operational data into insights that can support management decision-making.

The report is designed for executive and operational audiences. It provides an overview of commercial performance while highlighting delivery reliability and order fulfilment as priority areas for improvement.

## Business Objectives

- Monitor overall sales and order performance.
- Identify high-value customers and leading products.
- Compare revenue across product categories and cities.
- Review inventory and warehouse indicators.
- Measure shipment timeliness and delivery delays.
- Understand the main reasons for product returns.
- Translate findings into practical business recommendations.

## Tools and Technologies

- **Power BI** — data modelling, DAX measures, interactive report pages, and visualisations.
- **Power Query** — data profiling, transformation, and cleaning.
- **Excel and CSV files** — initial data review and source data preparation.

## Data Overview and Preparation

The project uses multiple datasets covering customers, orders, order items, products, inventory, shipments, delivery performance, returns, suppliers, warehouses, and employees.

Data preparation included reviewing data types, missing values, duplicates, identifier fields, and relationships between tables. Date attributes, including month and quarter, were prepared for time-based analysis, and a dedicated date table was created.

### Dataset Summary

| Dataset | Records / Notes |
|---|---:|
| Orders | 5,000 rows; no missing values or duplicate order IDs reported |
| Order Items | 15,000 rows |
| Products | 250 products |
| Shipments | 5,000 rows |
| Returns | 500 records |
| Suppliers | 150 records |
| Inventory | 4,000 rows initially; 3 duplicate rows removed, leaving 3,997 rows |
| Warehouses | 15 records after the header was correctly applied |
| Customers | Included in the source data |
| Delivery Performance | Included in the source data |
| Employees | Included in the source data |

### Data Modelling Notes

- Supplier data did not have a direct relationship to Products or Shipments in the supplied data. Supplier-level conclusions are therefore limited to the available fields and relationships.
- Warehouse capacity was not provided. Warehouse analysis uses available stock and transaction indicators rather than a direct capacity-utilisation measure.
- The analysis uses the supplied data and the relationships established for the report. Any patterns observed should be treated as areas for further investigation rather than proof of causation.

## Power BI Report Pages

The report contains **seven pages**. The main analytical pages include:

1. **Executive Dashboard** — high-level KPIs and monthly trends.
2. **Customer Analysis** — leading customers, customer value by city, and category revenue.
3. **Inventory & Warehouse** — inventory and warehouse indicators.
4. **Supplier & Product** — category revenue, top products by revenue, and products requiring stock attention.
5. **Shipment & Delivery Analysis** — shipment timeliness, delays, and delivery performance.
6. **Warehouse Details** — additional warehouse-level analysis.

The report also includes a returns-reason visual. Page navigation and report-page tooltips help users move between report views and inspect product details.

## Key Metrics and Findings

### Executive KPIs

| Metric | Result |
|---|---:|
| Total orders | 5,000 |
| Total shipments | 5,000 |
| Total units sold | 82K |
| Total products | 250 |
| Average order value | 4.33K |
| Average delivery delay | 3.57 days |
| Delayed shipments | 3,186 |
| Delayed shipment rate | 63.72% |
| On-time shipments | 1,814 |
| On-time delivery rate | 36.28% |
| Total revenue | 21.67M |

*Dashboard values are shown using rounded labels where applicable.*

### Revenue by Product Category

| Category | Revenue |
|---|---:|
| Fashion | 8.06M |
| Food | 7.11M |
| Electronics | 6.50M |

Fashion generated the highest revenue among the three categories, followed by Food and Electronics.

### Revenue by City

The dashboard shows the following approximate city-level revenue:

| City | Approximate Revenue |
|---|---:|
| Kano | 5.7M |
| Lagos | 5.5M |
| Abuja | 5.2M |
| Ibadan | 5.2M |

Kano ranks first, followed by Lagos. Abuja and Ibadan have similar revenue, with Ibadan slightly lower in the displayed visual.

### Customer Value

The top revenue-generating customer visual identifies:

| Customer | Approximate Revenue |
|---|---:|
| Customer 263 | 74K |
| Customer 815 | 70K |
| Customer 512 | 70K |
| Customer 223 | 69K |
| Customer 597 | 65K |

These customers may warrant retention-focused engagement. Management should also assess whether revenue depends disproportionately on a small group of customers before deciding on a specific retention strategy. Repeat-purchase analysis could help evaluate customer retention opportunities.

Average revenue per customer by city is approximately 22K for Lagos, Kano, and Abuja, and 20K for Ibadan.

### Product Performance

The top products by revenue include:

| Product | Approximate Revenue |
|---|---:|
| P040 | 191K |
| P085 | 187K |
| P186 | 181K |
| P234 | 180K |

These products are candidates for closer review of demand, profitability, stock availability, and sales trends.

### Shipment and Delivery Performance

Of 5,000 shipments:

- **3,186 were delayed**, representing **63.72%**.
- **1,814 were on time**, representing **36.28%**.
- The average delivery delay was **3.57 days**.

The high delayed-shipment rate makes delivery reliability the clearest immediate operational priority. City-level analysis also identified Lagos as having the highest delayed-shipment volume (**1,701**) and a delayed-shipment rate of **64.26%**.

### Returns Analysis

The dashboard reports 500 returns:

| Return Reason | Count | Share |
|---|---:|---:|
| Late Delivery | 185 | 37.0% |
| Wrong Item | 163 | 32.6% |
| Damaged | 152 | 30.4% |
| **Total** | **500** | **100%** |

Late Delivery is the most frequently recorded return reason, followed by Wrong Item and Damaged. The findings indicate that delivery reliability, fulfilment accuracy, and product handling should all be considered in a returns-improvement programme.

## Recommendations

1. **Improve delivery reliability.** Investigate the causes of delays, monitor on-time delivery and average delay, and prioritise locations with high delayed-shipment volumes or rates.
2. **Improve fulfilment accuracy and product handling.** Track Wrong Item and Damaged returns and review the fulfilment processes associated with them.
3. **Retain high-value customers.** Monitor repeat purchases and customer retention, and investigate opportunities to improve engagement with valuable customer segments.
4. **Use category performance to guide decisions.** Investigate category demand, profitability, and sales trends before changing inventory or marketing allocation.
5. **Strengthen inventory visibility.** Use available warehouse-stock indicators to support replenishment and stock-allocation decisions.
6. **Track improvement with KPIs.** Monitor delivery performance, return reasons, customer retention, revenue, and inventory indicators over time.

## Limitations and Interpretation

- **Incomplete September data:** The dashboard notes that September 2026 data is available through 8 September. Monthly comparisons involving September should be interpreted accordingly.
- **Warehouse capacity:** Capacity data was not provided, so capacity utilisation cannot be calculated directly from the supplied data.
- **Supplier relationships:** The supplied datasets do not provide a direct relationship from Suppliers to Products or Shipments. Supplier-level conclusions should remain within the available fields and relationships.
- **Correlation and causation:** Observed patterns are investigation areas, not proof of causation.
- **Rounded values:** Revenue and average-value figures use rounded dashboard labels. Tables and narrative summaries therefore use approximate values where appropriate.

## Conclusion

The analysis identifies delivery reliability as SwiftLog's most urgent operational issue. At the same time, customer retention and growth in high-performing product categories offer commercial opportunities. Management should use clearly defined KPIs to track improvements and combine shipment, returns, customer, product, and inventory insights when setting priorities.

## Project Structure

```text
Swiftlog-Logistics-analytics/
├── Dashboard/
│   └── Swiftlog_Analytics.pbix
├── Data/
│   ├── SwiftLog_Customers.csv
│   ├── SwiftLog_Data_Dictionary.csv
│   ├── SwiftLog_Delivery_Performance.csv
│   ├── SwiftLog_Employees.csv
│   ├── SwiftLog_Inventory.csv
│   ├── SwiftLog_Order_Items.csv
│   ├── SwiftLog_Orders.csv
│   ├── SwiftLog_Products.csv
│   ├── SwiftLog_Returns.csv
│   ├── SwiftLog_Shipments.csv
│   ├── SwiftLog_Suppliers.csv
│   └── SwiftLog_Warehouses.csv
├── Presentation/
│   └── Executive_Presentation.pptx
├── References/
│   └── References.md
├── Report/
│   ├── Swiftlog_Dashboard_Screenshots.pdf
│   └── SwiftLog_Executive_BI_Report.pdf
└── README.md
```

## Project Deliverables

- Power BI interactive dashboard (`.pbix`)
- Executive BI report (`.pdf`)
- Dashboard screenshots (`.pdf`)
- Executive presentation (`.pptx`)
- Source datasets and data dictionary (`.csv`)
- Reference documentation (`References.md`)

## Project Context

Developed as part of the **AnalystLab Africa Experience Lab**, this project demonstrates practical application of data preparation, data modelling, KPI development, dashboard design, and business-focused analytical storytelling using Power BI.
