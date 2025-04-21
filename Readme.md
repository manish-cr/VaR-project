# Value at Risk (VaR) Analysis of S&P 500 Index

This project aims to calculate the **Value at Risk (VaR)** for the S&P 500 index using its all-time historical data. VaR is a widely used risk measure in finance that quantifies the potential loss in value of an asset or portfolio over a defined period for a given confidence interval.

## Methods Used

The following methods were employed to calculate VaR:

1. **Historical Method**:
   - This method uses the historical returns of the S&P 500 index to calculate VaR by determining the percentile of the return distribution corresponding to the desired confidence level.

2. **Parametric Method**:
   - Assumes that the returns follow a normal distribution.
   - VaR is calculated using the mean and standard deviation of historical returns along with the quantile function of the normal distribution.

3. **Monte Carlo Simulation**:
   - Simulates potential future price paths of the S&P 500 index to estimate VaR. Two approaches were used:
     - **Geometric Brownian Motion (GBM)**: Simulates price paths based on drift (mean return) and volatility (standard deviation of returns).
     - **Bootstrap Method**: Resamples historical returns to generate simulated price paths.

## Expected Shortfall (ES)

In addition to VaR, the **Expected Shortfall (ES)** was calculated. ES, also known as Conditional VaR, measures the average loss in the worst-case scenarios beyond the VaR threshold. It provides a more comprehensive view of tail risk.

## Data Source

The analysis uses historical data of the S&P 500 index, which is stored in the `data/SP500.csv` file.

## Implementation

The project is implemented in Python using the following libraries:
- `pandas` for data manipulation.
- `numpy` for numerical computations.
- `matplotlib` for data visualization.
- `scipy.stats` for statistical calculations.

## Results

The results include:
- VaR estimates for different confidence levels using all methods.
- Visualization of simulated price paths and return distributions.
- Expected Shortfall values for a deeper understanding of tail risk.

## How to Run

1. Ensure all dependencies are installed.
2. Open the Jupyter Notebook `src/VaR comparisons.ipynb`.
3. Follow the steps in the notebook to calculate VaR and ES.

## Conclusion

This project provides a comprehensive analysis of the risk associated with the S&P 500 index using multiple VaR calculation methods. It highlights the importance of understanding both VaR and Expected Shortfall for effective risk management.