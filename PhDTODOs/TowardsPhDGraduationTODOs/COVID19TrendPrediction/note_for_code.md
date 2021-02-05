# REFERENCES
# TERMINOGLOY

* statsmodel.tsa.statools.addfuller()
    * Dickey-Fuller unit root test.
        * definition
            * test with null hypothesis of the Augmented Dickey-Fuller is that there is a unit root,
             with the alternative that there is no unit root 
        * usecase
            * can be used to test for a unit root in a univariate rocess in the presense of serial correlation	

##variables
* ts? 
    * time seires data started at case > n  with rolling mean of m
* tsC
    * ts for 'ConfirmedCase'
    * tsC1 (China)
    * tsC2 (US)
    * tsC3 (Italy)
    * tsC4 (Spain)
    * tsC5 (Germany)
    * tsC6 (India)
* NtsC
    * numpy array tsC with shape (-1,1)

## Functions/methods
* statsmodel.tsa.statools.addfuller()
    * Dickey-Fuller unit root test.
        * definition
            * test with null hypothesis of the Augmented Dickey-Fuller is that there is a unit root,
             with the alternative that there is no unit root 
        * usecase
            * can be used to test for a unit root in a univariate rocess in the presense of serial correlation



# NOTE
* list of evaluation metrics 
    * MAPE (Mean absolute percentage error) 
    * MSE (mean square error)
    * RMSE (Root Mean Square error)
    * r2_score
* configuration setup for models
    * baseline model
* discussion + performance summary on models
    * baseline model
        * ARIMA
            * predicted value is higher than real
        * LSTM
            * predicted value is lower than real
        * MA
        * today's value (to predict next day)
        * generalized additive model (GAM)
        * XGBoost 

# FREQUENTLY ASKED QUESTIONS
* about Data
    * why should one use rolling mean for train/test time series data?
    * what is the train test split?
        * train on frist 0.85% and test on the last 15%
    * how do you predict the next value?
        * train 5 days predict 1 day (train 7 predict is 1 better?)
    * what are the list of evaluation metrics? 
        * MAPE (Mean absolute percentage error) 
        * MSE (mean square error)
        * RMSE (Root Mean Square error)
        * r2_score

