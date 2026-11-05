# Bike Buyers Analysis & Dashboard (Excel)

An Excel project that cleans a customer dataset, analyses which customers buy bikes, and presents the results in an interactive dashboard with slicers.

## Dataset
`bike_buyers` contains **1,026 customer records** with 13 columns: ID, Marital Status, Gender, Income, Children, Education, Occupation, Home Owner, Cars, Commute Distance, Region, Age and Purchased Bike (Yes/No).

## Tools
- Microsoft Excel: data cleaning, formulas (`IF`), PivotTables, PivotCharts, slicers

## Workbook structure
| Sheet | Contents |
|---|---|
| `bike_buyers` | Original raw data, kept unchanged |
| `Working sheet` | Cleaned copy of the data used for analysis |
| `Pivot Table` | PivotTables behind each chart |
| `Dashboard` | Final dashboard with charts and slicers |

## Steps

#### 1. Data cleaning
#### 2. Feature engineering
#### 3. PivotTables
#### 4. Dashboard

## Key findings
- **48%** of customers (481 of 1,000) bought a bike.
- **Buyers earn more on average:** about $58K versus $55K for non-buyers, for both men and women.
- **Short commutes buy more:** purchase rates are highest for 0–1 miles (55%) and 2–5 miles (59%), and lowest for 10+ miles (30%).
- **Middle-aged customers buy the most:** 55% of customers aged 31–54 bought a bike, compared with 35% of under-31s and 31% of those 55 and over.
- Other patterns: customers with **0–1 cars** (57–61%), **single** customers (54%) and the **Pacific** region (59%) have the highest purchase rates.

## Lessons learned
- **Always work on a copy:** keeping the raw sheet unchanged made it easy to compare and to start over if something went wrong.
- **Remove duplicates before analysing:** 26 duplicate rows would have inflated the counts.
- **Bins make patterns clearer:** grouping ages into brackets showed a clear trend that is hard to see age by age.
- **Slicers connected to several PivotTables** (via Report Connections) let one filter update the whole dashboard.
