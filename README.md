# Portfolio-Optimization-with-Financial-Data
Portfolio optimization project using Mean-Variance, Maximum Sharpe Ratio, and CVaR models on 5 years of financial data (AAPL, AMZN, GOOG, MSFT, TSLA). Includes data preprocessing, model formulation, algorithm implementation, and portfolio comparison using Python.

# Overview

This project performs quantitative portfolio optimization using five years of historical financial data from Apple, Amazon, Google, Microsoft, and Tesla. Three optimization models—Mean-Variance, Maximum Sharpe Ratio, and Conditional Value at Risk (CVaR)—are applied to evaluate risk–return trade-offs and identify the most efficient investment portfolio.

The models were implemented in Python using data pulled from Yahoo Finance via the **yfinance** library.

# Data Sources & Preprocessing

**Data Source:**  
Daily adjusted closing prices downloaded from **Yahoo Finance** (Oct 10, 2020 – Oct 10, 2025).

**Preprocessing steps included:**

- Selecting **Adjusted Close** prices to account for dividends/splits.  
- Removing missing values to create aligned time-series data.  
- Calculating **daily returns (%)**.  
- Computing:
  - Mean return vector  
  - Covariance matrix  
Both serve as core inputs for optimization models.


# Optimization Models

## **1️ Mean-Variance (Markowitz Model)**
- **Goal:** Minimize portfolio variance for a target return.  
- **Inputs:** Expected returns, covariance matrix.  
- **Output:** The lowest-risk portfolio for a chosen return level.  
- Best suited for **risk-averse investors**.


## **2️ Maximum Sharpe Ratio Portfolio**
- **Goal:** Maximize risk-adjusted return.  
- **Formula:** (Expected Return – Risk-Free Rate) / Volatility  
- Identifies the **most efficient portfolio** relative to risk.  
- Ideal for investors seeking optimized returns per unit risk.


## **3️ Conditional Value at Risk (CVaR)**
- **Goal:** Minimize losses beyond the Value at Risk (worst-case tail risk).  
- Useful for **downside-risk-focused** investors.  


# Algorithms Used
- **Global Minimum Variance (GMV):** Finds the lowest possible risk portfolio.  
- **Maximum Return Portfolio:** Maximizes expected return under a risk cap.  
- **Maximum Sharpe Ratio:** Identifies the best risk-adjusted portfolio.  
- All models solved as convex optimization problems.

# Optimization Results

| Model | Expected Return (%) | Volatility (%) | Sharpe Ratio |
|-------|----------------------|----------------|---------------|
| **GMV** | 20.98 | 24.28 | 0.86 |
| **Max Return** | 27.55 | 28.72 | 0.96 |
| **Max Sharpe** | 26.57 | 27.61 | 0.96 |

### **Key Insights**
- **GMV Portfolio:** Lowest volatility; ideal for conservative investors.  
- **Max Return Portfolio:** Highest return but also highest volatility.  
- **Max Sharpe Ratio Portfolio:**  
  🔹 Best balance between risk and reward  
  🔹 Provides strongest risk-adjusted performance  
  🔹 Selected as the **optimal portfolio**

### **Asset Weight Insights**
- GMV heavily weights **Microsoft**, followed by **Apple & Google**.  
- Sharpe-optimal and Max-return portfolios give **highest allocation to Google**.  
- Amazon receives close to **0 weighting** across models due to performance.  


# Visualizations Included
- Portfolio weight bar charts  
- Sharpe ratio comparison  
- Maximum return vs. volatility plots  
- Model comparison visual summaries  

# Final Summary
Across all three optimization models—GMV, Maximum Return, and Maximum Sharpe—analysis shows:

- GMV offers the **lowest risk**.
- Maximum Return offers the **highest growth**, with increased volatility.
- Maximum Sharpe provides the **best balance** of risk and return.
- Therefore, the **Maximum Sharpe Ratio portfolio** is recommended for long-term, risk-efficient investing.

# Files in This Repository
- Final project report (DOCX)  
- Python notebook (`.ipynb`) for optimization  
- README.md (documentation)  


# Author
Chandana Karnaty  
BANA 6670 – Prescriptive Analytics with Optimization  
University Project – Portfolio Optimization

