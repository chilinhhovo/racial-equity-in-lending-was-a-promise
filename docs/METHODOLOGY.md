# Methodology: Racial Equity in Lending Analysis

## Data Sources and Collection

### 1. Home Mortgage Disclosure Act (HMDA) Database
- **Source**: Federal Financial Institutions Examination Council (FFIEC)
- **Coverage**: 2018-2024
- **Records**: 15+ million mortgage applications
- **Variables**: Race, ethnicity, approval status, loan amount, interest rate, lender information

### 2. Bank Annual Reports and Filings
- **JPMorgan Chase**: Annual reports 2020-2024
- **Bank of America**: Annual reports 2020-2024  
- **Wells Fargo**: Annual reports 2020-2024
- **Focus**: Racial equity language, diversity commitments, quantitative goals

### 3. Federal Reserve Data
- **Interest Rate Trends**: Bank vs non-bank lending rates
- **Lending Volume**: Mortgage origination patterns
- **Geographic Distribution**: State and metropolitan area data

### 4. Department of Justice Settlements
- **Redlining Cases**: 2022-2025 enforcement actions
- **Settlement Amounts**: Community investment requirements
- **Geographic Focus**: Underserved minority communities

## Data Processing Methodology

### 1. Data Filtering Criteria
- **Complete Records**: Only applications with complete race and approval data
- **Primary Residences**: Excludes investment properties and refinancing
- **Conventional Loans**: Focuses on standard mortgage products
- **Lender Verification**: Confirms lender identity and type

### 2. Race and Ethnicity Classification
- **Primary Categories**: White, Black, Hispanic/Latino, Asian, Native American
- **Self-Reported**: Based on applicant self-identification
- **Consistent Coding**: Standardized across all years and lenders

### 3. Approval Rate Calculation
- **Numerator**: Approved applications
- **Denominator**: Total applications (approved + denied)
- **Formula**: Approval Rate = Approved / (Approved + Denied)
- **Confidence Intervals**: 95% confidence intervals for statistical significance

### 4. Gap Analysis
- **Primary Metric**: White approval rate - Black approval rate
- **Percentage Points**: Absolute difference in approval rates
- **Statistical Testing**: T-tests for significance of differences
- **Trend Analysis**: Year-over-year changes in gaps

## Statistical Methods

### 1. Descriptive Statistics
- **Means and Medians**: Central tendency measures
- **Standard Deviations**: Variability in approval rates
- **Percentiles**: Distribution of lending outcomes

### 2. Inferential Statistics
- **T-Tests**: Comparison of means between racial groups
- **ANOVA**: Multi-group comparisons across lenders
- **Regression Analysis**: Controlling for confounding variables
- **P-Values**: Statistical significance thresholds (α = 0.05)

### 3. Geographic Analysis
- **State-Level Aggregation**: 50 states + DC
- **Metropolitan Areas**: Census-defined metropolitan statistical areas
- **Spatial Autocorrelation**: Testing for geographic clustering
- **Regional Patterns**: North/South, Urban/Rural comparisons

### 4. Temporal Analysis
- **Year-over-Year Changes**: Linear trends in approval rates
- **Pre/Post Analysis**: Before and after key policy changes
- **Seasonal Adjustments**: Accounting for seasonal lending patterns
- **Cohort Analysis**: Following specific borrower groups over time

## Visualization Methodology

### 1. Chart Design Principles
- **Minimal Aesthetic**: Clean, professional appearance
- **Color Accessibility**: High contrast, colorblind-friendly palettes
- **Clear Typography**: Helvetica Neue for consistency
- **Responsive Design**: Works across all device sizes

### 2. Interactive Elements
- **Hover Tooltips**: Detailed information on demand
- **Zoom and Pan**: User-controlled exploration
- **Filtering**: Race, year, lender type selection
- **Responsive Charts**: Adapts to screen size changes

### 3. Geographic Visualizations
- **Choropleth Maps**: State-level approval rate differences
- **Small Multiples**: Year-by-year comparison maps
- **Color Scales**: Consistent across all visualizations
- **Legend Design**: Clear, informative labeling

## Quality Control Measures

### 1. Data Validation
- **Range Checks**: Approval rates between 0 and 1
- **Consistency Checks**: Same lender across years
- **Missing Data**: Identification and handling of incomplete records
- **Outlier Detection**: Statistical identification of unusual values

### 2. Cross-Validation
- **Multiple Sources**: Verification across different data sets
- **Temporal Consistency**: Logical progression over time
- **Geographic Logic**: Reasonable state-to-state variations
- **Lender Verification**: Confirmation of lender identities

### 3. Peer Review
- **Academic Review**: Methodology reviewed by housing economists
- **Data Source Verification**: Confirmation of data accuracy
- **Statistical Review**: Validation of analytical methods
- **Visualization Review**: Testing of chart clarity and accuracy

## Limitations and Caveats

### 1. Data Limitations
- **Self-Reported Race**: Potential for misclassification
- **Missing Data**: Some applications lack complete information
- **Lender Reporting**: Variations in reporting accuracy
- **Geographic Coverage**: Some areas may have limited data

### 2. Methodological Constraints
- **Correlation vs Causation**: Cannot establish direct causality
- **Confounding Variables**: Other factors may influence outcomes
- **Selection Bias**: Applications may not represent all potential borrowers
- **Temporal Scope**: Limited to 2018-2024 period

### 3. Interpretation Challenges
- **Complex Causality**: Multiple factors influence lending decisions
- **Policy Interactions**: Multiple policy changes occurring simultaneously
- **Market Conditions**: Economic factors affecting all borrowers
- **Lender Strategies**: Individual bank policies and practices

## Ethical Considerations

### 1. Data Privacy
- **Individual Anonymity**: No personal information in analysis
- **Aggregate Reporting**: Only group-level statistics presented
- **Data Security**: Secure handling of sensitive information
- **Informed Consent**: Use of publicly available data only

### 2. Responsible Reporting
- **Contextual Information**: Providing full context for findings
- **Balanced Presentation**: Acknowledging limitations and caveats
- **Educational Purpose**: Intended for academic and policy understanding
- **No Harm Principle**: Avoiding stigmatization of communities

### 3. Academic Integrity
- **Transparent Methods**: Full disclosure of analytical approaches
- **Reproducible Results**: Code and data available for verification
- **Peer Review**: Subject to academic scrutiny and validation
- **Continuous Improvement**: Updating methods based on feedback

## Future Research Directions

### 1. Expanded Data Sources
- **Longer Time Series**: Extending analysis beyond 2024
- **Additional Variables**: Income, credit score, property type
- **Alternative Data**: Alternative credit scoring and lending data
- **International Comparisons**: Cross-country lending patterns

### 2. Advanced Methodologies
- **Machine Learning**: Predictive modeling of approval patterns
- **Natural Language Processing**: Analysis of bank language changes
- **Network Analysis**: Lender relationship and influence patterns
- **Causal Inference**: More sophisticated causal identification

### 3. Policy Impact Assessment
- **Intervention Analysis**: Before/after policy change effects
- **Counterfactual Scenarios**: What-if analysis of policy alternatives
- **Cost-Benefit Analysis**: Economic impact of policy changes
- **Stakeholder Analysis**: Impact on different borrower groups

---

*This methodology document provides a comprehensive overview of the analytical approach used in this thesis. For specific technical details, please refer to the Jupyter notebooks in the `notebooks/` directory.*
