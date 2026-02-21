# TokoMart Indonesia - Sales Tracker Dashboard

An automated daily sales reporting dashboard for **TokoMart Indonesia**, a minimarket chain with 50+ branches across the Greater Jakarta area (Jabodetabek). Built to provide real-time visibility into daily sales performance per branch with interactive filtering capabilities.

## Overview

The Head of Commercial needs a way to monitor sales across all branches efficiently. This project delivers an interactive Google Sheets dashboard with dynamic slicers and pivot charts, enabling quick filtering by branch, product category, and date range.

## Dataset

- **Source:** `dataset/data.csv`
- **Period:** January 1, 2025 - March 31, 2026
- **Records:** ~5,000 rows

### Schema

| Column | Description |
|--------|-------------|
| `Date` | Transaction date |
| `BranchID` | Branch/outlet ID |
| `BranchName` | Branch/outlet name |
| `ProductCategory` | Product category |
| `ProductName` | Product name |
| `Quantity` | Number of items sold |
| `Price` | Unit price |
| `TotalSales` | Total sales amount (Price x Quantity) |
| `Salesperson` | Sales staff responsible for the transaction |

## Project Workflow

### 1. Data Cleaning

The raw dataset contains several anomalies that need to be addressed before analysis:

- **Date gaps** — Missing dates in the transaction timeline (~3 instances)
- **Negative values** — Illogical negative numbers in quantity or sales (~10 instances)
- **Future dates** — Dates beyond the valid period, likely data entry errors (~5 instances)
- **Zero values** — Transactions recorded with zero price or amount (~8 instances)
- **Duplicate rows** — Exact duplicate entries (~15 instances)

All anomalies are documented and either removed or corrected to produce a clean dataset.

### 2. Trend Analysis

Key questions explored in the analysis:

- Which branches are the most profitable?
- What are the best-selling products?
- Are there seasonal trends or patterns in sales?
- Are there specific days or weeks with consistently high or low sales?

### 3. Key Metrics

After cleaning, the following summary metrics are computed:

| Metric | Description |
|--------|-------------|
| **Total Quantity** | Sum of all items sold |
| **Total Sales** | Sum of all sales revenue |
| **Total Salespersons** | Count of unique sales staff |

### 4. Dashboard

An interactive dashboard built in Google Sheets featuring:

- **Slicers/Filters** — Filter by branch, product category, and date range
- **Pivot Charts** — Visual breakdowns of sales data
- **Conditional Formatting** — Highlight top and bottom performers
- **Executive Summary** — Key insights and actionable recommendations at the top

## Deliverables

| Output | Format |
|--------|--------|
| Working File | Google Sheets / Excel (.xlsx) |
| Final Dashboard | Google Sheets with Slicers & Pivot Charts |

## catatan
1. sebelum memulai kita harus paham dulu apa yang diingkan, apa keperluannya, siapa pic yang membutuhkan

karakteristik orang yang membutuhkan dashboard adalah orang ini keingintahuannya besar, mau eksploratif

karena data analyst adalah penyampai pesan, agar tersampai harus pas, tidak kurang tidak lebih

pastikan juga tau definisi dari setiap kolom