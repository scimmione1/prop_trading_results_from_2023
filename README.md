# Trading Results Analysis 2023

## Overview

This repository contains comprehensive analysis of proprietary trading results from 2023, including multiple prop trading firms and strategies. The analysis provides insights into trading performance, risk metrics, portfolio optimization, and statistical comparisons with market benchmarks.

## 📊 Project Structure

```
prop_trading_results_from_2023/
├── analysis_ipynb_files/          # Jupyter notebooks with analysis
│   └── analysis_full_data.ipynb   # Main comprehensive analysis
├── charts/                        # Generated visualizations
├── README.md                      # This file
├── prop_trading_results_from_2023.html  # HTML report
└── prop_trading_results_from_2023.pdf   # PDF report
```

## 🎯 Analysis Objectives

- **Performance Evaluation**: Analyze trading results across different prop firms
- **Risk Assessment**: Calculate risk metrics including Sharpe ratio, maximum drawdown, VaR
- **Benchmark Comparison**: Compare trading performance against S&P 500 (SPY)
- **Statistical Analysis**: Perform correlation analysis and significance testing
- **Portfolio Optimization**: Explore optimal portfolio allocation strategies
- **Visualization**: Create comprehensive charts and reports

## 📈 Key Features

### Trading Firms Analyzed
- **FTMO**: European prop trading firm
- **5%ers**: Prop trading challenge platform
- **FundedNext (FN)**: Trading funding program
- **MyForexFunds (MFX)**: Forex prop trading firm
- **The5%ers Match**: Additional trading accounts

### Analysis Components

1. **Daily Returns Analysis**
   - Calculate daily returns for each trading account
   - Aggregate performance across multiple accounts
   - Statistical distribution analysis

2. **Risk Metrics**
   - Sharpe Ratio calculation
   - Maximum Drawdown analysis
   - Value at Risk (VaR) estimation
   - Volatility measurements

3. **Benchmark Comparison**
   - S&P 500 (SPY) performance comparison
   - Relative performance metrics
   - Correlation analysis

4. **Portfolio Optimization**
   - Mean-variance optimization
   - Risk parity strategies
   - Efficient frontier analysis

5. **Monte Carlo Simulation**
   - Future performance projections
   - Risk scenario analysis
   - Confidence intervals

## 🔧 Technical Stack

### Python Libraries Used
```python
import pandas as pd              # Data manipulation and analysis
import numpy as np               # Numerical computing
import matplotlib.pyplot as plt  # Plotting and visualization
import seaborn as sns           # Statistical data visualization
import yfinance as yf           # Financial data retrieval
import scipy.stats as stats     # Statistical functions
import riskfolio as rp          # Portfolio optimization
import quantstats as qs         # Quantitative analysis
```

### Data Sources
- **Trading Account Data**: CSV files with daily account balances
- **Market Data**: Yahoo Finance API for benchmark data
- **Date Range**: Full year 2023 trading data

## 📋 Prerequisites

### Required Python Packages
```bash
pip install pandas numpy matplotlib seaborn
pip install yfinance scipy quantstats
pip install riskfolio-lib openpyxl
```

### Data Requirements
- Trading account CSV files with date and balance columns
- Internet connection for downloading market data
- Jupyter Notebook environment

## 🚀 Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/scimmione1/prop_trading_results_from_2023.git
   cd prop_trading_results_from_2023
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt  # If requirements.txt exists
   # Or install packages individually as listed above
   ```

3. **Prepare Data**
   - Place your trading CSV files in the appropriate directories
   - Ensure CSV files have consistent date and balance columns
   - Verify date formats are consistent

4. **Run Analysis**
   - Open `analysis_ipynb_files/analysis_full_data.ipynb`
   - Execute cells sequentially
   - Review generated charts and metrics

## 📊 Key Metrics & Results

### Performance Summary (2023)
- **Total Accounts Analyzed**: Multiple prop trading accounts
- **Analysis Period**: January 1, 2023 - December 31, 2023
- **Benchmark**: S&P 500 Index (SPY)

### Risk Metrics Calculated
- **Sharpe Ratio**: Risk-adjusted return measurement
- **Maximum Drawdown**: Largest peak-to-trough decline
- **Volatility**: Standard deviation of returns
- **Value at Risk (VaR)**: Potential loss estimation
- **Beta**: Market sensitivity coefficient

### Visualization Outputs
- Daily returns time series
- Cumulative performance charts
- Risk-return scatter plots
- Correlation heatmaps
- Drawdown analysis
- Monte Carlo simulation results

## 📁 File Descriptions

### Core Analysis Files
- **`analysis_full_data.ipynb`**: Main analysis notebook containing all calculations
- **`prop_trading_results_from_2023.html`**: Exported HTML report
- **`prop_trading_results_from_2023.pdf`**: PDF version of the analysis

### Data Processing
- CSV files are processed to extract daily returns
- Date standardization and missing data handling
- Account balance normalization for comparison

### Visualization
- All charts are generated using matplotlib and seaborn
- Export capabilities for PNG, PDF, and interactive formats
- Customizable styling and color schemes

## 🔍 Analysis Methodology

### Data Cleaning
1. Import CSV files with trading account data
2. Standardize date formats and handle missing values
3. Calculate daily returns from account balances
4. Remove outliers and validate data quality

### Performance Calculation
1. **Daily Returns**: `(Today's Balance - Yesterday's Balance) / Yesterday's Balance`
2. **Cumulative Returns**: Progressive multiplication of daily returns
3. **Annualized Metrics**: Scale daily metrics to annual equivalents

### Risk Assessment
1. **Volatility**: Standard deviation of daily returns
2. **Sharpe Ratio**: `(Return - Risk-free Rate) / Volatility`
3. **Maximum Drawdown**: Largest cumulative loss from peak
4. **VaR**: Statistical measure of potential losses

### Benchmark Analysis
1. Download S&P 500 data using yfinance
2. Calculate same metrics for benchmark
3. Perform statistical comparison tests
4. Analyze correlation and beta relationships

## 📈 Usage Examples

### Basic Performance Analysis
```python
# Load trading data
df = pd.read_csv('trading_data.csv')
df['returns'] = df['balance'].pct_change()

# Calculate key metrics
sharpe_ratio = df['returns'].mean() / df['returns'].std() * np.sqrt(252)
max_drawdown = (df['balance'] / df['balance'].cummax() - 1).min()
```

### Benchmark Comparison
```python
# Download SPY data
spy = yf.download('SPY', start='2023-01-01', end='2023-12-31')
spy_returns = spy['Adj Close'].pct_change()

# Calculate correlation
correlation = df['returns'].corr(spy_returns)
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/analysis-improvement`)
3. Commit your changes (`git commit -am 'Add new risk metric'`)
4. Push to the branch (`git push origin feature/analysis-improvement`)
5. Open a Pull Request

## 📝 License

This project is for educational and personal analysis purposes. Trading data is anonymized and aggregated.

## ⚠️ Disclaimer

This analysis is for educational purposes only and should not be considered as financial advice. Past performance does not guarantee future results. Trading involves substantial risk of loss.

## 📞 Contact

- **Author**: Nelli
- **Repository**: [prop_trading_results_from_2023](https://github.com/scimmione1/prop_trading_results_from_2023)
- **Branch**: master

## 🔄 Recent Updates

- Comprehensive analysis of 2023 trading results
- Integration of multiple prop trading firms data
- Advanced risk metrics calculation
- Portfolio optimization features
- Monte Carlo simulation capabilities

---

**Note**: This repository contains sensitive trading data. Ensure proper data privacy and security measures when working with financial information.
