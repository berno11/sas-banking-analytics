# 🏦 SAS PROC SQL — Banking Analytics Portfolio

<div align="center">

**Bernice Kidiiga** · Senior Data Analyst · Charlotte, NC

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
![SAS](https://img.shields.io/badge/SAS-PROC%20SQL-blue)
![Domain](https://img.shields.io/badge/Domain-Banking%20%26%20Financial%20Services-darkgreen)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

📧 berno77@gmail.com &nbsp;|&nbsp; 📍 Charlotte, NC &nbsp;|&nbsp; 💼 [View Full Portfolio](https://github.com/YOUR_USERNAME/sas-banking-analytics)

</div>

---

## About

This repository demonstrates applied **SAS PROC SQL** skills using a realistic mock banking dataset modeled after enterprise financial services environments — the same analytical patterns used in regulatory reporting, loan portfolio analysis, AML/KYC compliance, audit exception tracking, and data reconciliation at institutions like **Wells Fargo** and **Bank of America**.

> 🔒 **Dataset files are not included in this public repository.**
> Column definitions and data structure are documented in [`DATA_DICTIONARY.md`](DATA_DICTIONARY.md).
> To request the full practice datasets, contact **berno77@gmail.com**

---

## Repository Structure

```
sas-banking-analytics/
│
├── README.md                          ← This file
├── LICENSE                            ← CC BY-NC 4.0 (view only, no commercial use)
├── DATA_DICTIONARY.md                 ← Full column definitions (datasets not included)
│
├── setup/
│   └── sas_ondemand_setup.md          ← SAS OnDemand for Academics configuration
│
└── exercises/                         ← 25 PROC SQL exercises with full solutions
    ├── 01_basic_select_where.sas
    ├── 02_group_by_aggregation.sas
    ├── 03_inner_join.sas
    ├── 04_left_join_gap_detection.sas
    ├── 05_subquery_vs_cte.sas
    ├── 06_case_statement.sas
    ├── 07_having_clause.sas
    ├── 08_union_all.sas
    ├── 09_create_table.sas
    ├── 10_correlated_subquery.sas
    ├── 11_ranking_monotonic.sas
    ├── 12_date_functions.sas
    ├── 13_null_handling_data_quality.sas
    ├── 14_three_table_join.sas
    ├── 15_calculated_exception_report.sas
    ├── 16_reconciliation_query.sas
    ├── 17_macro_variable_into.sas
    ├── 18_audit_aging_report.sas
    ├── 19_deduplication.sas
    ├── 20_ctr_regulatory_summary.sas
    ├── 21_percent_of_total.sas
    ├── 22_not_exists_orphan_detection.sas
    ├── 23_exception_trend_analysis.sas
    ├── 24_insert_into.sas
    └── 25_end_to_end_regulatory_report.sas
```

---

## Skills Demonstrated

| Category | Concepts |
|----------|----------|
| **Filtering & Selection** | WHERE, AND/OR, IN, BETWEEN, IS NULL |
| **Aggregation** | COUNT, SUM, AVG, MIN, MAX, GROUP BY, HAVING |
| **Joins** | INNER JOIN, LEFT JOIN, three-table joins |
| **Subqueries & CTEs** | Correlated subqueries, WITH clause, IN/EXISTS/NOT EXISTS |
| **Conditional Logic** | CASE WHEN, CALCULATED keyword |
| **Set Operations** | UNION ALL, UNION |
| **Date Functions** | INPUT(), YEAR(), MONTH(), period filtering |
| **Data Quality** | NULL profiling, deduplication, gap detection |
| **Automation** | SELECT INTO macro variables, CREATE TABLE, INSERT INTO |
| **Regulatory Patterns** | CTR summaries, loan risk tiers (DPD), reconciliation |
| **Audit Reporting** | Exception aging, severity bucketing, remediation tracking |

---

## Exercise Index

| # | Exercise | Banking Use Case |
|---|----------|-----------------|
| 01 | Basic SELECT + WHERE | AML/KYC customer filtering |
| 02 | GROUP BY + Aggregation | Portfolio distribution by account type |
| 03 | INNER JOIN | Customer–account 360 view |
| 04 | LEFT JOIN — Gap Detection | Orphan customer records / onboarding failures |
| 05 | Subquery vs. CTE | High-risk customer transaction extraction |
| 06 | CASE Statement | Loan risk tier classification (DPD buckets) |
| 07 | HAVING Clause | Concentrated account holders (KYC) |
| 08 | UNION ALL | Cross-system exception + CTR combined report |
| 09 | CREATE TABLE | Delinquent loan staging table |
| 10 | Correlated Subquery | Above-average exposure by segment |
| 11 | Ranking with MONOTONIC() | Top 10 balances per account type |
| 12 | Date Functions | Q4 high-value transaction filter |
| 13 | NULL Handling + Profiling | Loan table data quality scorecard |
| 14 | Three-Table JOIN | Full 360-degree customer view |
| 15 | CALCULATED Keyword | Over-limit account exception detection |
| 16 | Reconciliation Query | Source vs. EDW balance variance |
| 17 | Macro Variable INTO | Dynamic threshold-based exception flagging |
| 18 | Audit Aging Report | Exception aging by severity bucket |
| 19 | Deduplication | Duplicate customer record detection |
| 20 | CTR Regulatory Summary | Monthly CTR filing by channel and type |
| 21 | Percent of Total | Loan portfolio concentration by type |
| 22 | NOT EXISTS | Accounts with no transaction history |
| 23 | Exception Trend Analysis | Exception heat map by source system |
| 24 | INSERT INTO | Appending new audit exception records |
| **25** | **★ End-to-End Regulatory Report** | **Full portfolio dashboard — all 5 tables joined** |

---

## Professional Background

12+ years of enterprise data analytics in financial services and healthcare:

- **Regulatory reporting** — data validation, reconciliation, and audit support across EDW environments
- **Data governance** — source-to-target mapping, data lineage, quality control frameworks  
- **SQL & SAS analytics** — large-scale querying on Teradata, Oracle, and SQL Server  
- **Visualization** — Tableau dashboards for compliance, portfolio, and operational KPIs

*Tools: SAS · SQL · Python · Tableau · Alteryx · Oracle · Teradata · SQL Server · BigQuery*

---

## License & Usage

© 2024 Bernice Kidiiga · Licensed under [CC BY-NC 4.0](LICENSE)

- ✅ View and learn from this code
- ✅ Reference with attribution for personal/academic use
- ❌ Do not redistribute or publish as your own work
- ❌ Do not use commercially without written permission

---

*All datasets referenced in this repository are fully synthetic. No real customer, account, or financial data is included.*
