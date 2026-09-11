fabric-medallion-demo
│
├── data
│
│   ├── customers_raw.csv
│   ├── orders_raw.csv
│   ├── products_raw.csv
│   └── marketing_raw.csv
│
└── README.md

FABRIC MEDALLION DATASET
BRONZE: Load all CSVs as-is into Delta tables.
SILVER: Deduplicate by latest _load_ts; cast types; standardize values; validate null/range/date; check referential integrity; write bad records to rejects.
GOLD: Create dim_customer, dim_product, dim_date, fact_sales, fact_marketing.
KPIs: Net Revenue, Total Orders, AOV, Top Products, CLV, Revenue by Region, Marketing ROI.
