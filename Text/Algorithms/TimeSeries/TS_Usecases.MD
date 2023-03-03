## Time Series Use Cases 

Depending on the application, different time series models are recommended. 

For the cases in which the underlying mechanisms are too complicated or unknown, such as:
* Retail sales 
* Stock market 

It is bettwer to apply a simple statistical model, such as:
* Autorregressive models (ARIMA, SARIMA ...)
* Exponential smoothing methods (holt winters)
* Theta method 

When interpretatiblity is not a priority, machine learning methods can be implemented: 
* QRF (quantile regression forests) 
* RNN (Recurrent Neural Networks) 
* GMB (gradient boosted trees)
* SVR (supported vector regression)
* Gaussian Process Regression 

### Uber 

To make choosing the right forecasting method easier for our teams, the Forecasting Platform team at Uber built a parallel, language-extensible backtesting framework called Omphalos to provide rapid iterations and comparisons of forecasting methodologies. 
