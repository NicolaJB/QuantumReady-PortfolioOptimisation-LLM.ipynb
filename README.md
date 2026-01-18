# Quantum-Ready Portfolio Optimisation with LLM-Derived Risk Scores (Classical Prototype)

## Overview
This repository implements a classical portfolio optimisation workflow where traditional expected returns are replaced with LLM-derived weighted risk scores. The objective is to minimise portfolio variance while maintaining strong risk-adjusted expected returns, following Modern Portfolio Theory (MPT) principles. The notebook is designed as a modular, end-to-end prototype demonstrating all the steps needed for quantitative portfolio workflows:
- Data ingestion and preprocessing for multiple instruments
- Feature engineering and LLM-driven risk scoring
- Variance-based portfolio optimisation under diversification constraints
- Backtesting with out-of-sample evaluation
- Structured, audit-ready outputs for compliance and reproducibility

### Quantum-Ready Design
Although currently classical, the pipeline is quantum-ready: any component, particularly risk scoring or optimisation, can be replaced with quantum or hybrid classical–quantum methods without rebuilding the workflow. This makes it a practical sandbox for experimentation with quantum-enhanced portfolio allocation, variational circuits, or other quantum ML approaches.

### This version:  
- Reads like a professional **prototype/portfolio repo**.  
- Emphasises LLM integration, auditability, reproducibility, and backtesting.  
- Keeps headings, tables, and code blocks for clarity.  
- Highlights technical impact without overloading the body text.  

The project also serves as a teaching and prototype example for exploring how LLMs can enhance transparent, audit-ready financial decision-making workflows.

## Features
- LLM-driven risk scoring: generate per-stock risk scores from textual risk factors
- Portfolio optimisation: minimise variance under allocation constraints
- Audit-ready outputs: structured logs of risk scores and optimised weights
- Visualisation: clear plots of portfolio allocation suitable for stakeholder review
- Reproducible workflow: end-to-end pipeline contained in a single notebook

## Technical Highlights
- Replaces traditional expected returns with LLM-derived weighted risk scores
- Optimises portfolio allocations with constraints on diversification
- Backtests portfolio performance on out-of-sample data to produce Sharpe ratios and drawdown metrics
- Generates audit-ready logs for compliance tracking
- Produces visualisations of portfolio allocations and expected risk
- Demonstrates integration of modern NLP and classical quantitative finance pipelines

## Repository Structure
```bash
portfolio-optimisation-llm-risk/
├─ README.md # This file
├─ PortfolioOptimisation.ipynb # Full analysis pipeline
├─ data/ # (Optional) sample documents / risk factors
└─ images/ # Example outputs (charts, audit logs)
```

## Quick Start

1. **Download the notebook**  
   Save `PortfolioOptimisation-LLMDerived-RiskScores.ipynb` from this repository to your local machine or open it directly in Google Colab.

2. **Open in Jupyter or Colab**  
   Launch the notebook in your preferred environment.

3. **Run the first cell to install dependencies**
   
   The first cell installs the required Python packages automatically:
   ```python
   !pip install yfinance pandas numpy matplotlib scipy transformers
   ```
   Requires Python ≥3.11, yfinance, pandas, numpy, matplotlib, scipy, transformers.
   
4. **Configure tickers and risk documents**
- In the first cell, edit the tickers list or documents dictionary to match your own portfolio universe.

5. **Run all cells**
The notebook performs the following steps:
- Download historical stock prices
- Compute daily returns and covariance matrix
- Generate LLM risk scores for each stock
- Optimise portfolio weights under diversification constraints
- Backtest portfolio performance on out-of-sample data
- Log structured outputs for audit
- Visualise portfolio allocations

6. Outputs
```
| Ticker | LLM_Risk_Score | Optimised_Weight |
| ------ | -------------- | ---------------- |
| AAPL   | 0.000857       | 11.2%            |
| GOOGL  | 0.997363       | 32.6%            |
| MSFT   | 0.080955       | 13.9%            |
| AMZN   | 0.997703       | 35.8%            |
| TSLA   | 0.999336       | 6.5%             |
```
**Example Portfolio Weights Allocation & Performance Charts**: 

A bar chart visualises the fraction of capital allocated to each stock according to variance minimisation.  

![Portfolio Weights](images/portfolio_weights.png)

Portfolio performance plot visualises confirmation of portfolio growth, stability, and risk.

![Portfolio Performance](images/portfolio_performance.png)

### Interpretation Guide
- LLM Risk Score: 0 = low risk (positive sentiment), 1 = high risk (negative sentiment)
- Optimised Weight: fraction of capital allocated to each stock
- Portfolio Variance: total risk metric based on covariance matrix given chosen weights
- Portfolio Sharpe Ratio: measure of risk-adjusted performance, computed on full and out-of-sample periods

### Data and Compliance
- Uses publicly available market data (Yahoo Finance) and synthetic sample documents
- No confidential or personally identifiable information is included
- Provided for demonstration and educational purposes only

### Technologies
- Python 3.11
- yfinance for historical stock data
- NumPy and Pandas for data processing
- SciPy for optimisation
- Matplotlib for visualisation
- Hugging Face Transformers for LLM inference

## Licence
MIT Licence. See the LICENCE file for details.
