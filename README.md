SwiftLog Logistics Analytics & Business Intelligence
Project Overview
SwiftLog Logistics Analytics is a business intelligence project
developed as part of the AnalystLab Africa Experience Lab. It uses Power
BI to analyse sales, customers, products, inventory, warehouses,
returns, and shipment performance, turning operational data into
insights that can support management decisions.

The report is designed for executive and operational audiences. It
highlights commercial performance while identifying delivery reliability
and fulfilment as priority areas for improvement.
Business Objectives
- Monitor overall sales and order performance.
- Identify high-value customers and leading products.
- Compare revenue across product categories and cities.
- Review inventory and warehouse indicators.
- Measure shipment timeliness and delivery delays.
- Understand the main reasons for product returns.
- Translate findings into practical business recommendations.
Tools Used
- Power BI --- data modelling, DAX measures, interactive report
  pages, and visualisations.
- Power Query --- data profiling, transformation, and cleaning.
- Excel / CSV source files --- initial data review and
  preparation.
Data Overview
The project uses multiple related datasets covering customers, orders,
order items, products, inventory, shipments, delivery performance,
returns, suppliers, warehouses, and employees.

Dataset preparation included checking data types, missing values,
duplicates, identifier fields, and relationships between tables. Date
attributes, including month and quarter, were prepared for time-based
analysis, and a dedicated date table was created.
Data preparation notes
- Orders contained 5,000 rows and no missing values or duplicate order
  IDs.
- Order Items contained 15,000 rows.
- Products contained 250 products.
- Shipments contained 5,000 rows.
- Returns contained 500 records.
- Suppliers contained 150 records.
- Inventory contained 4,000 rows initially; three duplicate rows were
  removed, leaving 3,997 rows.
- Warehouse contained 15 records after the header was correctly
  applied.
- Supplier data did not have a direct relationship to Products or
  Shipments in the supplied data.
- Warehouse capacity was not provided, so warehouse analysis relies on
  available stock and transaction indicators rather than a direct
  capacity measure.
Power BI Report Pages
The report contains seven pages. The main pages include:
1. Executive Dashboard --- high-level KPIs and monthly trends.
2. Customer Analysis --- leading customers, customer value by city,
   and category revenue.
3. Inventory & Warehouse --- inventory and warehouse indicators.
4. Supplier & Product --- category revenue, top products by
   revenue, and products requiring stock attention.
5. Shipment & Delivery Analysis --- shipment timeliness, delays,
   and delivery performance.
6. Warehouse Details --- additional warehouse-level analysis.
The report also includes a returns-reason visual. Page navigation and
report-page tooltips are used to help users move between report views
and inspect product details.
Key Metrics and Findings
Executive KPIs
  Metric                        Result
  Total orders                   5,000
  Total shipments                5,000
  Total units sold                 82K
  Total products                   250
  Average order value            4.33K
  Average delivery delay     3.57 days
  Delayed shipments              3,186
  Delayed shipment rate         63.72%
  On-time shipments              1,814
  On-time delivery rate         36.28%
  Total revenue                 21.67M
Revenue by Product Category
  Category        Revenue
  Fashion           8.06M
  Food              7.11M
  Electronics       6.50M

Fashion contributes the highest revenue among the three categories,
followed by Food and Electronics.
Revenue by City
The dashboard shows the following approximate city-level revenue:

  City       Revenue
  Kano          5.7M
  Lagos         5.5M
  Abuja         5.2M
  Ibadan        5.2M

The chart places Kano first, followed by Lagos. Abuja and Ibadan are
close, with Ibadan slightly lower in the displayed visual.
Customer Value
The top revenue-generating customer visual identifies:
- Customer 263 --- approximately 74K
- Customer 815 --- approximately 70K
- Customer 512 --- approximately 70K
- Customer 223 --- approximately 69K
- Customer 597 --- approximately 65K
These customers may warrant retention-focused engagement. Management
should also assess whether revenue depends disproportionately on a
small group of customers before deciding on a specific retention
strategy. Repeat-purchase analysis can help evaluate customer retention
opportunities.

Average revenue per customer by city is approximately 22K for Lagos,
Kano, and Abuja, and 20K for Ibadan.
Product Performance
The top products by revenue include:
- P040 --- approximately 191K
- P085 --- approximately 187K
- P186 --- approximately 181K
- P234 --- approximately 180K
These products are useful candidates for closer review of demand,
profitability, stock availability, and sales trends.
Shipment and Delivery Performance
Of 5,000 shipments:
- 3,186 were delayed, representing 63.72%.
- 1,814 were on time, representing 36.28%.
- Average delivery delay was 3.57 days.
The high delayed-shipment rate makes delivery reliability the clearest
immediate operational priority. City-level analysis also identified
Lagos as having the highest delayed-shipment volume (1,701) and a
delayed rate of 64.26%.
Returns
The dashboard reports 500 returns:

  Return reason       Count      Share
  Late Delivery         185      37.0%
  Wrong Item            163      32.6%
  Damaged               152      30.4%
  Total         500   100%

Late Delivery is the most frequently recorded return reason, followed by
Wrong Item and Damaged. The results indicate that delivery reliability,
fulfilment accuracy, and product handling should all be considered in a
returns-improvement programme.
Recommendations
1. Improve delivery reliability. Investigate the causes of delays,
   monitor on-time delivery and average delay, and prioritise locations
   with high delayed-shipment volume or rates.
2. Improve fulfilment accuracy and product handling. Track Wrong
   Item and Damaged returns and review the fulfilment processes
   associated with them.
3. Retain high-value customers. Monitor repeat purchases and
   customer retention, and investigate opportunities to improve
   engagement with valuable customer segments.
4. Use category performance to guide decisions. Investigate
   category demand, profitability, and sales trends before changing
   inventory or marketing allocation.
5. Strengthen inventory visibility. Use available warehouse-stock
   indicators to support replenishment and stock allocation decisions.
6. Track improvement with KPIs. Monitor delivery performance,
   return reasons, customer retention, revenue, and inventory
   indicators over time.
Limitations and Interpretation
- September 2026 data is incomplete; the dashboard notes that data is
  available through 8 September. Monthly comparisons involving
  September should be interpreted accordingly.
- Warehouse capacity was not provided, so capacity utilisation cannot
  be calculated directly from the supplied data.
- The supplied datasets do not provide a direct relationship from
  Suppliers to Products or Shipments; supplier-level conclusions
  should stay within the available fields and relationships.
- Observed patterns are investigation areas, not proof of causation.
- Revenue and average-value figures are displayed using rounded labels
  in the dashboard. Tables and narrative summaries use approximate
  values where appropriate.
Conclusion
The analysis identifies delivery reliability as SwiftLog's most urgent
operational issue. At the same time, customer retention and growth in
high-performing product categories offer commercial opportunities.
Management should use clearly defined KPIs to track improvements and
combine shipment, returns, customer, product, and inventory insights
when setting priorities.

Swiftlog-Logistics-analytics/
│
├── Dashboard/
│   └── Swiftlog_Analytics.pbix
│
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
│
├── Presentation/
│   └── Executive_Presentation.pptx
│
├── References/
│   └── References.md
│
├── Report/
│   ├── Swiftlog_Dashboard_Screenshots.pdf
│   └── SwiftLog_Executive_BI_Report.pdf
│
└── README.md

