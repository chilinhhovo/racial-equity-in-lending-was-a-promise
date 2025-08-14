# Racial Equity in Lending: A Promise That Didn't Last

## Overview
This repository contains the data, analysis, and interactive visualizations for a thesis examining racial equity commitments in mortgage lending and their subsequent rollback under the Trump administration's 2025 executive order.

## Project Structure

```
hmda-thesis-github/
├── index.html                 # Main interactive thesis webpage
├── assets/
│   ├── images/
│   │   └── exec_order/        # Executive order images for scrollytelling
│   ├── charts/                # Key charts and visualizations
│   └── maps/                  # Geographic visualizations
├── data/                      # All CSV data files
├── notebooks/                 # Jupyter notebooks for analysis
└── docs/                      # Documentation and methodology
```

## Key Findings

### Executive Order Impact
- **January 20, 2025**: President Trump signed executive order ending diversity programs
- **Disparate Impact Doctrine**: Key enforcement mechanism of Fair Housing Act removed
- **Regulatory Rollback**: Banks no longer held accountable for racial gaps without proof of explicit bias

### JPMorgan Chase Case Study
- **2020**: $30 billion racial equity commitment, 17 mentions in annual report
- **2021**: Strong language maintained, 16 racial equity references
- **2022**: Shift to "long-term impact," mentions dropped to 7
- **2023-2024**: Retreat from explicit racial equity commitments

### Lending Disparities
- **Approval Rate Gaps**: Black borrowers consistently approved at lower rates than White borrowers
- **Geographic Patterns**: Highest denial rates in states with histories of racial exclusion
- **Bank vs Non-Bank**: Non-bank lenders charge higher fees while filling lending gaps

## Data Sources

### Primary Data
- **HMDA Database**: 15+ million mortgage records (2018-2024)
- **Bank Annual Reports**: JPMorgan Chase, Bank of America, Wells Fargo
- **Federal Reserve**: Interest rate and lending data
- **DOJ Settlements**: Redlining enforcement cases
- **Bloomberg Terminal**: Financial data and lender information

### Key Datasets
- `race_approval_rates_by_state_year.csv`: State-level approval rates by race and year
- `bank_race_summary.csv`: Bank-specific approval rate disparities
- `bank_nonbank_interest_rate_by_race_year.csv`: Interest rate differences by lender type
- `merged_by_race_cleaned.csv`: Top lender analysis by race
- `state_race_summary.csv`: Geographic lending patterns
- `bloomberg_scraped_structured.csv`: Bloomberg financial data for lender analysis

## Interactive Features

### Charts and Visualizations
1. **Bank Approval Rate Disparities**: Interactive charts showing White vs Black approval gaps
2. **State Comparison Maps**: Geographic visualization of lending disparities
3. **Temporal Analysis**: Year-over-year changes in racial equity commitments
4. **Lender Type Analysis**: Bank vs non-bank lending patterns

### Scrollytelling Elements
- **Executive Order Timeline**: Interactive exploration of policy changes
- **JPMorgan Commitment Evolution**: Visual tracking of language changes
- **Geographic Patterns**: State-level lending disparity maps

## Methodology

### Data Processing
- **Filtering**: Strict criteria for complete race and approval data
- **Aggregation**: State, year, and race-level summaries
- **Gap Calculation**: White approval rate minus Black approval rate
- **Statistical Analysis**: Significance testing and trend analysis

### Visualization Approach
- **Minimal Design**: Clean, professional aesthetic matching academic standards
- **Responsive Layout**: Works across all device sizes
- **Interactive Elements**: Hover tooltips with detailed information
- **Accessibility**: High contrast, clear typography, descriptive labels

## Key Charts

### 1. Approval Rate Disparities by Bank
- **JPMorgan Chase**: ~6 percentage point gap
- **Bank of America**: ~2 percentage point gap (smallest)
- **Wells Fargo**: Double-digit gaps, narrowing after 2023

### 2. Geographic Patterns
- **Mississippi, Louisiana, Arkansas**: 14+ percentage point gaps
- **Historical Context**: States with histories of racial exclusion
- **Temporal Trends**: Persistent disparities 2018-2024

### 3. Lender Type Analysis
- **Non-Bank Dominance**: 61%+ of single-family mortgages by 2022
- **Fee Structure**: 24.7% higher setup fees than banks
- **Access Patterns**: Higher approval rates but higher costs

## Technical Implementation

### Frontend Technologies
- **HTML5/CSS3**: Semantic structure and responsive design
- **JavaScript**: Interactive charts and data processing
- **Plotly.js**: Chart rendering and interactivity
- **D3.js**: Geographic visualizations and data manipulation

### Data Processing
- **Python**: Jupyter notebooks for analysis
- **Pandas**: Data manipulation and aggregation
- **Matplotlib/Seaborn**: Static chart generation
- **CSV Export**: Clean data for web integration
- **Web Scraping**: Bloomberg Terminal data collection

### Responsive Design
- **Mobile-First**: Optimized for all screen sizes
- **CSS Grid/Flexbox**: Modern layout techniques
- **Media Queries**: Adaptive styling across breakpoints
- **Touch-Friendly**: Optimized for mobile interaction

## Installation and Usage

### Local Development
1. Clone the repository
2. Open `index.html` in a web browser
3. Ensure all data files are in the `data/` directory
4. For development, use a local server (e.g., Python `http.server`)

### Data Updates
1. Place new CSV files in the `data/` directory
2. Update file paths in `index.html` if necessary
3. Test all visualizations with new data

### Customization
- **Charts**: Modify Plotly configurations in JavaScript functions
- **Styling**: Update CSS variables and classes
- **Data**: Replace CSV files with new datasets
- **Content**: Edit HTML structure and text content

## Dependencies

### Web Dependencies
- Plotly.js (CDN)
- PapaParse (CSV parsing)
- D3.js (geographic visualizations)

### Development Dependencies
- Python 3.8+
- Jupyter Notebook
- Pandas
- Matplotlib
- Seaborn

## Contributing

### Guidelines
- Maintain academic rigor and data accuracy
- Follow responsive design principles
- Ensure accessibility compliance
- Document all data sources and methodology

### Code Style
- Clean, readable HTML/CSS/JavaScript
- Consistent naming conventions
- Comprehensive commenting
- Error handling for data loading

## License and Attribution

### Data Sources
- **HMDA**: Home Mortgage Disclosure Act database
- **Bank Reports**: Public annual reports and filings
- **Federal Data**: Public government datasets

### Academic Use
This project is intended for academic research and public education about racial equity in lending. All data sources are publicly available and properly attributed.

## Contact

For questions about methodology, data sources, or technical implementation, please refer to the documentation in the `docs/` directory or review the Jupyter notebooks in the `notebooks/` folder.

---

**Note**: This repository contains sensitive data about racial disparities in lending. Please use this information responsibly and in accordance with academic and ethical guidelines.
