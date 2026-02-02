# Global Universal Health Coverage Indicators (1985-2024)

## SEO Project Name
Global Universal Health Coverage (UHC) Service & Financial Hardship Indicators, 1985-2024

## SEO Description
A comprehensive, country-level time-series dataset of universal health coverage service coverage and financial hardship indicators, spanning 210 countries and regions from 1985-2024, with urban/rural and income-quintile stratifications for equity analysis.

## Top 5 Kaggle Tags
- universal-health-coverage
- global-health
- sdg-3-8
- health-indicators
- time-series

## Dataset Coverage
This dataset tracks UHC service coverage and financial hardship (catastrophic spending and impoverishing health expenditures). Values are reported as a 0-100 scale for service coverage indices and as percentages of population for financial hardship indicators. Equity breakdowns are provided by urbanization (urban/rural/total) and income quintiles (Q1-Q5 and all).

## Temporal and Geospatial Scope
- Start date: 01/01/1985
- End date: 12/31/2024
- Geospatial coverage: 210 countries and regions worldwide (global scope; country/region level).

## Provenance (Source and Transformations)
The indicator names align with WHO/World Bank monitoring of SDG 3.8, including the UHC Service Coverage Index (SDG 3.8.1) and financial hardship measures (SDG 3.8.2). The dataset has been consolidated into a single CSV with standardized columns and units. In the accompanying notebook, light transformations are applied for analysis: data type casting, duplicate detection/removal for analytic views, and summary aggregations (no imputation performed).

## Data Collection Methodology
Indicators are typically derived from nationally representative household surveys and administrative health system sources, and then harmonized by global health agencies for cross-country comparability. Stratifications by urbanization and income quintile reflect equity-focused reporting practices used in UHC monitoring frameworks.

## Columns and Details (Kaggle Dataset Card)
| Column | Type | Description | Example/Notes |
|---|---|---|---|
| Country_or_Region | string | Country or region name. | "Afghanistan" |
| Year | integer | Calendar year of observation. | 1985-2024 |
| Indicator | string (categorical) | UHC service coverage or financial hardship indicator. | "UHC Service Coverage Index" |
| Value | float | Indicator value. | 0-100 scale or percentage |
| Unit | string (categorical) | Measurement unit for Value. | "0-100 scale" or "Percentage of population" |
| Urbanization | string (categorical) | Urbanization stratifier. | "Urban area", "Rural area", "Total" |
| Income_Quintile | string (categorical) | Income quintile stratifier. | "Q1 (Poorest)" ... "Q5 (Richest)" or "All" |

### Indicator List (8 total)
- UHC Service Coverage Index
- Catastrophic Spending (More than 10% of household budget)
- Catastrophic Spending (More than 25% of household budget)
- Financial Hardship
- Financial Hardship (Impoverishing)
- Financial Hardship (Large Non-Impoverishing)
- Financial Hardship - 2.1: Pushed into poverty (based on societal poverty line) due to out-of-pocket health expenditure
- Financial Hardship - 2.2: Further impoverished due to out-of-pocket health expenditure, based on the societal poverty line

## Dataset Source (Correct Source + Link)
Primary source: World Health Organization (WHO) Global Health Observatory (UHC indicators, SDG 3.8)  
https://www.who.int/data/gho/data/themes/universal-health-coverage

Supplementary catalog reference (UHC global monitoring data):  
https://datacatalog.worldbank.org/search/dataset/0060802/universal-health-coverage-global-monitoring-data-2021

## Biggest Problems and Challenges
- Duplicate rows across key fields suggest the need for deduplication or clarification of source granularity.
- Uneven temporal coverage by country can bias trend comparisons.
- Mixed indicator units (index vs. percentages) require careful separation in analysis.
- Changes in survey methods and definitions over time can affect comparability.
- Equity stratifications may be missing for some countries/years, limiting subgroup analysis.
