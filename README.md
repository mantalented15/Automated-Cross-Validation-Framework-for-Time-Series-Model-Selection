# Automated-Cross-Validation-Framework-for-Time-Series-Model-Selection

Created an automated framework for a demand forecasting problem to choose the best performing model on a weekly basis.

The models considered are:
1) Facebook Prophet
2) Moving Average
3) Simple Exponential Smoothing
4) Holt Winter's 
5) ARIMA


**High Level Process Flow:**
![Screenshot 2021-09-27 at 11 00 58 AM](https://user-images.githubusercontent.com/20403651/134850134-10abf967-bbd4-4607-96f3-9c505276c95a.png)

Backtesting:

Backtesting is the time series equivalent of cross-validation. It is an attempt to bootstrap the data in such a way that we can estimate the expected test error. We cannot use cross-validation directly since this is sequenced data. Order must be respected to avoid peeking.

In Expanding Window, we expand the training size from some starting size to a maximum size. This method provides a good balance between creating enough training-test pairs while maximizing the amount of data your models receive.

![Screenshot 2021-09-27 at 11 03 55 AM](https://user-images.githubusercontent.com/20403651/134850401-d78ef4c4-f077-4b9d-b6c3-39378275710f.png)
