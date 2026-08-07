# AI-Based Price Estimation & Algorithmic Trading Automation With Portfolio Optimization on Cryptocurrencies

## Overview

This project is at the intersection of artificial intelligence, financial analysis, and blockchain technology, focusing on the cryptocurrency market. It leverages Long Short-Term Memory (LSTM) networks for time-series forecasting, incorporating both econometric indicators and sentiment analysis to enhance prediction accuracy. The core objective is to provide an AI-driven framework for price estimation and to automate trading strategies with an emphasis on portfolio optimization.

### Key Features

- **LSTM for Time-Series Prediction**: Utilizes LSTM networks trained on historical data from Binance, aiming to forecast future cryptocurrency prices with high accuracy.
- **Econometric Indicators and Sentiment Analysis**: Enhances prediction accuracy by integrating traditional technical analysis indicators with sentiment analysis from various online sources.
- **Automated Trading Strategy**: Implements an automated trading strategy that dynamically adjusts based on the AI's predictions and a set of predefined rules for risk management.
- **Portfolio Optimization**: Employs flexible computing techniques to optimize asset allocation within a portfolio, maximizing returns while minimizing risk.

### Results

Alpha testing of our model demonstrated an 88.7% average accuracy in price prediction. This significant level of accuracy underscores the effectiveness of combining LSTM with econometric indicators and sentiment analysis for cryptocurrency price forecasting.

## Repository Structure

| Path | Description |
|------|-------------|
| `Reguler Code/` | Production-style pipeline: Binance download helpers, indicator computation, LSTM trainer, virtual trading bots |
| `Reguler Code/Scrapt_Coin_Price/` | Binance Vision downloaders for klines, trades, and aggTrades |
| `ShortTime/` | Short-horizon LSTM + RSI experiments and CSV export scripts |
| `Attempt to RealTime/` | Notebooks exploring nearer-to-real-time LSTM forecasting |
| `Archive/PA1`–`PA3` | Earlier assignment/iteration notebooks (LSTM, CHZ, sentiment-augmented LSTMv2) |
| `BiL4009-Rapor.pdf`, `Poster.pdf`, `Sunum.pptx` | Project report, poster, and presentation |

## Typical Workflow (`Reguler Code/`)

1. Download klines via `Scrapt_Coin_Price/` or `main.py`
2. Merge/convert with `Conventer.py`
3. Compute indicators with `Indicators.py`
4. Train LSTMs with `Trainer.py` (batch via `Trainer-main.py` + `config.json`)
5. Simulate trading with `VirtualBot_Dynmc.py` / `VirtualBot_DynmcTime.py`
