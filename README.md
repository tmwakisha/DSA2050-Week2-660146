# DSA 2050 Week 2 Practical Lab

**Student:** Tamara Mwakisha  
**Student ID:** 660146

## Objective
Complete the practical on source inspection, SQL, key checks, joins, reconciliation, segment KPIs, and the JSON region lookup.

## Findings
1. CustomerID C004 occurs twice. The original join returned 16 rows instead of 15 and increased sales from Ksh. 113,500 to Ksh. 122,600 because O005 was repeated.
2. The cleaned join returned 15 rows and Ksh. 113,500 in sales. Order O015 for C999 remains unmatched and is worth Ksh. 9,900.
3. Electronics had the highest category sales at Ksh. 51,500. Corporate had the highest segment sales at Ksh. 46,800. Nairobi had the highest identified regional sales at Ksh. 39,800.

## Files
1. `DSA2050_Week2_SQL_Lab.ipynb` contains the practical sections and answers.
2. `customers.csv`, `orders.csv`, and `regions.json` contain the source data.

## Run
Open the notebook in Jupyter or VS Code. Restart the kernel and run all cells from top to bottom.
