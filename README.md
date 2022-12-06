# Comparison_of_GARCH_variants_and_StochVol_Model
The various variants of GARCH available in the **rugarch** package along with the Stochastic Volatility Forecasting Model have been compared in this repository. **Considering the fact that market does not react to positive and negative news in the same way (there is more volatility when any bad news comes in as compared to the volatility on coming of any good news), Skewed Student t-Distribution has been used to model the Return process in the GARCH models.** There are 7 variants available for GARCH models in rugarch, namely **"sGARCH", "fGARCH", "eGARCH", "gjrGARCH", "apARCH", "iGARCH", and "csGARCH"**. Further, there are 8 sub-variants available for the fGARCH variance model, namely ** "GARCH", "TGARCH", "AVGARCH","NGARCH", "NAGARCH", "APARCH", "GJRGARCH", and "ALLGARCH"**.

The in-sample data consists of NIFTY50 daily (Adj. Closing Price) returns from "2007-09-18" upto "2020-12-31". The forecasting results have been backtested on the daily returns of 248 trading days of the year 2021. The VaR has been calculated on 90%, 95% and 99% confidence intervals for all models.

The following results have been obtained:
The top performers at 90% confidence interval are:
model	alpha(10%)
apARCH	91.53226
gjrGARCH	91.53226
csGARCH	91.53226
fGARCH_APARCH	91.53226
fGARCH_GJRGARCH	91.53226

The top performer at 95% confidence interval is:
model	alpha(5%)
csGARCH	95.96774

The top performer at 99% confidence interval is:
model	alpha(1%)
fGARCH_AVGARCH	98.79032

Stochastic Volatility Forecasting Model performed poorly at all three levels giving a meagre accuracy of 86.29% (breached 90% confidence bar 34 out of 248 trading days), an accuracy of 92.74% (breached the 95% confidence bar (18 out of 248 trading days) and an accuracy of 98.39% (breached 99% confidence bar 4 out of 248 trading days).
