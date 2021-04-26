* here> writing log about the current experiment observation 
    * add content in validation, and write about hte following 
        * definition of "run"
            * A run is complete when all model is trained on training data. A concept of run is neccessary in
                time series prediction because of autocorrelation and temporal dependencies properties of the
                task allow test data to be added back to training after the test data is predicted by models.
                In the other word, test data can be converted to training data once test data is predicted.
                Therefore, if your task is to predict 1 test data, maximum run is limited by number of test
                data.
        * test_loss_per_run
            * test_loss_per_run is simply test loss. "per_run" suffix indicate that test_loss of new run will
                be concatenated to the test loss of previous run. This way we can observe performance of test
                on different number of runs. 
            * There are a flag to control behavior or test_loss_per_run, namely
                "evaluate_many_test_data_per_run."
        * val_loss 
            * val_loss (validation loss) does not track model performance on validation data. This is because,
                in the epidemic prediction task, data is limited. Instead, we use val_loss to test on test
                data. The different between val_loss and test_loss_per_run is that val_loss tracks
                model performance on test data on each epoch while test_loss_per_run predict tracks model
                performance on test data after a run is completed.
        * definition of step.
            * step = epoch * number of runs.
            * the concept of step is needed to compare experiments that use both epoch and run parameters.
        * and barplot
            * average of prediction on test data AFTER model has finished all the training.
