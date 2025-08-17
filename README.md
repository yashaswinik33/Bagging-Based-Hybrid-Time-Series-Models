# Forecasting: Base, Hybrid, and Bagged Hybrid Models  

**Author:** Yashaswini K  

---

##  Description  

This project implements and compares different time series forecasting approaches for **12 Indian economic indicators**:  

1. **Base Models** – individual forecasting models (SARIMA, ETS, STL+SARIMA, STL+ETS, NNAR, MLP).  
2. **Hybrid Models** – parallel hybrid forecasting with various weighting methods (Simple Mean, Trimmed Mean, Weighted Mean, SWAM, OLS-based, and Variance-Covariance weighting).  
3. **Bagged Models** – bootstrap aggregation applied to base models to reduce variance and improve forecast stability.  

The project outputs:  
- **Forecast predictions**  
- **Evaluation metrics**: RMSE and MAE  

---

##  Aim & Objectives  

**Aim:**  
To develop a **bagging-based hybrid time series model** to forecast Indian economic indicators with better forecasting capacity than the existing hybrid model.  

**Objectives:**  
- To examine the performance of selected base models in forecasting Indian economic indicators.  
- To examine the performance of parallel hybrid models with various weighting methods.  
- To examine the performance of bagged base models.  
- To examine the performance of bagging-based hybrid models with different weighting methods.  

---

## Dataset  

The dataset consists of **12 economic indicators** (monthly, various periods 2006–2022):  

- **E1** Broad Money Growth (%)  
- **E2** Broad Money to Reserves (%)  
- **E3** Composite Stock Price Index (monthly average, local index)  
- **E4** Policy Rate (% per annum, end of period)  
- **E5** Exchange Rate (Local Currency per US$, average)  
- **E6** Headline Inflation Rate  
- **E7** Real Effective Exchange Rate (CPI-based, 2015=100)  
- **E8** Consumer Price Index: Total All Items (Growth rate, YoY)  
- **E9** Economic Policy Uncertainty Index (India)  
- **E10** Manufacturing Production Index (2015=100)  
- **E11** Real Broad Effective Exchange Rate (2020=100)  
- **E12** Goods Export Value (USD, millions)  

---

## Data Sources  

- **Clearing Corporation Of India Limited (CCIL)**  
  - Provides financial instrument indices, treasury bills, government securities, etc.  
  - Dataset extracted from CCIL Treasury Bill Index (2009–2022).  
  - 🔗 [CCIL Data](https://www.ccilindia.com/Research/Statistics/Pages/CCILTBILLIndex.aspx)  

- **Asian Development Bank (ADB)**  
  - Provides economic and financial indicators for Asian economies.  
  - Data collected for GDP, inflation, and related economic measures.  
  - 🔗 [ADB Database](https://aric.adb.org/database/economic-financial-indicators)  

---

## Requirements  

This project is implemented in **R**. Required packages:  

```r
install.packages(c("tidyverse", "ggplot2", "readxl", "forecast", "nnfor", "neuralnet"))

