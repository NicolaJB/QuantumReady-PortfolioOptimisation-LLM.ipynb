# RL Portfolio Optimiser

A practical demonstration of using **Reinforcement Learning (Proximal Policy Optimisation)** and **Modern Portfolio Theory (Markowitz)** to optimise a financial portfolio of equities. This project simulates a portfolio management scenario using a custom OpenAI Gym environment and compares classical optimisation with a modern RL-based strategy.

Built as a portfolio project for Applied AI / ML roles in finance, particularly aligned with roles involving NLP, RL, time-series, and production ML systems.

---

## Project Overview

This notebook walks through:

1. **Data Retrieval**  
   Downloads historical stock data using `yfinance`.

2. **Classical Portfolio Optimisation**  
   Uses Markowitz Modern Portfolio Theory to compute the optimal asset weights that minimise portfolio variance subject to constraints.

3. **Custom Gym Environment**  
   Defines a simulation environment (`PortfolioEnv`) to mimic real-world daily returns and allow interaction with an RL agent.

4. **Reinforcement Learning with PPO**  
   Trains a Proximal Policy Optimisation (PPO) agent from `stable-baselines3` to learn an adaptive rebalancing strategy.

5. **Evaluation & Comparison**  
   Compares the cumulative return of the RL strategy versus the classical Markowitz solution.

---

## Technologies Used

- `Python 3.11`
- `yfinance` for historical data
- `NumPy`, `Pandas`, `Matplotlib` for data manipulation and plotting
- `scipy.optimize` for classical optimisation
- `gymnasium` to build the custom environment
- `stable-baselines3` for the PPO agent

---

## Results Summary

| Strategy         | Return Metric                |
|------------------|------------------------------|
| Classical        | Static weights, Markowitz-optimal |
| PPO Agent (RL)   | Dynamic rebalancing strategy |

A cumulative return plot is provided to illustrate performance differences over the same investment horizon.

---

## Files

- `RL_Portfolio_Optimisation.ipynb` — Main Colab notebook containing full code and explanations.
- `README.md` — You’re reading it.

---

## Running the Notebook

To run in Google Colab:

1. Open the notebook in Colab or upload it directly
2. Ensure the runtime uses a GPU (optional, but speeds up PPO training)
3. Install dependencies:
  ```bash
   !pip install yfinance stable-baselines3 gymnasium pandas matplotlib
```
4. Run each cell in sequence
