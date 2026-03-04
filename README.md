# Post-Acquisition Data Unification & Executive Sales Intelligence Dashboard

## 1. Business Context

Atlon, a mature sports equipment manufacturer operating on structured ERP systems, acquired Sports Bar — a high-growth nutrition startup.

### The Challenge:

- Disparate data systems  
- Inconsistent formats  
- Missing historical records  
- Conflicting revenue definitions  
- Misaligned reporting cycles  
- No unified supply chain view  

Leadership chose to preserve the startup’s culture and autonomy, which increased integration complexity.

### Operational Risk:

Without a reliable data layer, forecasting, inventory planning, and executive decision-making would be compromised.

---

## 2. Objective

Design and implement a scalable, unified data foundation in Databricks Free Edition to:

- Normalize denormalized source data
- Align metrics across entities
- Repair incomplete time series
- Standardize channel & customer structures
- Deliver executive-grade dashboards

---

## 3. Architecture Approach

### Medallion Architecture

#### Bronze Layer  
- Raw ingestion of denormalized CSV  
- Schema inference  
- Basic validation  

#### Silver Layer  
- Data cleansing  
- Date normalization  
- Revenue recalculation validation  
- Channel standardization  
- Customer deduplication  

#### Gold Layer  
- Fact table: Sales transactions  
- Dimensions: Date, Customer, Product, Channel  
- Derived KPIs (growth %, share %, concentration ratios)  

---

## 4. Key Metrics Built

### Revenue Metrics:
- Total Revenue
- Revenue by Channel
- Revenue Share %
- MoM Growth %
- YoY Growth %

### Customer Metrics:
- Active Customers
- Customer Concentration Ratio (Top 1, 5, 10)
- Revenue per Customer
- Transaction Frequency

### Product Metrics:
- Top 10 Products by Revenue
- Revenue Distribution

### Operational Signals:
- Average Selling Price
- Average Order Value
- Volume vs Revenue trend comparison

---

## 5. Executive Insights Derived

### Revenue Structure

- 78% revenue driven by Retail channel  
- 20% via Direct  
- Acquisition channel newly launched  

Business remains structurally retail-dependent.

---

### Customer Risk

- Largest customer: ~9%  
- Top 5: ~33%  
- Top 10: ~60%  
- 52 active customers drive 105B+ revenue  

Indicates moderate clustering but no single point of failure.

---

### Growth & Momentum

- Revenue shows steady upward trend through 2025  
- Late-year spike likely tied to expansion or seasonal demand  
- Acquisition channel exhibits volatility due to early-stage implementation  

---

### Strategic Position

The business is:

- Stable
- Retail-heavy
- Moderately concentrated
- Experimenting with diversification
- Operationally scalable

However:

Margin visibility, retention analysis, and inventory linkage remain future priorities.

---

## 6. Risks Identified

- Channel dependency on retail
- Moderate customer clustering
- Product concentration risk
- New channel volatility
- Limited profitability view

---

## 7. Key Learnings

1. Post-acquisition integration is more about clarity than consolidation.
2. Revenue dashboards without concentration analysis are incomplete.
3. Share % without growth % misleads.
4. Early-stage channel data should not be overinterpreted.
5. Executive dashboards must balance structure, momentum, and risk.

---

## 8. Future Enhancements

- Contribution margin by channel
- Repeat purchase analysis
- Customer lifetime value
- Inventory turnover integration
- Supply chain forecasting alignment

---

## Conclusion

This project demonstrates how a structured data engineering approach can convert fragmented, post-acquisition chaos into executive-ready intelligence.

Before transformation comes truth.

This was about building that truth layer.
"""
