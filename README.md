RL vs ML for Stock Price Prediction
This repository presents the complete implementation for the research project titled "A Comparative Study of Reinforcement Learning and Traditional Machine Learning Techniques for Stock Price Prediction." The project investigates the effectiveness of various supervised and reinforcement learning models in forecasting stock prices and building profitable trading strategies.

Project Overview
Stock price prediction is a challenging problem due to the dynamic and non-stationary nature of financial markets. This study evaluates both traditional machine learning and reinforcement learning approaches by:

Using historical data of Netflix Inc. (NFLX) stock from Yahoo Finance.

Implementing models for both daily and hourly resolutions.

Comparing supervised models (XGBoost and LSTM) with reinforcement learning agents (DQN, PPO, A2C).

Constructing a custom Gym-based trading environment that incorporates market constraints such as transaction costs and interest rates.

Evaluating model performance using realistic financial metrics.

Models Used
Supervised Learning
XGBoost: A gradient boosting algorithm used for binary classification of price movement direction.

LSTM: A deep learning model capable of learning from sequential patterns in time-series data.

Reinforcement Learning
DQN (Deep Q-Network): A value-based method using experience replay and target networks.

PPO (Proximal Policy Optimization): A stable policy gradient method using clipped objective functions.

A2C (Advantage Actor-Critic): A synchronous variant of actor-critic methods balancing value and policy learning.

All RL agents were trained using a custom Gym-compatible trading environment with realistic market conditions.

Dataset and Features
Data Source: Yahoo Finance (retrieved via yfinance API)

Timeframes:

Daily data from January 2014 to April 2024

Hourly data from the most recent 60 trading days

Features: Technical indicators including RSI, MACD, OBV, VWAP, and various price ratios

Preprocessing: Feature engineering with the ta library, missing value handling, and an 80/20 train-test split

Custom Trading Environment
A Gym-compatible trading environment was built to simulate real-world trading:

Action space: Short, Hold, Long

Constraints:

Transaction cost: 0.005%

Borrow interest: 0.0001%

Initial portfolio value: $1000

State representation: Technical indicators and engineered price features

Evaluation Metrics
Models were evaluated using a unified strategy evaluation function based on:

Total Profit

Cumulative Return (%)

Sharpe Ratio

Maximum Drawdown

Total Trades

Win Rate

Performance was visualized using bar charts for comparative analysis across models.

Key Findings
PPO and A2C models consistently outperformed others in terms of profit, risk-adjusted return, and win rate.

XGBoost achieved moderate success but exhibited higher volatility.

LSTM failed to generate meaningful profits in this scenario.

Reinforcement learning models demonstrated superior adaptability and risk management in dynamic environments.
