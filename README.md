# Portfolio Risk Analysis using PCA and GARCH Models
## Project Overview
This project aims to evaluate the risk of a candidate portfolio using **Principal Component Analysis (PCA)** and **GARCH(1,1)** models. The portfolio consists of six stocks: **META, AMZN, AAPL, GOOG, V, and JNJ**, with data spanning from **January 4, 2010, to December 31, 2019**. The analysis focuses on identifying factor structures using PCA and modeling volatility using GARCH to predict portfolio risk.


## Table of Contents
1. [Introduction](#introduction)
2. [Methodology](#methodology)
3. [Results](#results)
4. [Potential Improvements](#improvements)
5. [License](#license)
6. [Contact](#contact)


## Introduction <a name="introduction"></a>
### Project Goal
The goal of this project is to apply risk management techniques, including PCA and GARCH models, to evaluate the risk of a candidate portfolio. The analysis includes calculating **Value-at-Risk (VaR)** and conducting backtesting to validate the model's predictions.

### Portfolio Description
The portfolio consists of six equally weighted stocks:
- **META (Meta Platforms Inc.)**
- **AMZN (Amazon.com Inc.)**
- **AAPL (Apple Inc.)**
- **GOOG (Alphabet Inc.)**
- **V (Visa Inc.)**
- **JNJ (Johnson & Johnson)**

The data covers the period from **January 4, 2010, to December 31, 2019**.


## Methodology <a name="methodology"></a>
### Principal Component Analysis (PCA)
PCA is used to identify the factor structure of the portfolio. The first four principal components (PC1–PC4) account for nearly **90% of the total explained variance**, with PC1 alone explaining **52%**.

### GARCH(1,1) Model
The GARCH(1,1) model is applied to model the volatility of each factor. GARCH is chosen for its ability to capture **volatility persistence** and **heavy-tailed distributions** with fewer parameters compared to ARCH models.

### Value-at-Risk (VaR)
VaR is calculated using the **parametric method**, assuming that the standardized returns are normally distributed. The predicted VaR for the portfolio is **0.0216**.

### Backtesting
Backtesting is performed using **rolling predictions** to validate the model. The results show that the model tends to **overestimate VaR**, as indicated by the violation ratio and unconditional coverage test.


## Results
### Key Findings
1. **PCA Results**:
   - The first four principal components explain **90% of the variance**.
   - PC1 alone explains **52% of the variance**.

2. **VaR and Backtesting**:
   - Predicted VaR: **0.0216**.
   - Violation ratio: **0.441** (indicating overestimation of VaR).
   - The model captures tail behaviors effectively but struggles during extreme volatile periods.

3. **Coverage Tests**:
   - **Unconditional coverage test**: Rejected (violations do not occur at the expected frequency).
   - **Conditional coverage test**: Not rejected (violations are independent).


## Potential Improvements <a name='improvements'></a>
1. ### Distributional Assumptions:
The current model assumes that standardized returns are normally distributed. 
Future work could explore alternative distributions (e.g., Student-t or Generalized Error Distribution) to better capture the fat-tailed nature of financial data.

2. ### GARCH Model Enhancements:
Consider using more sophisticated GARCH models (e.g., EGARCH or GJR-GARCH) to capture asymmetric volatility effects (e.g., leverage effects).

3. ### Dynamic Portfolio Weights:
The current portfolio is equally weighted. Future work could explore dynamic weighting strategies (e.g., risk parity or minimum variance) to optimize the portfolio's risk-return profile.

4. ### Extended Data Range:
The current analysis covers the period from 2010 to 2019. Extending the data range to include more recent years (e.g., 2020-2023) could provide insights into the model's performance during extreme market conditions (e.g., COVID-19 pandemic).

5. ### Additional Assets:
The current portfolio consists of six stocks. Adding more assets (e.g., bonds, commodities, or international stocks) could improve portfolio diversification and risk management.

6. ### Advanced Backtesting Methods:
The current backtesting method uses rolling predictions. Future work could explore other methods (e.g., Bootstrap or Monte Carlo simulations) to validate the model's robustness.


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


## Contact <a name='contact'></a>
For questions or feedback, please contact:
- **GitHub**: [Your GitHub Profile](https://github.com/Yiyun-zhou)
