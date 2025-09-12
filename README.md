# Portfolio Optimisation with LLM-Derived Risk Scores

## Overview
This repository demonstrates how language-model-derived risk scores can augment classical portfolio optimisation. It replaces traditional expected returns with document-driven risk metrics to minimise portfolio variance while maintaining strong expected outcomes under Modern Portfolio Theory (MPT) principles.

It is intended as a teaching and prototype example for teams exploring how LLMs can enrich regulated financial decision-making with transparent, audit-ready outputs.

## Features
- LLM-driven risk scoring: generate per-stock risk scores from textual risk factors.
- Portfolio optimisation: minimise variance under allocation constraints.
- Audit-ready outputs: structured logs of risk scores and optimised weights.
- Visualisation: clear plots of allocation strategy for stakeholders.
- Fully reproducible: end-to-end workflow in a single notebook.

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
The notebook will:
- Download historical price data
- Compute returns and covariance matrix
- Generate risk scores via a language model
- Optimise portfolio weights
- Log structured outputs for audit
- Plot optimised allocations

## Outputs
Audit Log Table:

Ticker | LLM_Risk_Score | Optimised_Weight

**Example Portfolio Weights Allocation Chart**  
![Portfolio Weights](images/portfolio_weights.png)  

These outputs are suitable for presentations, stakeholder reviews, or compliance documentation.

## Interpretation Guide
- LLM Risk Score: 0 = low risk (positive sentiment), 1 = high risk (negative sentiment).
- Optimised Weight: Fraction of capital allocated to each stock under variance minimisation.
- Portfolio Variance: Total risk metric from the covariance matrix given chosen weights.

## Data and Compliance Note
This project uses publicly available market data (Yahoo Finance) and synthetic sample documents for risk scoring. No confidential or personally identifiable information is included. It is provided for demonstration and educational purposes only.

## Technologies
- Python 3.11
- yfinance – historical stock data
- NumPy / Pandas – data processing
- SciPy – optimisation
- Matplotlib – visualisation
- Hugging Face Transformers – LLM inference

## Licence
MIT Licence. See the LICENCE file for details.
