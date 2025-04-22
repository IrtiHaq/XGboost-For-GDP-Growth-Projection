# XGboost-For-GDP-Growth-Projection

## Research Question:
**How Accurately Can a Machine Learning Model be Used to Predict and Forecast GDP Growth Rates For OECD Nations?**
For this project, our goal is to explore how ML can be applied to Economic Data and be used to forecast and predict the GDP Growth Rate for OECD Nations. GDP Growth Rate Projections play a crucial role in helping Economists and Government planners plan Various Economic Policies: Both Monetary and Fiscal policies.. GDP is  a key economic metric in diagnosing and measuring the Health of an Economy. However, it can be difficult to predict and forecast GDP growth rates. We want to see ML models like XG-Boost play a role in helping predict and Forecast GDP Growth Rates.

## Model Card for GDP Growth Prediction using XGBoost
### Model Overview
- **Model Name:** GDP Growth Prediction using XGBoost
- **Version:** 1
- **Date:** 03/15/2025
- **Authors:** Irti Haq, Sanjana Kumar

### Model Description
- **Purpose:** This model is created to predict the GDP growth for the OECD and BRICS countries.
- **Architecture:** A hyperparameter-tuned XGBoost architecture is used for this model
- **Framework:** XGBoost

### Training Data
- **Dataset Used:** World Bank Data (wbgapi)
- **Data Source:** https://blogs.worldbank.org/en/opendata/introducing-wbgapi-new-python-package-accessing-world-bank-data
- **Data Characteristics:**
  - Features: These feature selections were based on the learnings from    
    1. Qureshi, S., Chu, B. M., & Demers, F. S. (2020). Forecasting Canadian GDP growth using xgboost (No. 20-14). Carleton University, Department of Economics.

    2. Adewale, M. D., Ebem, D. U., Awodele, O., Sambo-Magaji, A., Aggrey, E. M., Okechalu, E. A., ... & Oluyide, O. P. (2024). Predicting gross domestic product using the ensemble machine learning method. Systems and Soft Computing, 6, 200132.

```
    "FP.CPI.TOTL.ZG": "Inflation (CPI annual% %)",
    "SL.UEM.TOTL.ZS": "Unemployment rate (%)",
    "NE.CON.PRVT.KD": "Household consumption (constant US$)",
    "NE.EXP.GNFS.KD": "Total exports (constant US$)",
    "NE.IMP.GNFS.KD": "Total imports (constant US$)",
    "BX.KLT.DINV.CD.WD": "FDI net inflows (current US$)",
    "FM.LBL.MQMY.CN": "Money supply M2 (local currency)",
    "CM.MKT.LCAP.CD": "Stock market capitalization (current US$)",
    "SP.POP.TOTL": "Total population",
    "SL.TLF.TOTL.IN": "Total labor force",
    "SP.URB.TOTL": "Urban population",
    "NV.AGR.TOTL.KD": "Agriculture value-added (constant US$)",
    "NV.IND.TOTL.KD": "Industry value-added (constant US$)",
    "NV.SRV.TOTL.KD": "Services value-added (constant US$)",
    "FP.CPI.TOTL": "Consumer Price Index",
    "NE.CON.GOVT.ZS": "Government consumption (real, % of GDP)",
    "NE.CON.PRVT.ZS": "Private consumption (real, % of GDP)",
    "BN.CAB.XOKA.GD.ZS": "Current account balance (% of GDP)",
    "SL.EMP.TOTL.SP.ZS": "Employment (% of total population)",
    "PA.NUS.FCRF": "Official exchange rate (LCU per US$, period average)",
    "NY.GDP.DEFL.KD.ZG": "GDP deflator",
    "NY.GDP.MKTP.KD.ZG": "Real GDP growth annual%l% %)",
    "NE.IMP.GNFS.ZS": "Imports (real, % of GDP)",
    "NV.IND.TOTL.ZS": "Industrial production index",
    "NE.GDI.FTOT.ZS": "Fixed investment (total, real)",
    "FI.RES.TOTL.CD": "Foreign exchange reserves (current US$)",
    'CM.MKT.LCAP.GD.ZS': 'Market capitalization of listed domestic companies (% of GDP)'
```
  - Number of Rows - 930


## Evaluation Metrics
- **Metrics Used:** RMSE and MAPE
- **Performance:**
  - Mean Squared Error: 13.564
  - Mean Absolute Percentage Error: 0.927

## Limitations
- This model is specifically created to work with the format of the World Bank dataset.
- We have seen that the model does not perform well in the case of some specific countries, though this could just mean that there was not enough data for these countries in the dataset.

## Usage
- **Installation:** The .ipynb notebook contains all necessary install statements. No additional installation is required.
- **Inference:** The final model is defined in the variable `best_model_proj`, which can be used for inference. For example:

```predictions = best_model_proj.predict(X_test)```
