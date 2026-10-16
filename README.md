# data-science-project
# Monthly Visitor Arrivals and Hotel Room Occupancy in Macao, 2024–2025
Data Science Project for CISC7204

## Research Question
Is there a statistically significant positive association between monthly visitor arrivals and the average hotel room occupancy rate in Macao from January 2024 to December 2025? Do months with more arrivals tend to have higher occupancy?

## Dataset Source and Usage Permissions
Two datasets are obtained from the **Statistics and Census Service (DSEC), Government of the Macao SAR**, open official public statistics.
- Visitor Arrivals: shturl.cc/MxKYg0cqMbvJSpVMOwU1AKG4woOfJoB3phgv9YK6bQ9TmMgphfPWsUk974amTA7‑US
- Hotel Occupancy Rate: https://www.dsec.gov.mo/statistic.aspx?lang=en-us

Supplied source files:
- `visitor‑arrivals.xls` : Monthly total visitor arrivals (number of persons)
- `hotel‑occupancy.xlsx` : Monthly average hotel room occupancy rate (percentage %)

Time filter: January 2024 ‑ December 2025 (24‑month observations).
These public datasets are permitted for academic study and non‑commercial analysis.

## Methods and Tools
**Tools**: Python, Pandas, Matplotlib, SciPy.
1. Load original `.xls` / `.xlsx` spreadsheets.
2. Parse date‑month labels, filter records to 2024‑01 to 2025‑12.
3. Merge two datasets by month, check missing values, duplicates and out‑of‑range entries.
4. Compute descriptive statistics, Pearson correlation coefficient and two‑sided p‑value.
5. Generate time‑series dual‑axis line chart and scatter plot with fitted regression line for visual exploration.

## Key Findings and One Limitation
### Key Findings
After merging, 24 complete monthly records are obtained with no missing months.
Monthly visitor arrivals range from 2 528 011 to 4 219 034 people. Hotel occupancy ranges from 82.8 % to 93.1 %. Both variables peak in August 2025.

Pearson correlation result: **r = 0.823, n=24, p < 0.001, R² = 0.678**.
There exists a **strong statistically significant positive association**: months with higher visitor arrivals generally correspond to higher hotel room occupancy. 17 out of 23 month‑to‑month changes move in the same direction.

### Limitation
This analysis shows correlation instead of causation. It does not control for confounding factors including seasonality, hotel room supply, special local events, and proportion of same‑day visitors. Monthly time‑series observations may also be autocorrelated.

## Instructions for running the analysis
1. Clone this repository
2. Install dependencies: pip install -r requirements.txt
3. Open the .ipynb notebook and run cells sequentially.
