### FUTURE_DS_01
## 📊 Business Sales Performance Analytics
## Future Interns — Data Science & Analytics | Task 1

## 📌 Task Overview
1) Analyze business sales data to identify revenue trends, top-selling products, high-value categories, and regional/geographic performance
2) Present findings in a client-ready dashboard with actionable business recommendations.

## 📁 Dataset
Source: E-commerce Orders Dataset — Kaggle (Carrie1)
This is a real UK-based online retail dataset containing transactional records between December 2010 and December 2011. It includes invoice numbers, product descriptions, quantities, unit prices, customer IDs, and country of purchase.

## 🛠️ Tools Used
1) Microsoft Excel / CSV — initial data formatting and file conversion (dataset was too large as .xlsx, converted to .csv for Power BI ingestion)
2) Power BI Desktop — data transformation via Power Query, data modelling, and dashboard creation

## 🔧 Data Transformation Steps (Power Query)
The raw dataset required the following transformations before analysis:
1) Renamed tables for clarity and consistency
2) Changed data types: InvoiceNo and UnitPrice were converted from Text → Decimal Number
3) Fixed decimal formatting: Replaced . with , in the UnitPrice column to allow correct data type conversion (locale-based formatting issue)
4) Created a new Revenue column using the formula:
   Revenue = [UnitPrice] * [Quantity]

## 📊 Dashboard Pages
The Power BI dashboard consists of 4 report pages:
1) Analysis of Sales Trends Over Time
2) Top Products & Sales Performance
3) Are High Sales Driven by Volume or Price?
4) Geographic Performance

### 💡 Open Creating_Dashboard_-_Transforming_Data.pbix in Power BI Desktop to fully interact with the dashboard — hover over data points to see figures, filter by quarter/country, and explore the visuals dynamically.

## 🖼️ Dashboard Screenshots
## Page 1 — Analysis of Sales Trends Over Time
![Revenue Trends](screenshots/1_revenue_trends.png)
## Page 2 — Top Products & Sales Performance
![Top Products](screenshots/2_top_products.png)
## Page 3 — Are High Sales Driven by Volume or Price?
![Volume vs Price](screenshots/3_volume_vs_price.png)
## Page 4 — Geographic Performance
![Geographic Performance](screenshots/4_geographic_performance.png)

## 🔍 Key Insights
# 1. Sales Growth Over Time
- Revenue grew significantly from late 2010 into 2011, with total revenue reaching £9.0M by end of 2011.
- The strongest quarter was Q4 2011 at £3.72M (38.11% of total revenue), suggesting a strong seasonal pattern — likely driven by holiday/Christmas shopping.
- The weakest period was Q4 2010 at only £0.7M, reflecting the dataset's starting point with minimal sales history.
- Monthly spikes are visible in September and November 2011, indicating seasonal demand peaks.

# 2. Top Products by Revenue
- DOTCOM POSTAGE was the highest revenue-generating product (£206.25K, 2.45% of total), though this is a service/logistics item rather than a physical product — worth noting for business interpretation.
- REGENCY CAKESTAND 3 TIER was the top physical product by revenue at £92.36K.
- The lowest-selling product by revenue was CLASSIC GLASS COOKIE JAR.
- Revenue is highly fragmented across hundreds of SKUs, with the top product accounting for only ~2.45%, indicating no single product dominates sales.

# 3. Top Products by Quantity
- WORLD WAR 2 GLIDERS ASSTD DESIGNS had the highest units sold (~60K), yet does not appear in the top revenue products — indicating it is a low-price, high-volume item.
- JUMBO BAG RED RETROSPOT and ASSORTED COLOUR BIRD ORNAMENT also ranked high in quantity sold.

# 4. Volume vs. Price (Revenue Drivers)
- The scatter plot reveals that most high-revenue products achieve this through price rather than volume — items like DOTCOM POSTAGE and REGENCY CAKESTAND 3 TIER sit high on the revenue axis but not the quantity axis.
- High-volume, low-revenue items (top-right, near zero on revenue axis) such as WORLD WAR 2 GLIDERS are low-margin novelty products.
- Several negative revenue and quantity entries (e.g., "Manual", "Amazon Fee", "Damaged", "Unsaleable, destroyed") represent data quality issues / returns / adjustments that were retained in the dataset — in a production environment these would be filtered out or handled separately.

# 5. Geographic Performance
- The United Kingdom dominates overwhelmingly, generating £8.2M — approximately 87% of total revenue.
- International markets are significantly underdeveloped: the next largest markets are Netherlands and EIRE (Ireland) at £0.3M each, followed by Germany and France at £0.2M each.
- Australia stands out as a Southern Hemisphere anomaly at £0.1M — representing an unexpected market presence outside Europe.
- There is significant growth opportunity in European markets (Germany, France, Spain, Belgium, Sweden) that are currently underperforming relative to their market sizes.

## 💼 Business Recommendations
1) Capitalise on Q4 seasonality — Invest in inventory and marketing campaigns ahead of Q3/Q4 to capture the peak demand period, which accounts for over 38% of annual revenue.
2) Protect and grow the UK market while developing a structured international expansion strategy for Germany and France, which show early traction.
3) Investigate the Australia presence — understand how this market emerged and whether it can be scaled with targeted marketing or a local distribution partner.
4) Review postage/logistics pricing — DOTCOM POSTAGE being the top revenue line item may indicate shipping costs are being passed to customers in a way that inflates this category; this warrants a pricing strategy review.
5) Data hygiene — Implement cleaner transaction categorisation to separate legitimate sales from adjustments, returns, and damaged goods, which currently appear mixed in with product data.

## 📂 Repository Structure
```
FUTURE_DS_01/
│
├── README.md
├── data_-_4_Power_BI.xlsx                        *# Original Kaggle dataset (untransformed)*
├── Creating_Dashboard_-_Transforming_Data.pbix   *# Power BI dashboard file*
│
└── screenshots/
    ├── 1_revenue_trends.png
    ├── 2_top_products.png
    ├── 3_volume_vs_price.png
    └── 4_geographic_performance.png
```


