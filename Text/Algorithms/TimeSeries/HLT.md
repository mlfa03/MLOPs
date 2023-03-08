## Holt's Linear Trend Method 

### Use Case 
* Forecasting data that has a trend 
* Holt’s Linear Trend Method (aka Double Exponential Smoothing) accounts for data that has a trend because it adds a second single exponential smoothing model to capture the trend (either upwards or downwards).
* 

### Method 
This method has 3 major aspects for performing the predictions. It has an average value with the trend and seasonality. The three aspects are 3 types of exponential smoothing and hence the hold winter’s method is also known as triple exponential smoothing.

* **Exponential Smoothing:** Simple exponential smoothing as the name suggest is used for forecasting when the data set has no trends or seasonality.
* **Holt’s Smoothing method:** Holt’s smoothing technique, also known as linear exponential smoothing, is a widely known smoothing model for forecasting data that has a trend.
* **Winter’s Smoothing method:** Winter’s smoothing technique allows us to include seasonality while making the prediction along with the trend.
* Holt winter’s method takes into account average along with trend and seasonality while making the time series prediction.
* It can handle the seasonality in the data set by just calculating the central value and then adding or multiplying it to the slope and seasonality


### Final Remarks
* One major limitation of this algorithm is the multiplicative feature of the seasonality. The issue of multiplicative seasonality is how the model performs when we have time frames with very low amounts. A time frame with a data point of 10 or 1 might have an actual difference of 9 but there is a relative difference of about 1000%, so the seasonality, which is expressed as a relative term could change drastically and should be taken care of of of when building the model.
