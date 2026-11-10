
# Medicare Fraud Detection & Provider Billing Analysis

### Identifying Unusual Medicare Billing Patterns Through Data Analytics

## Project Overview

Medicare Part B provides outpatient healthcare coverage to millions of Americans. With approximately 1.3 million providers billing Medicare, identifying unusual billing patterns and prioritizing providers for further review is an important challenge.

This project analyzes Medicare provider billing data alongside the HHS Office of Inspector General (OIG) exclusion records to investigate potential indicators of unusual billing activity.

Rather than relying solely on total Medicare payments, we examine provider billing behavior, service intensity, and specialty-specific differences to identify patterns that may support more effective provider screening.

**Research Question:** How can data analytics help identify unusual Medicare billing patterns and improve the prioritization of providers for further review?

## Data Sources

The analysis combines two publicly available datasets:

**1. CMS Medicare Part B Provider Summary (2024)**

- Source: Centers for Medicare & Medicaid Services (CMS)
- 1,296,739 provider records
- 81 variables
- Includes provider characteristics, Medicare payments, service volumes, beneficiary counts, specialties, and patient characteristics.

**2. HHS OIG List of Excluded Individuals/Entities (LEIE)**

- Source: HHS Office of Inspector General
- 84,001 records
- 18 variables
- Contains information about individuals and organizations excluded from federal healthcare programs.

The datasets were linked using National Provider Identifiers (NPIs) to compare billing patterns between OIG-matched providers and other Medicare providers.

## Tools & Methodology

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, and Jupyter Notebook.

The analysis involved:

1. **Data Preparation:** Cleaning provider records, handling missing values, and integrating CMS and OIG datasets.
2. **Exploratory Data Analysis:** Examining distributions of Medicare payments, beneficiary counts, and service volumes.
3. **Provider Comparison:** Comparing billing patterns between OIG-matched and non-matched providers.
4. **Specialty-Based Analysis:** Evaluating providers relative to others within the same medical specialty.
5. **Anomaly Screening:** Identifying unusual billing patterns using payment and service-intensity indicators.
6. **Data Visualization:** Communicating key findings through statistical charts and comparisons.

## Key Findings

### 1. Medicare Payments Are Highly Concentrated

Medicare reimbursements are distributed unevenly across providers.

- The top 1% of providers account for approximately 35.5% of total Medicare payments.
- The top 10% account for approximately 66.5%.

However, high payments do not necessarily indicate inappropriate billing, as provider size, specialty, and patient volume can significantly influence total reimbursement.

### 2. Payment Amount Alone Is Not a Reliable Screening Indicator

The analysis identified 157 providers matched to OIG exclusion records, including 83 providers with at least 100 Medicare beneficiaries.

A screening approach based solely on payment amount missed 82 of these 83 providers.

This suggests that relying only on total payments may overlook potentially relevant billing patterns.

### 3. Service Intensity Provides Additional Information

OIG-matched providers tended to report more services per beneficiary than other providers.

This suggests that service intensity may offer useful supplementary information when evaluating billing patterns, particularly when providers are compared within the same specialty.

### 4. Multiple Screening Indicators Are More Informative

Payment-based and service-intensity screening indicators showed only partial overlap.

No single screening rule consistently identified all potentially unusual providers, highlighting the importance of combining multiple indicators rather than relying on one metric.

## Business Implications

The findings suggest several opportunities to improve Medicare provider screening:

- Compare providers with peers in the same medical specialty rather than using universal payment thresholds.
- Consider service intensity alongside total Medicare payments.
- Account for differences in patient characteristics and practice size.
- Use multiple billing indicators to prioritize providers for further review.
- Treat unusual billing patterns as screening signals rather than definitive evidence of fraud.

A more comprehensive screening approach could help healthcare oversight organizations allocate limited review resources more effectively.

## My Contributions

As a member of the project team, I contributed to the data visualization and interpretation of Medicare billing patterns.

My responsibilities included:

- Developing analytical visualizations to explore provider billing behavior and screening indicators.
- Comparing provider-level payment and service-intensity measures.
- Analyzing the overlap between different screening criteria.
- Documenting findings and interpreting the implications of the results.
- Contributing visualizations and analytical explanations to the final project presentation.

## Limitations

This analysis identifies potentially unusual billing patterns rather than confirmed fraudulent behavior.

OIG exclusion status does not necessarily indicate that a provider committed Medicare billing fraud, and differences in patient complexity, medical specialty, and practice characteristics can influence billing patterns.

The results should therefore be interpreted as indicators for further investigation, not definitive conclusions about provider misconduct.

## Project Notebook

The full analysis, code, and supporting visualizations are available in this repository:

[B01-Medicare-Fraud-Detection.ipynb](B01-Medicare-Fraud-Detection.ipynb)

## Conclusion

This project demonstrates how data analytics can support healthcare oversight by identifying unusual provider billing patterns and evaluating alternative screening strategies.

The analysis highlights the limitations of relying solely on total payment amounts and emphasizes the potential value of combining specialty-adjusted comparisons with service-intensity indicators.

Through this project, I gained experience working with large public healthcare datasets, integrating multiple data sources, developing analytical visualizations, and translating quantitative findings into actionable business recommendations.
