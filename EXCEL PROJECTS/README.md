# 📈 Excel Analytics & Business Intelligence Workbooks

## Overview
This folder contains end-to-end Microsoft Excel spreadsheet models, interactive sales dashboards, automated MIS reporting templates, and pivot analysis workbooks designed for operational and management decision-making.

---

## Workbook Inventory & Technical Details

| Workbook Name | Business Domain | Key Functions & Features | Formats / Components | Inspection Status |
| :--- | :--- | :--- | :--- | :--- |
| **`EMP_SALES_DASHBOARD .xlsm`** | Human Resources & Sales Management | Employee Sales KPIs, Monthly Performance Metrics, Dynamic Filters, VBA Macro Automations | Macro-Enabled Workbook (`.xlsm`) | Inspected Structure & Macros |
| **`MIS REPORT_ DATA.xlsm`** | Executive MIS Reporting | Automated Monthly Management Information System (MIS) Reports, Variance Summaries, VBA Macros | Macro-Enabled Workbook (`.xlsm`) | Inspected Structure & Macros |
| **`BIKE_BUYERS_ Dataset.xlsx`** | Consumer Demographics & Customer Segmentation | Demographics Analysis (Income, Distance, Age, Commute), Pivot Tables, Slicers, Dashboard Visuals | Standard Excel (`.xlsx`) | Inspected Data & Pivots |
| **`Pivot_Table.ods`** | Sales Summaries | Data Aggregations, Pivot Summaries across product categories | OpenDocument Spreadsheet (`.ods`) | Inspected Structure |
| **`New Attendance excel sheet.xlsx`** | Operational HR | Employee Attendance Tracking, Working Days, Absenteeism Rates | Standard Excel (`.xlsx`) | Inspected Structure |

---

## Detailed Project Descriptions

### 1. Employee Sales Dashboard (`EMP_SALES_DASHBOARD .xlsm`)
- **Purpose:** Tracks monthly sales productivity, sales targets, commission tiers, and regional performance per employee.
- **KPIs & Metrics:** Total Revenue, Sales Target Attainment %, Regional Rank, Average Order Value.
- **Excel Tools Used:** `SUMIFS`, `VLOOKUP`/`XLOOKUP`, Data Validation lists, Conditional Formatting, Form Control Buttons, VBA Macro routines.

### 2. MIS Management Report (`MIS REPORT_ DATA.xlsm`)
- **Purpose:** Consolidates operational data into executive-level monthly MIS reports for leadership review.
- **KPIs & Metrics:** Target vs Actual Revenue, Expense Ratios, Department Cost Breakdown.
- **Excel Tools Used:** Nested `IF` statements, `INDEX`/`MATCH`, Dynamic Pivot Tables, Macro-driven sheet updates.

### 3. Bike Buyers Demographic Analysis (`BIKE_BUYERS_ Dataset.xlsx`)
- **Purpose:** Analyzes demographic factors influencing customer bike purchasing decisions.
- **Key Columns:** `Marital Status`, `Gender`, `Income`, `Children`, `Education`, `Occupation`, `Home Owner`, `Cars`, `Commute Distance`, `Age`, `Purchased Bike`.
- **Excel Tools Used:** Nested `IF` income binning, Calculated Fields, Interactive Pivot Tables with Slicers.

---

## Limitations & Notes
- VBA macros require enabling macros upon opening `.xlsm` files in Microsoft Excel.
- Formula logic and macro code structures were inspected directly from binary XML spreadsheet components.
