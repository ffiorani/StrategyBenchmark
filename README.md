---
# StrategyBenchmark

## Overview
This repository contains a Python notebook that compares various strategies for pairs trading. The notebook evaluates these strategies on multiple asset pairs to determine their performance.

## Methodology
1. **Data Collection**: 
   - Selected a list of 50 stocks from NASDAQ.
   - Downloaded their daily data over a specified period from Yahoo Finance.
   - Split the data into two periods: in-sample (for model training) and out-of-sample (for model testing).

2. **Pairs Selection**: 
   - Identified cointegrated pairs during the in-sample period.

3. **Strategy Implementation**:
   - Used the identified cointegrated pairs to run different variants of a mean-reverting strategy based on the z-score of their spread.

4. **Strategy Variants**:
   - **Denoising the spread with a Kalman filter**: Used the filtered spread as a new signal.
   - **Linear regression prediction**: Predicted the spread using linear regression and used this prediction as a signal.
   - **Moving average vs. Exponential moving average**: Compared the use of moving averages and exponential moving averages for generating signals.
   - **Hedge ratio adjustments**: Applied variants that reweighted the spread based on a hedge ratio.
   - **Buy and hold strategy**: Used as a baseline for comparison.

## Performance Metrics
The strategies were evaluated based on:
- **Sharpe Ratio**
- **Total Returns**
- **Maximum Drawdown**

The results were visualized using:
- **Categorical Plots**: Showing the mean of the metrics with a 95% confidence interval.
- **Histograms**: Displaying the frequency of each strategy performing the best.

## Results
The results indicated that while all strategies outperformed the buy and hold strategy, the linear regression with hedge ratios strategy consistently performed the best across all metrics in most scenarios.

## Usage
To explore the plots and results:
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/StrategyBenchmark.git
   ```
2. Navigate to the repository directory:
   ```sh
   cd StrategyBenchmark
   ```
3. Run the notebook:
   ```sh
   jupyter notebook
   ```
   Open the `StrategyBenchmark.ipynb` notebook and execute the cells.

## Presentation
The results from this notebook were presented to the members of [Capitox](https://capitox.co.uk/home).

Feel free to reach out if you have any questions or suggestions!

---
