# SwiftLog Logistics Analytics & Business Intelligence

## Project Overview

**SwiftLog Logistics Analytics** is a business intelligence project developed as part of the **AnalystLab Africa Experience Lab**. Using Microsoft Power BI, the project analyses customers, orders, products, inventory, warehouses, returns, and shipment performance to support business decision-making.

The report provides an overview of commercial performance and highlights delivery reliability and order fulfilment as priority areas for improvement.

## Business Objectives

- Monitor sales and order performance.
- Identify high-value customers and leading products.
- Compare revenue across product categories and cities.
- Review inventory and warehouse indicators.
- Measure shipment timeliness and delivery delays.
- Understand the main reasons for returns.
- Translate findings into practical recommendations.

## Tools and Technologies

- **Microsoft Power BI** — data modelling, DAX measures, interactive report pages, and visualisations.
- **Power Query** — data profiling, transformation, and cleaning.
- **Excel and CSV files** — source data review and preparation.

## Data Overview and Preparation

The project uses 11 operational datasets covering customers, orders, order items, products, inventory, shipments, delivery performance, returns, suppliers, warehouses, and employees, along with a data dictionary.

Preparation included reviewing data types, missing values, duplicates, identifiers, and table relationships. Date attributes such as month and quarter were prepared for time-based analysis, and a dedicated date table was created.

### Dataset Summary

| Dataset | Records / Notes |
|---|---|
| Customers | 1,000 customer records |
| Orders | 5,000 rows; OrderID is unique |
| Order Items | 15,000 rows |
| Products | 250 products |
| Inventory | 4,000 rows retained for analysis |
| Shipments | 5,000 rows |
| Delivery Performance | 5,000 rows |
| Returns | 500 records |
| Suppliers | 150 records |
| Warehouses | 15 records after correcting the header row |
| Employees | 200 employee records |

### Data Modelling and Preparation Notes

- Repeated `WarehouseID`–`ProductID` combinations in Inventory were retained because they may represent separate inventory transactions or stock movements. Inventory visuals refer to **recorded stock quantity**, not a confirmed current stock balance.
- Supplier data has no direct relationship to Products or Shipments in the supplied data, limiting supplier-level conclusions.
- Warehouse capacity was not provided. Stock, product-range, staffing, and shipment measures are operational indicators, not direct capacity utilisation.
- Returns does not contain a ProductID, so returns cannot reliably be attributed to individual products when an order contains multiple items.
- The supplied order dates cover 2026. September data in the current dashboard is incomplete, with records available through 8 September.
- Observed patterns identify areas for investigation and do not, by themselves, prove causation.

## Power BI Report Pages

The report contains **five main analytical pages and two supporting interactive pages**.

### Main Analytical Pages

1. **Executive Dashboard** — high-level KPIs, monthly revenue and order trends, shipment status, and returns by reason.
2. **Customer Analysis** — leading customers, customer value by city, revenue by city, and category-related comparisons.
3. **Inventory & Warehouse** — recorded stock quantities, product range, warehouse shipment activity, staffing, and warehouse indicators.
4. **Shipment & Delivery Analysis** — shipment timeliness, delay rates, monthly shipment volume, and warehouse/location comparisons.
5. **Supplier & Product Analysis** — product revenue, revenue by category, and products with high recorded stock quantities.

### Supporting Interactive Pages

6. **Warehouse Details** — a drill-through page for examining warehouse-level shipment and delivery indicators.
7. **Product Details** — a tooltip page that displays additional product information when users hover over supported product visuals.

The returns-by-reason analysis is a visual on the Executive Dashboard, not a separate report page.

## Key Metrics and Findings

### Executive KPIs

| Metric | Result |
|---|---:|
| Total orders | 5,000 |
| Total shipments | 5,000 |
| Total customers | 1,000 |
| Total products | 250 |
| Total units sold | Approximately 82K |
| Total revenue | Approximately 21.67M |
| Average order value | Approximately 4.33K |
| Average recorded delivery delay | 3.57 days |
| Delayed shipments | 3,186 |
| Delayed shipment rate | 63.72% |
| On-time shipments | 1,814 |
| On-time delivery rate | 36.28% |

*The source data does not specify a currency, so monetary values are shown in the dataset's units. Dashboard values are rounded where applicable.*

### Revenue by Product Category

| Category | Approximate Revenue |
|---|---:|
| Fashion | 8.06M |
| Food | 7.11M |
| Electronics | 6.50M |

Fashion generated the highest revenue among the three categories, followed by Food and Electronics.

### Customer Value

The top revenue-generating customer visual includes:

| Customer | Approximate Revenue |
|---|---:|
| Customer 263 | 74K |
| Customer 815 | 70K |
| Customer 512 | 70K |
| Customer 223 | 69K |
| Customer 597 | 65K |

These customers may warrant closer review for retention opportunities. Repeat-purchase analysis would help assess customer retention and revenue concentration.

### Product Performance

Leading products by revenue include:

| Product | Approximate Revenue |
|---|---:|
| P040 | 191K |
| P085 | 187K |
| P186 | 181K |
| P234 | 180K |

These products are candidates for further review of demand, profitability, stock availability, and sales trends. Revenue alone does not establish product profitability.

### Shipment and Delivery Performance

Of 5,000 shipments, **3,186 (63.72%) were delayed** and **1,814 (36.28%) were on time**. The average recorded delivery delay was **3.57 days**.

The high delayed-shipment rate makes delivery reliability the clearest immediate operational priority. W05, W09, and W03 were among the warehouses with the highest delayed-shipment rates. Lagos had the highest delayed-shipment volume, with 1,701 shipments and a delayed-shipment rate of 64.26%.

### Returns Analysis

| Return Reason | Count | Share |
|---|---:|---:|
| Late Delivery | 185 | 37.0% |
| Wrong Item | 163 | 32.6% |
| Damaged | 152 | 30.4% |
| **Total** | **500** | **100%** |

Late Delivery is the most frequently recorded return reason, followed by Wrong Item and Damaged. Delivery reliability, fulfilment accuracy, and product handling should all be considered in a returns-improvement programme.

### Inventory and Warehouse Indicators

The inventory dataset contains 4,000 rows. The report compares recorded stock quantities and product coverage across 15 warehouses, alongside warehouse shipment volumes and employee counts. Since capacity and a verified current stock balance are not supplied, these measures should not be interpreted as direct capacity utilisation or definitive on-hand inventory.

## Recommendations

1. **Improve delivery reliability.** Investigate delay causes, monitor on-time delivery and average delay, and prioritise warehouses and locations with high delayed-shipment volumes or rates.
2. **Review warehouses with higher delay rates.** Start with W05, W09, and W03 and investigate possible workload, dispatch, routing, or other contributing factors.
3. **Improve delivery performance in Lagos.** Review the high volume and rate of delayed shipments and identify practical process improvements.
4. **Improve fulfilment accuracy and handling.** Track Wrong Item and Damaged returns and review picking, packing, and dispatch processes.
5. **Strengthen inventory visibility.** Review recorded stock movements and improve the data available to determine current balances and replenishment needs.
6. **Use category performance to guide decisions.** Assess demand, profitability, and sales trends before changing inventory or marketing allocation.
7. **Protect high-revenue products.** Monitor demand and stock availability for leading products while assessing profitability.
8. **Review high-value customer behaviour.** Monitor repeat purchases and retention to identify opportunities to maintain valuable customer relationships.
9. **Explore predictive delivery monitoring.** If additional historical and operational data becomes available, evaluate whether delay risks can be identified earlier.
10. **Establish supplier performance reporting when data is linked.** Capture supplier-to-product or supplier-to-shipment identifiers and relevant service measures before drawing supplier performance conclusions.
11. **Improve operational data collection.** Consider collecting warehouse capacity, dispatch and delivery timestamps, product-level return details, and supplier linkage fields.
12. **Monitor progress through Power BI.** Use consistent KPIs and regular reviews to assess changes in delivery, returns, customer, and inventory outcomes.

## Assumptions and Data Limitations

- **Currency:** The source data does not specify a currency. Revenue and average order value are reported in the dataset's units.
- **Inventory records:** Repeated warehouse–product combinations were retained as potentially meaningful transactions. Summed stock quantity is described as recorded stock quantity, not a verified current balance.
- **Warehouse capacity:** Capacity information is unavailable, so direct utilisation cannot be calculated.
- **Supplier relationships:** The supplier table has no direct relationship to Products or Shipments.
- **Returns detail:** Returns has no ProductID, limiting product-level return analysis.
- **Incomplete September:** September 2026 data is available only through 8 September in the current report and should not be compared with complete months without qualification.
- **Scope and causation:** Available order dates cover 2026. The analysis is descriptive and does not prove causes.
- **Rounded figures:** Some dashboard values are rounded and are presented as approximate values.

## Conclusion

The analysis identifies delivery reliability as SwiftLog's most urgent operational issue. Late delivery is also the largest recorded return reason. Customer value and category/product revenue patterns offer opportunities for further investigation. Management should use clearly defined KPIs to track improvements and combine shipment, returns, customer, product, and inventory insights when setting priorities.

## Suggested Project Structure

```text
SwiftLog-Logistics-Analytics/
├── Dashboard/
│   └── SwiftLog_Analytics.pbix
├── Data/
│   ├── SwiftLog_Customers.csv
│   ├── SwiftLog_Delivery_Performance.csv
│   ├── SwiftLog_Employees.csv
│   ├── SwiftLog_Inventory.csv
│   ├── SwiftLog_Order_Items.csv
│   ├── SwiftLog_Orders.csv
│   ├── SwiftLog_Products.csv
│   ├── SwiftLog_Returns.csv
│   ├── SwiftLog_Shipments.csv
│   ├── SwiftLog_Suppliers.csv
│   ├── SwiftLog_Warehouses.csv
│   └── SwiftLog_Data_Dictionary.xlsx
├── Presentation/
│   └── Executive_Presentation.pptx
├── References/
│   └── References.md
├── Report/
│   ├── Dashboard_Screenshots.pdf
│   └── SwiftLog_Executive_BI_Report.pdf
└── README.md
```

*The folder and file names above are suggested. Update them to match the names used in the actual repository.*

## Project Deliverables

- Power BI interactive dashboard (`.pbix`)
- Executive BI report (`.pdf`)
- Dashboard screenshots (`.pdf`)
- Executive presentation (`.pptx`)
- Source datasets and data dictionary
- README and reference documentation

## Project Context

Developed as part of the **AnalystLab Africa Experience Lab**, this project demonstrates practical application of data preparation, data modelling, KPI development, dashboard design, and business-focused analytical storytelling using Power BI.
