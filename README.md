# DSA2050 — Week 2 SQL Practical Lab

**Student:** Tamara Mwakisha  
**Student ID:** 660146  
**Repository:** `DSA2050-Week2-660146`

## Objective
This practical evaluates retail customer and order data using pandas and SQLite. It establishes each source's grain, inspects duplicate and unmatched keys, applies SQL selection and aggregation, and tests customer-order joins with row-count and sales reconciliation. A JSON region lookup is integrated only after the customer key is made unique. The intentionally problematic source records are retained and their analytical consequences are documented before correction.

## Key findings
1. `C004` is duplicated in the customer file. In the original left join, its `O005` order (`Ksh. 9,100`) is repeated, increasing output rows from 15 to 16 and sales from `Ksh. 113,500` to `Ksh. 122,600`.
2. The cleaned one-row-per-customer join returns 15 rows and reconciles to `Ksh. 113,500`. The unmatched order for `C999` remains in the result at `Ksh. 9,900` and is not assigned to a segment or region.
3. Electronics leads product-category sales (`Ksh. 51,500`); Corporate leads identified customer-segment sales (`Ksh. 46,800`); Nairobi leads identified-region sales (`Ksh. 39,800`). These revenue comparisons do not establish profitability or performance relative to market opportunity.

## Project files
- `DSA2050_Week2_SQL_Lab.ipynb` — section-by-section practical, SQL, formatted KPI tables, answers Q1–Q18, and conclusion.
- `customers.csv` — supplied customer-level source, including duplicate `C004`.
- `orders.csv` — supplied order-level source, including unmatched `C999`.
- `regions.json` — region code-to-name lookup.

## Run
Open the notebook in Jupyter or VS Code and run all cells from a clean kernel. Python, pandas, and SQLite are required. The notebook recreates `retail_lab.db` in its working directory.
