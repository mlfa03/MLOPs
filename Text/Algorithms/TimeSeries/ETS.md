## ETS Time Series Models 

ETS stands for Error - Trend - Season. ETS models are designed to forecast time series data by observing the trend and seasonality patterns in a time series and forecasting them for future data to come.

A time series can be decomposed into: 
* Seasonal patterns
* General tendencies 
* Error 


![image](https://user-images.githubusercontent.com/39881974/223716468-92409524-96de-4a1b-a805-d8b0f74f7e1b.png)




### Trend plot

The Trend plot from the Time Series Decomposition helps us to decide the following:

* If the trend plot is linear then we apply it additively (A).
* If the trend line grows or shrinks exponentially, we apply it multiplicatively (M).
* If there is no clear trend, no trend component is included (N).


file:///home/mariana.almeida/Imagens/trend.png![image](https://user-images.githubusercontent.com/39881974/222714767-7ef00e45-418a-4872-838f-7ff36708fdd1.png)


### Seasonality plot

The Seasonal plot from the Time Series Decomposition helps us to decide the following,

* If the peaks and valleys for seasonality are constant over time, we apply it additively (A).
* If the size of the seasonal fluctuations tends to increase or decrease with the level of time series, we apply it multiplicatively (M).
* If there is no seasonality, it is not applied (N).

### Error plot 

The Error plot from the Time Series Decomposition helps us to decide the following,

* If the error plot has constant variance over time (peaks and valleys are about the same size), we apply it additively (A).
* If the error plot is fluctuating between large and small errors over time, we apply it multiplicatively (M).
* There is no case when we do not consider Error into account


### Cyclical patterns 


