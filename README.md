# aspiring-junior-data-analyst-portfolio
Superstore Sales Dataset

# Superstore Sales Dashboard (2015–2018)

An interactive Excel dashboard and written report that analyse four years of retail order data to show where sales come from, what is driving growth, and where the business should focus next.

# Screenshots of Superstore Sales Dashboard (2015–2018)

<img width="1366" height="768" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/c63e9aa2-0ade-474d-960b-8c8f253ef1af" />

<img width="1366" height="768" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/8fd3191c-8ab9-4098-855f-eb16cd9bcd88" />

<img width="1366" height="768" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/dd105edb-540e-4f82-b9d1-a6b8575642b0" />

<img width="1366" height="768" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/ecfe1cb1-dca8-4290-a938-eab3759ffa00" />


## 1. The Business Problem

Superstore sells furniture, office supplies and technology across the United States. Leadership needs to understand its sales performance, but the raw data is 9,800 order lines that are hard to read at a glance.

This project answers one main question: **where do Superstore's sales come from, what is driving growth, and where should the business focus next?**

It breaks that into seven specific questions:

1. Are we growing?
2. Where does the growth come from?
3. When do customers buy?
4. What do we sell?
5. Where do we sell?
6. Who buys from us?
7. How do we ship?

## 2. Tools Used

- **Microsoft Excel**: data cleaning, analysis and the dashboard itself
- **Excel Tables**: the cleaned data is stored as a structured table named `SalesData`
- **Pivot-style summary tables**: built with `SUMIFS`, `AVERAGEIFS` and `IFERROR` formulas, so they recalculate from the data
- **Data validation (dropdown)**: a year selector that updates the headline numbers and charts
- **Chart visualizations**: column, bar and line charts for sales by year, month, sub-category, region, segment, state and shipping mode
- **Data cleaning**: date conversion, duplicate removal, filling missing values and creating helper columns (Year, Month, Quarter, Ship Days)

## 3. Key Insights

- **Sales grew 51% from 2015 to 2018** ($480K to $722K), after a small dip in 2016 (−4%). Total sales were $2.26M.
- **Growth came from volume, not bigger orders.** Orders rose 75% and customers rose 17%, but the average order value fell 14% ($506 to $435).
- **Sales are highly seasonal.** Q4 brings 38.5% of annual sales, and September, November and December together bring 43%.
- **Sales are concentrated.** California and New York make up 33% of sales, and the top 20% of customers drive 48%.
- **Growth is uneven.** Corporate (+85%) and Home Office (+77%) grew far faster than Consumer (+25%), while the South region grew only 18% compared with 70% in the West.

## Data

- **Source:** Superstore sales dataset (`train.csv`)
- **Size:** 9,800 order lines, cleaned to 9,799 rows covering 4,922 orders and 793 customers
- **Period:** 3 January 2015 to 30 December 2018

### Data cleaning steps

- Converted dates from text to real dates
- Removed 1 duplicate row
- Filled 11 missing postal codes (all Burlington, Vermont) with 05401 (an assumption)
- Added Year, Month, Quarter and Ship Days columns
- Added three flag columns to count distinct orders and customers

## Repository contents

| File | Description |
| --- | --- |
| `Superstore_Excel_Dashboard.xlsx` | The dashboard, summary tables, cleaned data and a pivot table guide |
| `superstore_cleaned.csv` | The cleaned dataset |
| `Superstore Sales Performance 2015–2018 Dashboard Report.pdf` | The written report that explains the dashboard |

## How to use the dashboard

1. Open `Superstore_Excel_Dashboard.xlsx` and go to the **Dashboard** sheet.
2. Use the **Select year** dropdown (cell C3) to choose All, 2015, 2016, 2017 or 2018.
3. The headline numbers and charts update. The Sales by year chart always shows all four years.
4. The tables behind each chart are on the **Analysis** sheet, and the cleaned data is on the **Data** sheet.

## Limitations

- The data has sales only. It has no profit, quantity or discount, so the findings say nothing about profitability.
- The data covers four years, which limits how far long-term trends can be read.
- Large single orders (for example one copier worth $61.6K) can distort individual sub-categories.

## Next steps

- Add profit and discount data to see which products, regions and customers are actually profitable
- Build native PivotTables with slicers for Region and Segment
- Test the recommendations in the report, such as Q1 promotions and bundles to raise the average order value
