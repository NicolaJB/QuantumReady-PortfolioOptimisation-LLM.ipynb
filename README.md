
# RL Portfolio Optimiser

A practical demonstration of portfolio optimisation by integrating **Reinforcement Learning (Proximal Policy Optimisation, PPO)** with **Modern Portfolio Theory (Markowitz)**. This project simulates a financial portfolio management scenario through a custom OpenAI Gymnasium environment, comparing classical optimisation techniques with an adaptive RL-based strategy.

Built as a demonstration for practical skills in reinforcement learning, financial time-series analysis, custom environment design, and performance evaluation.


## Project Overview

This notebook guides you through:

1. **Data Retrieval**  
   Fetches historical equity price data using `yfinance`.

2. **Classical Portfolio Optimisation**  
   Applies Markowitz’s Modern Portfolio Theory to calculate asset weights that minimise portfolio variance while satisfying investment constraints.

3. **Custom Gymnasium Environment**  
   Implements a tailored simulation environment (`PortfolioEnv`) that models daily returns and portfolio rebalancing for reinforcement learning.

4. **Reinforcement Learning with PPO**  
   Trains a PPO agent from `stable-baselines3` to learn a dynamic portfolio allocation policy.

5. **Evaluation & Comparison**  
   Assesses and compares cumulative returns between the classical static portfolio and the RL-driven strategy.


## Technologies Used

- Python 3.11  
- `yfinance` for data acquisition  
- `NumPy`, `Pandas`, `Matplotlib` for data processing and visualisation  
- `scipy.optimize` for classical portfolio optimisation  
- `gymnasium` for building the custom RL environment  
- `stable-baselines3` for PPO reinforcement learning  


## Custom Reinforcement Learning Environment (Gymnasium)

The custom environment simulates a realistic portfolio management task, featuring:

- Observation and action spaces designed around portfolio weights and market return data  
- Reward function reflecting portfolio performance metrics (e.g., returns, risk-adjusted returns)  
- Step mechanics capturing the dynamics of asset price changes and portfolio rebalancing  

This environment enables effective training of PPO agents in a controlled yet realistic setting.


## Results Summary

| Strategy       | Description                     |
|----------------|---------------------------------|
| Classical      | Static portfolio weights based on Markowitz optimisation |
| PPO Agent (RL) | Adaptive dynamic portfolio rebalancing learned via reinforcement learning |

Visual comparison of cumulative returns illustrates the potential performance gains achievable by RL approaches.


## Files

- `RL_Portfolio_Optimisation.ipynb` — Complete Colab notebook with full code, explanations, and visualizations.  
- `README.md` — Project overview and instructions (this file).


## Running the Notebook

To run this project in Google Colab:

1. Open or upload the notebook in Colab.  
2. (Optional) Select a GPU runtime to speed up PPO training.  
3. Install dependencies by running:

    ```bash
    !pip install yfinance stable-baselines3 gymnasium pandas matplotlib
    ```

4. Execute cells sequentially to follow the complete workflow.

## License

This project is licensed under the MIT License.
