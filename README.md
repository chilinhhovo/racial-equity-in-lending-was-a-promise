# Racial Equity in Mortgage Lending: Methodology, Analysis, and Visualizations

## Overview
This repository contains the data, code, and visualizations for a thesis examining racial equity commitments in U.S. mortgage lending, the persistence of approval gaps for Black and Latino borrowers, and shifts in diversity, equity, and inclusion (DEI) language in bank annual reports.

## Project Structure

```
hmda-thesis/
├── data/                         # Cleaned datasets, drop logs, and intermediate CSV files
├── notebooks/
│   ├── filter_2018_strict_only_race_expanded.ipynb   # HMDA data cleaning, strict filtering, and approval gap calculation
│   ├── bloomberg_lei.ipynb                           # Bloomberg scraping to fill missing lender names
│   ├── reports_scraping.ipynb                        # Annual report scraping and DEI term counting
├── docs/
│   ├── MP_methodology.pdf         # Full written methodology
├── assets/
│   ├── charts/                    # Static visualizations
│   ├── maps/                      # Choropleth maps
└── index.html                     # Interactive scrollytelling page
```

## Methodology Summary

### 1. Building the Lending Dataset
- **Data Source**: Public **Home Mortgage Disclosure Act (HMDA)** files for 2018–2024 (~124M records).
- **Cleaning Steps**:
  - Standardized borrower race codes (including Asian subgroups) and ethnicity fields.
  - Converted all financial fields (income, loan amount, property value, DTI) to numeric.
  - Created a unique row ID by concatenating lender **Legal Entity Identifier (LEI)** with the record index.
- **Strict Filter Criteria** (matched to regulatory/academic standards):
  1. Conventional (loan_type = 1) first-lien mortgages.
  2. Owner-occupied, site-built properties with ≤4 units.
  3. Complete data for income, loan amount, property value, and DTI.
  4. Applications coded as originated, approved but not accepted, or denied.
- Result: ~10M comparable records per year.

_Notebook_: `filter_2018_strict_only_race_expanded.ipynb`

### 2. Calculating Approval Rate Gaps
- Grouped by lender, state, year, and race.
- Approval rate = approvals ÷ total applications.
- **Gap** = White approval rate − Black approval rate (and − Latino rate where ethnicity available).
- Also calculated median loan amounts by race/year.
- Exported summary CSVs for visualization.

### 3. Resolving Lender Name Gaps
- HMDA lists lenders by LEI; some names missing in initial mapping.
- Wrote asynchronous scraper using **Playwright** to:
  - Open Bloomberg company profile.
  - Extract legal name text and match to LEI.
- Manually cross-checked remaining names for accuracy.

_Notebook_: `bloomberg_lei.ipynb`

### 4. Analyzing Corporate Language
- **Source**: Annual reports for largest banks (and available reports for major non-banks).
- Extracted text with **PyMuPDF** for consistent parsing.
- Counted case-insensitive matches of curated DEI terms (full list in methodology PDF).
- Observed:
  - Sharp rise in explicit racial equity terms in 2020–2021.
  - Decline in 2022–2024, replaced by euphemisms like “economic mobility” and “financial inclusion.”

_Notebook_: `reports_scraping.ipynb`

### 5. Cross-Checking with Experts and Enforcement Actions
- Interviews with fair lending experts for context.
- Reviewed DOJ redlining cases under the **Combatting Redlining Initiative**.
- Incorporated April 2025 policy change: end of DEI programs and halt to disparate-impact enforcement.

## Key Outputs
- **Choropleth Maps**: State-level approval gaps.
- **Time Series**: Approval rates by bank/race.
- **DEI Language Trends**: Term frequency over time in annual reports.
- **Scrollytelling Page**: Integrates visuals and narrative (`index.html`).

## Limitations
- Public HMDA data omits credit scores and other underwriting variables.
- Latino borrower analysis depends on sometimes incomplete ethnicity field.
- DEI term lists cannot capture all euphemisms.
- Non-bank lenders rarely publish detailed annual reports.

## Reproducibility
All processing is documented in the Jupyter notebooks. The **strict filter** and term-counting logic are parameterized for re-use with future HMDA releases and corporate filings.
