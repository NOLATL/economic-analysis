# U.S. Economic Analysis: Consumer Financial Health & Recession Indicators (2000-2025)

## Overview

This repository contains a comprehensive, data-driven analysis of the U.S. economy from 2000 to present, with particular emphasis on the post-pandemic period (2022-2025). The analysis examines the striking paradox of resilient economic indicators alongside elevated consumer financial stress, investigating the mechanisms that have sustained consumer spending despite significant headwinds.

## Key Questions Addressed

- **Why do traditional recession indicators remain benign while consumer sentiment is depressed?**
- **How did households maintain spending through 25 months of negative real wage growth?**
- **What is the sustainability of current consumption patterns?**
- **Are we heading toward a recession, or has the economy achieved a soft landing?**

## Executive Summary

The analysis reveals a U.S. economy that is **not in crisis, but in a vulnerable state**. While unemployment remains low (4.3%) and inflation has moderated (2.94%), consumers have depleted pandemic savings (from 31.8% peak to 4.6% currently) and accumulated debt to maintain spending through the longest negative real wage period in the dataset (April 2021 - May 2023). Financial stress indicators show yellow lights across the board—elevated but not yet critical.

**The Central Finding:** The resilience of consumer spending should not be mistaken for consumer financial strength. The next 12-18 months will be critical in determining whether positive real wage growth can rebuild household financial buffers before the next economic shock arrives.

## Data Sources

All economic data is sourced from the **Federal Reserve Economic Data (FRED)** database maintained by the Federal Reserve Bank of St. Louis. The analysis utilizes the FRED API via the `fredapi` Python library for programmatic data access.

## Methodology

### Standardized Time Periods
The analysis uses consistent period definitions across all indicators:
- **Pre-Pandemic**: Jan 2000 - Feb 2020 (241 months)
- **Pandemic Era**: Mar 2020 - Dec 2021 (21 months)
- **Post-Pandemic**: Jan 2022 - Oct 2022 (9 months)
- **AI Era**: Nov 2022 - Present (33 months)

## Analysis Framework

### 1. Recession Indicators
- **Sahm Rule Analysis**: Real-time recession probability assessment
- **Yield Curve Inversion**: Historical analysis of 10Y-2Y spread with 90.9% recession prediction accuracy
- **Current Status**: No Sahm signal (0.13 gap vs. 0.5 threshold); yield curve normalized after 793-day inversion

### 2. Inflation Deep Dive
- Overall CPI trends with 3-month and 12-month moving averages
- Category-level disaggregation across 9 major components
- Market-based inflation expectations (5Y and 10Y breakeven rates)
- **Finding**: Inflation at 2.94%, approaching Fed's 2% target; housing (3.97%) remains primary driver

### 3. Labor Market Dynamics
- Unemployment trends across standardized time periods
- Industry-level employment tracking (6 sectors)
- JOLTS analysis: job openings, hires, quits, layoffs
- Labor force participation and U-6 unemployment
- **Finding**: Strong but cooling—openings down from 12k+ peak to 7,227k; quits/layoffs ratio declining

### 4. Real Wage Crisis Analysis
- Nominal wage growth vs. inflation
- Identification of negative real wage periods
- **Critical Finding**: 25 consecutive months of negative real wage growth (April 2021 - May 2023) with -1.88% average loss—the longest period in the dataset

### 5. Consumer Financial Health
- Personal savings rate tracking (pandemic surge → drawdown)
- Consumer credit analysis (revolving vs. non-revolving)
- Financial stress indicators dashboard (delinquencies, charge-offs, debt service ratio)
- **Finding**: Savings depleted to 4.6% (below 5.2% pre-pandemic); all stress metrics trending upward but below crisis levels

### 6. Consumer Sentiment
- University of Michigan Consumer Sentiment Index
- Sentiment-reality disconnect analysis
- **Finding**: Sentiment at 58.2 vs. 82.3 average—businesses see sales, consumers feel stress

### 7. Comprehensive Integration
- Multi-indicator overlay visualization
- Phase identification: Pandemic Buffer → Savings Drawdown → Debt Accumulation
- Sustainability assessment of current consumption patterns

## Key Findings

### The Economic Paradox
- **Traditional indicators**: Unemployment 4.3%, no Sahm signal, normalized yield curve ✅
- **Consumer stress**: Sentiment 58.2, savings 4.6%, credit accelerating ⚠️
- **The mechanism**: Households depleted pandemic savings and accumulated debt to maintain spending through negative real wage period

### Financial Stress: Yellow Lights, Not Red
- Credit card delinquency: 3.05% vs. 6.77% (2008 crisis) ✅
- Auto loan delinquency: 1.79% vs. 10.40% (2008 crisis) ✅
- Debt service ratio: 11.25% vs. 13.0% (crisis threshold) ✅
- **But**: All metrics trending upward; savings buffer depleted; limited room for further drawdown ⚠️


## Key Insights

1. **The 25-Month Real Wage Crisis**: The longest negative real wage period in the dataset explains the mechanism behind consumer financial stress—households had to choose between cutting spending or depleting savings/accumulating debt.

2. **The Great Savings Drawdown**: Personal savings rate fell from 31.8% (April 2020) to 4.6% (current), below both pre-pandemic (5.2%) and long-term average (5.7%).

3. **Yellow Lights Everywhere**: Financial stress indicators are elevated and trending upward, but remain well below 2008 crisis levels—suggesting vulnerability rather than crisis.

4. **The Sentiment-Reality Disconnect**: Consumer sentiment (58.2) is closer to recession levels despite strong employment because consumers feel the stress of depleted savings and accumulated debt, even as they continue spending.

5. **Sustainability Question**: The next 12-18 months are critical—can positive real wage growth rebuild household buffers before the next shock?

### Critical Assessment
**Reasons for Concern:**
- Savings buffer largely depleted with limited room for further drawdown
- Multiple stress indicators trending in wrong direction
- Margin for error has narrowed considerably

**Reasons for Optimism:**
- Real wages finally positive after 25 months of erosion
- Stress metrics still well below crisis levels
- Labor market remains strong

## Limitations & Caveats

- **BNPL Debt**: Buy Now Pay Later debt is not fully captured in traditional consumer credit statistics, suggesting actual household debt may be higher than measured
- **Lagging Data**: Some indicators (quarterly data, JOLTS) have reporting delays
- **Unprecedented Context**: The pandemic period created unique dynamics that may limit historical comparisons
- **Forward-Looking Uncertainty**: Analysis is descriptive and diagnostic, not predictive


## Repository Structure
├── README.md # This file ├── economic_analysis.ipynb # Main Jupyter notebook with full analysis ├── requirements.txt # Python dependencies └── data/ # (Data pulled via FRED API)



## Installation & Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab
- FRED API key (free from https://fred.stlouisfed.org/docs/api/api_key.html)

### Setup

1. Clone the repository:

bash git clone https://github.com/NOLATL/economic-analysis.git cd us-economic-analysis



2. Install dependencies:

bash pip install -r requirements.txt



3. Set up your FRED API key:

In the notebook, replace with your API key
fred = Fred(api_key='your_api_key_here')



4. Run the analysis:

bash jupyter notebook economic_analysis.ipynb



## Requirements

pandas>=1.5.0 numpy>=1.23.0 plotly>=5.11.0 fredapi>=0.5.0

## Contributing

This is an analytical repository focused on economic research. If you identify data issues, methodological improvements, or have suggestions for additional analysis, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **Federal Reserve Bank of St. Louis** for maintaining the FRED database
- **National Bureau of Economic Research (NBER)** for recession dating
- **Bureau of Labor Statistics (BLS)** for employment and inflation data
- **University of Michigan** for consumer sentiment data

## Contact

For questions, suggestions, or collaboration opportunities, please open an issue in this repository.

## Citation

If you use this analysis in your research or reporting, please cite:

U.S. Economic Analysis: Consumer Financial Health & Recession Indicators (2000-2025)
Jared Carollo: GitHub: https://github.com/NOLATL/economic-analysis (2025)


---

**Disclaimer**: This analysis is for informational and educational purposes only. It does not constitute financial, investment, or economic advice. Economic conditions can change rapidly, and past performance does not guarantee future results.
