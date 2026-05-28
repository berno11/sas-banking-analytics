# Data Dictionary — Mock Banking Datasets

> **Note:** The actual dataset files are not included in this public repository to protect the integrity of the practice environment.
> To request access to the full CSV files for collaborative learning or review purposes, contact: **berno77@gmail.com**

---

## Overview

Five interconnected synthetic datasets modeled after an enterprise banking data environment. All data is fully fictitious — no real customers, accounts, or financial records are included.

| Dataset | Rows | Primary Key | Description |
|---------|------|-------------|-------------|
| `customers` | 200 | CUSTOMER_ID | Customer master with segmentation, risk, and AML attributes |
| `accounts` | 500 | ACCOUNT_ID | Account portfolio — balances, types, origination channels |
| `transactions` | 1,000 | TRANSACTION_ID | Transaction ledger with CTR flags and channel data |
| `loans` | 300 | LOAN_ID | Loan portfolio — delinquency, risk classification, balances |
| `audit_exceptions` | 150 | EXCEPTION_ID | Data governance exception tracking and remediation |

---

## Table: CUSTOMERS

| Column | Data Type | Sample Values | Description |
|--------|-----------|---------------|-------------|
| CUSTOMER_ID | VARCHAR(6) | C0001, C0002 | Unique customer identifier |
| CUSTOMER_NAME | VARCHAR | Customer_1 | Synthetic customer name |
| CUSTOMER_TYPE | VARCHAR | Individual, Business | Account holder classification |
| SEGMENT | VARCHAR | Retail, Commercial, Wholesale, Private, Small Business | Business segment |
| STATE | VARCHAR(2) | NC, TX, CA | US state code |
| OPEN_DATE | DATE | 2015-06-30 | Date relationship opened |
| STATUS | VARCHAR | Active, Inactive, Closed, Suspended | Current customer status |
| RELATIONSHIP_YEARS | NUMERIC | 1–30 | Length of banking relationship |
| AML_FLAG | VARCHAR | Yes, No | Anti-money laundering flag |
| RISK_RATING | VARCHAR | Low, Medium, High, Very High | KYC risk classification |

---

## Table: ACCOUNTS

| Column | Data Type | Sample Values | Description |
|--------|-----------|---------------|-------------|
| ACCOUNT_ID | VARCHAR(7) | A00001 | Unique account identifier |
| CUSTOMER_ID | VARCHAR(6) | C0001 | Foreign key → CUSTOMERS |
| ACCOUNT_TYPE | VARCHAR | Checking, Savings, Mortgage, HELOC, Auto Loan, CD, Money Market, LOC | Product type |
| CURRENT_BALANCE | NUMERIC | -500 to 500,000 | Current account balance (USD) |
| CREDIT_LIMIT | NUMERIC | 1,000 to 1,000,000 | Credit limit where applicable |
| OPEN_DATE | DATE | 2010-09-13 | Account open date |
| ACCOUNT_STATUS | VARCHAR | Open, Closed, Delinquent, Charged Off, Frozen | Account status |
| CURRENCY | VARCHAR(3) | USD, EUR, GBP, CAD | Account currency |
| ORIGINATION_CHANNEL | VARCHAR | Branch, Online, Mobile, Telephone | How account was opened |
| INTEREST_RATE | NUMERIC | 0.000–7.500 | Current interest rate (%) |

---

## Table: TRANSACTIONS

| Column | Data Type | Sample Values | Description |
|--------|-----------|---------------|-------------|
| TRANSACTION_ID | VARCHAR(8) | T000001 | Unique transaction identifier |
| ACCOUNT_ID | VARCHAR(7) | A00001 | Foreign key → ACCOUNTS |
| TRANSACTION_TYPE | VARCHAR | Deposit, Withdrawal, Transfer, Payment, Fee, Interest, Wire, Reversal | Transaction category |
| TRANSACTION_AMOUNT | NUMERIC | -50,000 to 50,000 | Signed transaction amount |
| ABS_AMOUNT | NUMERIC | 0 to 50,000 | Absolute value of amount |
| TRANSACTION_DATE | DATE | 2022-09-12 | Date transaction posted |
| STATUS | VARCHAR | Posted, Pending, Reversed, Failed, Flagged | Processing status |
| CHANNEL | VARCHAR | ATM, Branch, Online, Mobile, ACH, Wire, POS | Transaction channel |
| REFERENCE_NUMBER | VARCHAR | REF288085 | System reference number |
| CTR_FLAG | VARCHAR | Yes, No | Currency Transaction Report flag (>$10,000) |

---

## Table: LOANS

| Column | Data Type | Sample Values | Description |
|--------|-----------|---------------|-------------|
| LOAN_ID | VARCHAR(7) | L00001 | Unique loan identifier |
| ACCOUNT_ID | VARCHAR(7) | A00001 | Foreign key → ACCOUNTS |
| CUSTOMER_ID | VARCHAR(6) | C0001 | Foreign key → CUSTOMERS |
| LOAN_TYPE | VARCHAR | Mortgage, Auto, Personal, Commercial, HELOC, SBA, Student | Loan product type |
| ORIGINAL_AMOUNT | NUMERIC | 5,000–1,000,000 | Original loan amount at origination |
| OUTSTANDING_BALANCE | NUMERIC | 0–1,000,000 | Current outstanding balance |
| INTEREST_RATE | NUMERIC | 1.500–8.500 | Loan interest rate (%) |
| ORIGINATION_DATE | DATE | 2015-01-01 | Loan origination date |
| MATURITY_DATE | DATE | 2025-2040 | Loan maturity date |
| LOAN_STATUS | VARCHAR | Current, 30DPD, 60DPD, 90DPD, Charged Off, Paid Off, Defaulted | Delinquency status |
| DAYS_PAST_DUE | NUMERIC | 0–180 | Number of days past due |
| COLLATERAL_FLAG | VARCHAR | Yes, No | Secured/collateralized indicator |

---

## Table: AUDIT_EXCEPTIONS

| Column | Data Type | Sample Values | Description |
|--------|-----------|---------------|-------------|
| EXCEPTION_ID | VARCHAR(5) | E0001 | Unique exception identifier |
| IDENTIFIED_DATE | DATE | 2022-04-15 | Date exception was identified |
| EXCEPTION_TYPE | VARCHAR | Missing Documentation, Balance Mismatch, Duplicate Record, Source System Discrepancy, Stale Data | Exception category |
| SEVERITY | VARCHAR | Low, Medium, High, Critical | Business impact severity |
| STATUS | VARCHAR | Open, In Review, Resolved, Escalated, Waived | Remediation status |
| SOURCE_SYSTEM | VARCHAR | CoreBanking, LoanSystem, GL, DataWarehouse, ReportingLayer, ETL_Pipeline | System where exception originated |
| RELATED_RECORD_ID | VARCHAR | A00001 or C0001 | Account or customer ID linked to exception |
| ASSIGNED_ANALYST | VARCHAR | Analyst_1 through Analyst_10 | Analyst responsible for remediation |
| RESOLUTION_DATE | DATE | 2022-05-01 | Date exception was resolved (if applicable) |
| DAYS_OPEN | NUMERIC | 0–90 | Number of days exception has been open |

---

## Relationship Diagram

```
CUSTOMERS (CUSTOMER_ID) ────────┬──── ACCOUNTS (CUSTOMER_ID → ACCOUNT_ID)
                                 │              │
                                 └──── LOANS    └──── TRANSACTIONS (ACCOUNT_ID)
                                      (CUSTOMER_ID, ACCOUNT_ID)

AUDIT_EXCEPTIONS.RELATED_RECORD_ID  →  references ACCOUNT_ID or CUSTOMER_ID
```

---

*Datasets designed by Bernice Kidiiga to reflect enterprise banking data patterns from 12+ years of financial services experience.*
*Contact berno77@gmail.com to request dataset files.*
