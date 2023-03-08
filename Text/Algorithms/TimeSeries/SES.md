## Simple Exponential Smoothing Method 

### Use case

Time series does not have a trend line and does not have seasonality component. We would use a Simple Exponential Smoothing model.


### Method 

* Forecast is calculated by multiplying past values by relative weights, which are calculated based upon what is termed a smoothing parameter (alpha).
* Alpha is the magnitude of the weight applied to the previous values, with the weights decreasing exponentially as the observations get older.
* The smoothing parameter can be set for any value between 0 and 1.
* If the smoothing parameter is close to one, more recent observations carry more weight or influence over the forecast (if α = 0.8, weights are 0.8, 0.16, 0.03, 0.01, etc.).
* If the smoothing parameter is close to zero, the influence or weight of recent and older observations is more balanced 

#### About the smoothing parameter 
* Choosing the correct smoothing parameter is often an iterative process. 
* Advanced statistical tools, like Alteryx, will select the best smoothing parameter based upon minimizing forecasting error. Otherwise, you will need to test many smoothing parameters against each other to see which model best fits the data.

### Final Remarks 
* The advantage of exponential smoothing methods over simple moving averages is that new data is depreciated at a constant rate, gradually declining in its impact, whereas the impact of a large or small value in a moving average, will have a constant impact. 
* However, this also means that exponential smoothing methods are more sensitive to sudden large or small values.
* The simple exponential smoothing method does not account for any trend or seasonal components, rather, it only uses the decreasing weights to forecast future results. 
* **This makes the method suitable only for time series without trend and seasonality.**
