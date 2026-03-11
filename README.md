# 📊 Supply Chain Analytics
> End-to-end analytics project built on Snowflake + Power BI
> using Medallion Architecture across 6 business domains.

---

## 🎯 Business Problem
A medical supply company needed visibility into warehouse capacity, 
supplier performance, and customer profitability across 5 warehouses 
and 500 customers in Canada.

## 🔍 Key Findings
- 2 warehouses (North Distribution, Mountain View) operating above 
  90% capacity with no redistribution plan
- Short-term suppliers delivering 2.5× slower than long-term contracts 
  (27 days vs 11 days avg lead time)
- Top customers concentrated in High Value / High Discount quadrant — 
  margin at risk despite strong revenue

## 🛠️ Tech Stack
- **Snowflake** — data warehouse, Medallion Architecture
- **Power BI** — 6-page executive dashboard + DAX measures
- **SQL** — Bronze → Silver → Gold transformations

## 🏗️ Architecture
Raw CSV Files
     ↓
  BRONZE       ← Raw ingestion, no transformations, full audit trail
     ↓
  SILVER       ← Cleaned, deduplicated, joined across 6 domains
     ↓
   GOLD        ← 6 aggregated tables consumed by Power BI


## 📊 Dashboard Pages
| Page | Description |
|------|-------------|
| Overview | Revenue, margin, units, warehouse utilization KPIs |
| Inventory | Stock levels, reorder alerts, utilization by warehouse |
| Warehouse | Lead time, throughput, orders by location |
| Supplier | Contract type performance, SLA compliance |
| Customer | Segmentation matrix, LTV, industry breakdown |
| Insights | Executive summary + actionable recommendations |


## 💡 What I Learned
- Designing a proper Medallion Architecture from scratch
- Writing complex multi-table joins across 6 domains in Snowflake
- Translating data findings into executive-level business recommendations
