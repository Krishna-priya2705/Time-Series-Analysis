
This R Shiny application is an interactive Time Series Analysis Tool designed to help users perform comprehensive time series modeling and diagnostics without writing code. The app features a clean dashboard layout using the `shinydashboard` package, enabling an intuitive and user-friendly experience.

Users begin by uploading a dataset in CSV or Excel format. Once uploaded, the app dynamically presents a dropdown for selecting the variable to be analyzed. A frequency input allows users to define the periodicity of the data (e.g., monthly = 12, quarterly = 4), which is essential for accurate time series construction.

Upon initiating analysis, the app performs several core time series tasks:
Time Series Plot and Decomposition Plot visualize the overall pattern and components (trend, seasonality, residuals).
Stationarity Testing is done using the Augmented Dickey-Fuller (ADF) test, with an interpretation message indicating if the data is stationary.
 Users can opt-in for additional analysis modules such as:
ACF and PACF plots to identify autocorrelations and help in ARIMA model selection.
SARIMA modeling using `auto.arima()`, including summary statistics, residual checks, Ljung-Box test, and normality test of residuals.
Smoothing techniques like Simple Moving Average, Exponential Smoothing, and Holt-Winters method for trend smoothing and forecasting.
GARCH modeling using the `rugarch` package to handle volatility clustering and time-varying variance.

All visual outputs are rendered dynamically using `ggplot2` and `forecast` libraries. Conditional panels ensure that only the user-selected analyses appear on the results tab, keeping the UI clean and responsive.

Finally, the app provides a PDF report download feature. By leveraging an R Markdown template, it generates a reproducible summary of the time series analysis, making it useful for presentations or documentation.

This tool is ideal for analysts, researchers, and students looking to explore time series data with ease and flexibility.
