# Time-Series
Projects and learnings to analyze and create models with time series data


Exploratory Analysis and Time Series Preparation

This project involves the complete process of exploratory analysis and initial preparation of time series data, which is essential for building robust predictive models. Below are the main concepts applied:

📈 1. Time Series Decomposition
The time series was decomposed into trend, seasonality, and residual components.
This helps to understand the structure and patterns in the series over time and informs better modeling decisions.
- Time series smoothing technique
   - Moving Average
   - Exponential Smoothing
   - Smoothing Filter
   - Model-based decomposition
   - regularization method
     
- Seasonality detection
   - Fourier
   - ACF (Autocorrelation Function): measures the correlation between observations and their lags.
   - PACF (Partial Autocorrelation Function): measures direct correlation with lags, removing indirect influences.
   - The Augmented Dickey-Fuller (ADF) test was applied to check for the presence of a unit root (indicating non-stationarity).
Interpretation:
p-value < 0.05: the series is stationary.
p-value ≥ 0.05: the series is non-stationary.
   - Clustering or PCA
   - STL ( seasonal and trend decomposition using loess )
 
The Box-Cox transformation method and log transformations are powerful techniques
   - Both transformations help stabilize variance and make the distribution more normal, which is essential for many statistical models that assume data normality.

Cycle analysis

1.1 Purpose of Residual Analysis in Time Series
Residual analysis is a crucial step in time series modeling and validation (e.g., ARIMA, SARIMA, ETS). It helps assess whether the fitted model properly captures the underlying patterns in the data and whether key assumptions are satisfied.

A residual is defined as:

Residual = observed value – predicted value
The main goals of residual analysis are to check whether the residuals:

Are independent – no temporal patterns should remain (they should look like white noise).
Have zero mean – the average residual should be close to zero.
Are homoscedastic – the variance should be constant over time.
Follow a normal distribution – especially important for models relying on normality assumptions.

Common Methods of Residual Analysis
1. Residual Time Plot
2. Histogram of Residuals
3. Q-Q Plot (Quantile-Quantile)
4. ACF Plot of Residuals (Autocorrelation Function)
5. Ljung-Box Test
6. Durbin-Watson


📉 2. Stationary vs. Non-Stationary Series
A non-stationary series shows changes in mean, variance, or autocorrelation over time.
Most forecasting models require a stationary series with constant statistical properties throughout time.


🔄 3. Transformations to Achieve Stationarity
Applied transformations include:
First-order differencing to remove trend.
Log transformation to stabilize variance.
Trend or seasonality removal using methods like STL or seasonal decomposition.


📊 4. Distribution Analysis
Assessed the distribution of time series values (e.g., using histograms).
Calculated mean and median to observe distribution symmetry.
Important to understand if data follows a normal distribution, which can affect model choice.


📐 5. Hypothesis Testing
Statistical tests like ADF follow a hypothesis testing framework:
H₀ (null hypothesis): the series has a unit root (non-stationary).
H₁ (alternative hypothesis): the series is stationary.
The p-value determines whether to reject or accept H₀.


📉 6. AIC (Akaike Information Criterion)
Used to compare and select time series models such as ARIMA/SARIMA.
AIC penalizes models with more parameters.
Lower AIC values indicate better model fit with fewer assumptions.


✅ Initial Time Series Modeling Process Summary
Visualize the original series.
Decompose into components.
Test for stationarity using the ADF test.
Apply transformations to achieve stationarity.
Analyze ACF and PACF plots.
Select the model based on AIC and parameter significance (p-values).
