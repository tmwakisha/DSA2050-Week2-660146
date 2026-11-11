# DSA2050 Week 2 SQL Practical Lab

**Name:** Tamara Mwakisha  
**Student ID:** 660146

## Objective
This practical investigates retail customer and order data using pandas and SQLite. It demonstrates source inspection, grain and key validation, SQL filtering and aggregation, safe joining, row-count and total reconciliation, customer-segment KPIs, and integration of a JSON region lookup. The notebook preserves the intentionally duplicated customer key and unmatched order for investigation before applying a documented deduplication step.

## Three key findings
1. `C004` is duplicated in the customer table; its KSh 9,100 order is duplicated by the initial join, increasing the result from 15 to 16 rows and total sales from KSh 113,500 to KSh 122,600.
2. After retaining one `C004` record, the left join preserves all 15 orders and reconciles to KSh 113,500; unmatched order customer `C999` remains visible and contributes KSh 9,900.
3. Corporate has the highest known customer-segment sales (KSh 46,800); Nairobi has the highest identified-region sales (KSh 39,800). These are revenue-only results from a small dataset, not full profitability or performance measures.

## Files
- `DSA2050_Week2_SQL_Lab.ipynb` — executable practical and answers
- `customers.csv`, `orders.csv`, `regions.json` — source data
- `retail_lab.db` — generated SQLite database (recreated by notebook execution)
