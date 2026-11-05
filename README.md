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

### 1. Data cleaning
- Worked on a copy of the raw data (`Working sheet`) so the original stays untouched.
- **Removed 26 duplicate rows**, leaving 1,000 unique customers.
- Replaced short codes with full words for readability:
  - Marital Status: `M` → `Married`, `S` → `Single`
  - Gender: `M` → `Male`, `F` → `Female`
- Checked for missing values (none left in the cleaned data).

### 2. Feature engineering
Added an **Age Brackets** column with a nested `IF` formula:
```
=IF(L2>54,"old",IF(L2>=31,"middle age",IF(L2<31,"Adolescent","invalid")))
```
- Adolescent: under 31
- Middle age: 31–54
- Old: 55 and over

### 3. PivotTables
- Average income by gender, split by bike purchase
- Bike purchases by commute distance
- Bike purchases by age bracket
- Bike purchases by exact age

### 4. Dashboard
- **Bar chart:** average income per purchase, by gender
- **Line chart:** bike purchases by commute distance
- **Line chart:** bike purchases by age bracket
- **Line chart:** bike purchases by age
- **Slicers:** Marital Status, Region and Education filter all charts at once

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

## How to use
1. Download `Excel_Project_Dataset.xlsx`
2. Open it in Microsoft Excel and go to the `Dashboard` sheet
3. Use the slicers to filter by Marital Status, Region or Education

## Author
**Asli Ahmadova** · [GitHub](https://github.com/esliehmedova) · [LinkedIn](https://www.linkedin.com/in/esli-ehmedova09/)
