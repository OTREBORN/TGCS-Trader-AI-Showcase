# TGCS Trader AI

TGCS Trader AI is a Python-based trading automation project built around MetaTrader 5 and designed for XAUUSD analysis, trade planning, risk management, and systematic backtesting.

> **Status:** Active development and demo testing
> **Repository:** Public showcase
> **Core trading engine:** Kept private

## What It Does

TGCS Trader AI combines multiple market-analysis components to evaluate potential XAUUSD setups and generate structured trade plans.

The system currently includes:

* Market structure analysis
* Break of Structure (BOS) detection
* Liquidity and liquidity-sweep detection
* Order Block detection
* Fair Value Gap (FVG) detection
* RSI and ATR analysis
* Trading-session analysis
* Automated entry planning
* Stop-loss and take-profit calculation
* Risk-based position sizing
* MetaTrader 5 integration
* Historical backtesting
* Out-of-sample validation
* Live demo-market monitoring
* Demo trade execution testing

## System Architecture

```text
Market Data
     │
     ▼
Market Analysis
     │
     ├── Structure
     ├── BOS
     ├── Liquidity
     ├── Liquidity Sweeps
     ├── Order Blocks
     ├── FVG
     ├── RSI
     └── ATR
     │
     ▼
Signal Scoring
     │
     ▼
AI Decision Engine
     │
     ▼
Trade Planner
     │
     ├── Entry
     ├── Stop Loss
     └── Take Profit
     │
     ▼
Risk Management
     │
     ▼
MetaTrader 5
```

## Backtesting

The project has been tested against historical XAUUSD M5 data using progressively larger samples.

### 10,000-Candle Test

After correcting order-block timing and adding a structural-risk filter:

* **18 completed trades**
* **13 wins**
* **5 losses**
* **72.22% win rate**
* **1% risk-model simulated profit:** +$22,984.45
* **Maximum simulated drawdown:** $1,169.20
* **Maximum losing streak:** 1

These results are historical simulations and are **not a guarantee of future performance**.

## Out-of-Sample Validation

A separate unseen section of historical data was used to reduce the risk of evaluating the system only on the data used during development.

Validation results:

* **6 trades**
* **4 wins**
* **2 losses**
* **66.67% win rate**
* **+6R**
* **Profit factor:** 4.00

The sample is still small, so further forward testing is required.

## Risk Management

The system supports percentage-based risk management and evaluates:

* Account balance
* Risk percentage
* Stop-loss distance
* Position size
* Maximum structural risk
* Broker volume limits
* Spread conditions
* Duplicate-position protection

The current development configuration uses a 1% risk model for testing.

## Demo Forward Testing

The project is currently being tested on a MetaTrader 5 demo environment.

The live monitoring engine can:

* Watch XAUUSD
* Process new M5 candles
* Detect developing setups
* Generate trade plans
* Produce sound alerts
* Test demo execution
* Prevent duplicate positions
* Apply spread checks

The production strategy and proprietary implementation remain private.

## Technology

* Python
* MetaTrader 5
* Pandas
* Technical-analysis components
* Custom market-structure detection
* Risk-management engine

## Development Roadmap

* Expand forward demo testing
* Increase statistical sample size
* Improve execution reliability
* Add stronger trade journaling
* Expand risk controls
* Continue prop-firm compatibility research
* Build additional reporting and monitoring tools

## Disclaimer

TGCS Trader AI is a software-development and research project.

Historical backtests and simulated results do not guarantee future trading performance. Trading financial markets involves substantial risk, and automated systems can experience losses, technical failures, data issues, execution differences, and unexpected market conditions.

## Project

**TGCS Trader AI**
Built and maintained by **TGCS**
