# Excel-Filter-Tutorial

# 📊 Excel FILTER() Demo – Turning Excel into a Mini Query Engine

## 🚀 Overview

This project demonstrates how modern Excel functions like `FILTER()`, `SORT()`, `UNIQUE()`, and `CHOOSECOLS()` can transform Excel from a static spreadsheet tool into a **dynamic, query-driven analysis engine**.

Instead of relying solely on PivotTables or manual filters, this approach enables:

- SQL-like querying directly in Excel
- Dynamic, real-time filtering
- Formula-driven dashboards
- Clean, composable data logic

---
NOTE: The corresponding article can be found at:
https://datasciencereview.com/attention-excel-users-and-business-owners-allow-me-to-introduce-the-filter-function/

## 🎯 Objective

Show how small and medium-sized businesses (SMBs) can:

> **Get database-like capabilities without leaving Excel**

This project is especially useful for organizations that:
- Already rely heavily on Excel
- Want better insights without adopting complex tools
- Need lightweight, flexible reporting systems

---

## 📁 File Structure
excel_filter_demo.xlsx
├── SalesData → Raw dataset (structured as an Excel Table: Sales)
└── Analysis → Query layer using dynamic array formulas

---

## 🧾 Dataset

The dataset includes ~2 years of synthetic sales data with the following fields:

- Date  
- OrderID  
- Customer  
- Region  
- Product  
- Category  
- SalesAmount  
- Sales Rep  

The data is structured as an Excel Table (`Sales`) to enable:
- Structured references
- Automatic expansion
- Clean formula design

---

## 🧠 Core Concept: Excel as a Query Engine

This project maps Excel functions to SQL concepts:

| Excel Function | SQL Equivalent |
|----------------|----------------|
| `FILTER()`     | `WHERE`        |
| `SORT()`       | `ORDER BY`     |
| `UNIQUE()`     | `DISTINCT`     |
| `CHOOSECOLS()` | `SELECT`       |
| Table (`Sales`)| `FROM`         |

---

## 🔍 Example Queries

### 1. Filter by Region

```excel
=FILTER(Sales, Sales[Region]="East")

Similar SQL:
SELECT *
FROM Sales
WHERE Region = 'East'

## Multiple Conditions
=FILTER(Sales, (Sales[Region]="East")*(Sales[SalesAmount]>1000))

SQL
WHERE Region IN ('East', 'West')

## Sorting
=SORT(FILTER(Sales, Sales[Region]="East"), 7, -1)

SQL Sorting
ORDER BY SalesAmount DESC

## Unique Values
=UNIQUE(Sales[Customer])

SQL
SELECT DISTINCT Customer
FROM Sales

=FILTER(Sales, Sales[Region]=B1) (From Video)
