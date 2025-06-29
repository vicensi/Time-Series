# Time-Series
Projects and learnings to analyze and create models with time series data


Exploratory Analysis and Time Series Preparation

This project involves the complete process of exploratory analysis and initial preparation of time series data, which is essential for building robust predictive models. Below are the main concepts applied:

📈 1. Time Series Decomposition
The time series was decomposed into trend, seasonality, and residual components.
This helps to understand the structure and patterns in the series over time and informs better modeling decisions.


📉 2. Stationary vs. Non-Stationary Series
A non-stationary series shows changes in mean, variance, or autocorrelation over time.
Most forecasting models require a stationary series with constant statistical properties throughout time.


🧪 3. Stationarity Test
The Augmented Dickey-Fuller (ADF) test was applied to check for the presence of a unit root (indicating non-stationarity).
Interpretation:
p-value < 0.05: the series is stationary.
p-value ≥ 0.05: the series is non-stationary.


🔄 4. Transformations to Achieve Stationarity
Applied transformations include:
First-order differencing to remove trend.
Log transformation to stabilize variance.
Trend or seasonality removal using methods like STL or seasonal decomposition.


📊 5. Distribution Analysis
Assessed the distribution of time series values (e.g., using histograms).
Calculated mean and median to observe distribution symmetry.
Important to understand if data follows a normal distribution, which can affect model choice.


🔄 6. ACF and PACF (Correlation Functions)
ACF (Autocorrelation Function): measures the correlation between observations and their lags.
PACF (Partial Autocorrelation Function): measures direct correlation with lags, removing indirect influences.
These plots guide the selection of optimal parameters (p, d, q) for models like ARIMA.


📐 7. Hypothesis Testing
Statistical tests like ADF follow a hypothesis testing framework:
H₀ (null hypothesis): the series has a unit root (non-stationary).
H₁ (alternative hypothesis): the series is stationary.
The p-value determines whether to reject or accept H₀.


📉 8. AIC (Akaike Information Criterion)
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
