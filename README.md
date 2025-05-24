RL-Based Crypto Trading Bot
This project is a modular, reinforcement learning (RL)-powered trading system designed to operate on historical market data collected from Binance. It supports training and evaluation of agents across multiple cryptocurrency pairs (symbols) and timeframes (intervals) using a scalable and testable architecture.

🚀 Key Features
Reinforcement Learning Core: Utilizes the Proximal Policy Optimization (PPO) algorithm from Stable Baselines3 to learn trading strategies.

Multi-Symbol, Multi-Interval Support: Easily train agents on different combinations of coins (e.g., BTC, ETH) and intervals (e.g., 5m, 4h).

Custom Trading Environment: A Gym-compatible environment tailored for spot trading, supporting discrete actions (buy, sell, hold) and enriched with technical indicators (RSI, MACD, Bollinger Bands, etc.).

Web Interface: Flask-based interface to run experiments dynamically from a browser.

Reproducibility: Includes deterministic seeding, normalization, checkpointing, and backtesting functionality to ensure consistent results.

🧩 Architecture Overview
Data Module: Fetches OHLCV data from Binance and calculates indicators using ta, pandas, and numpy.

Environment Module: Custom RL environment built on gymnasium, designed for realistic trading simulations.

Training Module: Handles vectorized environments, model training, checkpoint saving, and evaluation.

UI Module: Lightweight Flask application for experiment orchestration and monitoring.

📊 Evaluation
The trained PPO agent showed consistent portfolio growth on unseen test data across multiple markets and conditions. Despite being deployed in a simulated environment, the model's latency and modularity make it suitable for future live integration.

🔧 Technologies
Python 3.10+

Gymnasium

Stable-Baselines3

Flask

Binance API (no keys required for public data)

TA-Lib (ta)

Pandas, NumPy

