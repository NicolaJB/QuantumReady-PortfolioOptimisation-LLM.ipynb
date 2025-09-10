
# Portfolio Optimisation with LLM-Derived Risk Scores

This project demonstrates AI-enhanced portfolio allocation, where traditional expected returns are replaced with risk scores derived from a language model (LLM). The goal is to minimise portfolio variance while maintaining strong expected outcomes, following Modern Portfolio Theory (MPT) principles.

The workflow showcases how multi-step AI pipelines can produce audit-ready, explainable outputs for financial decision-making in regulated or high-stakes environments.


## Key Features

- Analyse major stocks: **AAPL, GOOGL, MSFT, AMZN, TSLA**  
- Generate **document-driven risk scores** using an LLM  
- Compute portfolio variance and optimise allocations  
- Produce structured outputs suitable for **audit and compliance tracking**  
- Visualise the optimised portfolio allocations  

## Workflow Overview

1. **Data Retrieval & Preprocessing**  
   Download historical stock prices and compute returns and covariance matrix.  

2. **LLM Risk Scoring**  
   Generate risk scores per stock using a language model based on textual risk factors.  

3. **Portfolio Optimisation**  
   Define constraints and use classical optimisation to minimise variance under a minimum allocation per stock.  

4. **Evaluation & Audit Logging**  
   Compute weighted portfolio risk and variance; produce structured audit-ready outputs.  

5. **Visualisation**  
   Plot optimised portfolio weights to illustrate allocation strategy.  


## Technologies Used

- **Python 3.11**  
- **yfinance** – Historical stock data  
- **NumPy, Pandas, Matplotlib** – Data processing & visualisation  
- **scipy.optimize** – Portfolio optimisation  
- **transformers** – LLM inference for risk scoring  

## Outcomes

- Produced a fully reproducible, end-to-end AI workflow for portfolio optimisation.  
- Demonstrated how LLM-derived insights can augment classical financial models.  
- Created structured outputs for auditability, bridging AI with regulated-domain requirements.  

---

## License

This project is licensed under the **MIT License**.

