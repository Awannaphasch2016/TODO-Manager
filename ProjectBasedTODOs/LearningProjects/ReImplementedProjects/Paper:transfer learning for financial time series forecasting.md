# dataset
* first dataset 
    * source data 
        * hang seng commerce & industry (HSNC, 1000 time points)
        * hang seng commerce properties index (HSNP, 1000 time points)
    * target data 
        * hang seng commerce finnance index (HSNF, 1000 time points) 

* third dataset
    * source data
        * S&P 500 (GSPC) 
        * Nasdaq (IXIC)
    * target data
        * Dow 30 (DJI)

# TODO
* model implementation  
    * just use DNN
    * parameters setting
        * 90 days to predict next day
        * 70-30 split.
    * model architecture
        * DNN 
            * 2 layers
            * 256 per layers
            * tanh activation function
            * output layer continas one unit with linear activation function.
* here> download data.
    * lastest 1000 data point.
