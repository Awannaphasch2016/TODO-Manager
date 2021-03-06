# Notes
* what is suitable ec2 instance for machine leanring?
     * note: 
        * for our data science needs, we will most likely want to select something in the range of m5.large to m5.2xlarge, or a p2.xlarge for deep learning work. More details and pricing found here.

* how to run with fau cluster? (still don't have a way to use it)
    * how to send code to run with gpu?
        * using srun, 
            * usecase
                * you want to use srun when you want to run interactively.
                    * eg.
                        * `srun -p shortq7 --gres=gpu:1 --pty bash`
        * using sbatch,
            * usecase
                * sbatch can submit script, and you can continous your work.
                    * eg.
                        * `sbatch <sh file with #SBATCH>`
                            * this is a prefered method.
                                * #SBATCH only activate in slurm environment.
                        * `sbatch -p shortq7 --gres=gpu:1 <sh file without sbatch>`
# Question

# Optimization


* try running simple model from covid19trendcovid with fau cluster script
    * here> all use beta_apply_model_to_all_states
        * here> how to use predict_next_n_days in mlp?
    * run Models/previous_day_val_pred.py
    * run Models/lstm

* create a script to do the following
    * here> run hello_words.sh using setup_project_on_slurm
        * here> how to easily see content in s3 without opening it?
            * here> use streamlit to open file from s3.

* hdf5 and data compression related content 
    * read how i learn to love HDF5 Or How I Learned To Love Data Compression And Partial I/O
        * here> how is hdf5 related to sparse matric implementation?
    * doesn't seem like it is worth learning for my case 
        * here> try to complete the hdf5 kaggle 
            * https://www.kaggle.com/tanderton/hdf5-conversion-for-fast-data-loading
        * learn sparse matric
    * working with many dataset in machine learning project
        * hdf5 (with hiercical structure) vs h5py (data storage)?
        * here> whhen to use hdf5 ?
            * when to use hdf5
            * learn about hdf5
                * what small project to run? (deep learning related)
            * what is the common problem of hdf5?
            * how to load zip file to pandas without unzip it first? 
            * how to convert in-memeory dataframe to HDF5 using compression
            * sparse matrices make machine learning faster
    * figure out a way to manage files using hdf5
        * ref
            * https://stackoverflow.com/questions/59757016/keras-modelcheckpoint-overwrites-previous-best-checkpoint-when-training-resumed


* figure how to enable GPU
    * note
        * Window version
            * Window 10 Insider Preview 21318.1000 (rs_prerelease)
        * 
    * here> try to install Nvidia driver 
        * ref: 
            * use PyTorch and TensorFlow with an NVIDIA GPU in the Windows Linux Subsystem (WSL)
                * https://www.youtube.com/watch?v=mWd9Ww9gpEM
        * read documentation about nvcc
            * equivalent of TAsk Manager performance on linux?
                * here> GPU stress testing (no gui)

* how to run gpu on windows?
    * can I set up gpu to be run on windows?

* figure out how to plot 7 days ahead.
    * not important

# Waiting

* ask people from fiver for gpu setup help

* learn how to use determined AI
    * here> can this fit in my gpu work flow?
        * here> read determined.ai documentation
            * note
                * each 
            * detemrined cli 
            * determined cluster

* how to submit training jobs to Amazon SageMaker?
    * note
        * here> manage using SageMaker Python SDK
    * watch different people workflow on sagemaker
        * AWS live coding
            * https://www.youtube.com/watch?v=lO224Iec-uI&ab_channel=AmazonWebServices

    * learn AWS Deep Leanring AMIs
    * learn AWS Deep Learning Container (DLC)

* fau support ticket
    * https://helpdesk.fau.edu/TDClient/2061/Portal/Requests/TicketRequests/
        * id 17251487
        * keras tensorflow incompatibility

# TODO

* here> what is module in linux commnad?
    * same as centosOS?
    * how does module effect dynamic variable (aka environment variable)

* learn about pipenv and pyenv

* how to devleoep tensorflow with gpu and without gpu
    * setup
    * implementation

* how to devleoep pytorch with gpu and without gpu
    * setup
    * impementationJkw;

* here> can I install tensoflwo 2.4.1 on centos?
    * here> how to install conda on centos?
        * error
            * PackageNotInstalledError: Package is not installed in prefix.
              prefix: /mnt/beegfs/home/awannaphasch2016/.conda/envs/py38
              package name: conda
        * here> should I try to intall conda or just use virtualenv? 
    * what is the requirements?
    * what is tensorflow lastest version?

-- 3/5/2021 

* question
    * ref
        * https://phoenixnap.com/kb/how-to-install-tensorflow-centos
    * what version of keras is compatile with tensorflow 2.1
    * hwo can I upgrade tensorflwo to 2.2
    * what is my python version
* here> run model on fau cluster
    * here> run lstm 
        * here> write a script to run from fau cluster
            * here> install stuff
                * error
                    * here> keras required tensorflow 2.2 or higher.
            * write script for cluster
    * run mlp with 2000 epoch. 

* deploy so professor zhu can see it.
    * make sure file are search from s3 not local?


* expeirment monitoring 
    * goal: 
        * figure out a way to monitor large number of experiment for a project..
    * see exampel of weight and bias.
        * how is weight and bias use for minotoring purposed.
            * 10 mins
        * how cna I use weight and baises for my own project.
    * change epoch fo 2000.
    * figure out a way to monitor the project 
        * do i still need to manage file name by myself?
            * for filename of mlp. add hyperparameter and parameter as suffix after mlp
                * *_mlp_<parameters>_<hyperparameter>_*
* summarize of report about 1-5-7-30 days (prediction length)
    * requirement
        * model
            * all base line
        * eval metric
            * mse
* outline survey. 
    * eg
        * which type of methods to predict infection prediction for covid forecasting
* deploy 

-- 3/2/2021 5pm send to dr Zhu

* here> speed up my scripts
    * goal:
        * no need to optimize for anything just make it run.
    * here> run GPU on (windows -> koko cluster -> ec2)
        * here> run sample code with GPU in it. 
            * here> find simple GPU base deep learning model to run.
                * here> how to check srun is running gpu? 
					* here> try to run pytorch that use gpu.
                        * ref
                            * https://towardsdatascience.com/pytorch-switching-to-the-gpu-a7c0b21e8a99
                * create script to run nvidia-smi 
                    * check out what are availble modules that might activate nvidia 
                * implement pytorch that use GPU.
                    * here> run it on cluster (srun)
                * figure out best practice or easy way to convert CPU to GPU
                    * pytorch
                    * checkout humingbird.ml
                        * Error:
                            * error: RuntimeError: Found no NVIDIA driver on your system. Please check that you have an NVIDIA GPU and installed a driver from http://www.nvidia.com/Download/index.aspx
                                * here> hwo to check gpu from linux
                                    * here> check gpu with cuda toolkits
                        * goal:
                            * speed comparison
                        * model -> pytroch -> gpu
            * find simple GPU base deep learning model to run.
                * ray? 
                * rapid?
            * find simple cluster base deep learning model to run.
                * ray?
            * find simple cluster GPU based deep learning model to run. 
                * ray? 
                * Rapid?
            * measure training and inference speed of model
        * convert pandas to Dask

* send my code (start with lstm model) to be run on HPC.
    * save the following folder to s3.
        * Outputs/
        * Data/
    * send my code to be run on HPC GPU.
        * make sure I inkwo how to optimize code for GPU
            * can I use GPU on windows?

* use streamlit to show data easily 
    * here> show evaluation metrics on streamlit 
        * no need to deploy it. ( in case deploying it have speed differences)
    * design what I want to show on the dashboard
        * here> create hyperparameter tuning 
            * lets see what this is like
        * here> work on data profiling/sweetviz + streamlit
            * here> sweetviz
                * ref
                    * https://github.com/Jcharis/Streamlit_DataScience_Apps/tree/master/EDA_app_with_Streamlit_Components
    * deploy streamlit
        * requirement 
            * storage
                * put all Outpus content to s3 storage 
        * ref
            * deploy streamlit with heroku
                * here> https://towardsdatascience.com/deploy-streamlit-on-heroku-9c87798d2088
        * here> move Outputs/ to S3, so I can access it from my deployed application

* predict next 1/5/30
    * goal
        * decide on best performance window length
    * here> PredictNext=7
        * here> apply it to previous_day_prediction
            * here> validate that the follwing 
                * here> evaluation function 
                * plot are correct

    * PredictNext=30
    * put number matric on to streamlit
        * run streamlit


* implement the follwing as baseline
    * tgnn (transfer learning)
    * here> lstm
        * here>lstm with window sliding validation
        * send code to be trained in FAU HPC ()
    * gam
    * arima



* apply next day/3/5/week.
* parameter tuning

* try to set up debugging?
    * here> try to not use it until i relaly need to (train myself to simplified things for debugging)
* the model through all states
    * here> create a code that will run for all cases in Models/
        * here> apply it to all models
            * preivous day
            * LinearRegression
            * XGBoost
            * ' LSTM
            * ' MLP
            * ' GAM


* here> run the same model on state level dataset
    * note:
        * validation process
            * sliding window (train/val/test)
            * expanding window (train/val/test)
                * start with 85% (train-val) and 15% (test)

    * stochastic (random walk) basline
        * previous_day_prediciton
    * basic baseline
        * here> Autoregressive Integrated Moving Average (ARIMA)
        * Linear Regression
    * state of the art machine learning 
        * XGBoost (gradient boosting tree.)
    * statistical baseline model
        * here> GAM
            * here> see pyGAM
                * read https://tomkealy.github.io/blog/time-series-with-gams/
    * Deep learning baseline model
        * MLP
    * Deep learning time series baslines model
        * here> LSTM
            * save train data and then load it back
                * here> how to predict using checkpoint model
                    * here> read the following 
                        * https://machinelearningmastery.com/check-point-deep-learning-models-keras/
                            * here> how many option do i have for checkpoint?
                                * weight only and what else?
                                * how to load checkpoint?

* how to loop through the all the states?
* here> understand and run https://machinelearningmastery.com/xgboost-for-time-series-forecasting/ 
* implement GAM (generalized additive model) ?

* put survey on overleaf. (draft)
    * can I automate this?

* create baseline for the https://www.kaggle.com/anakwanna/covid-19-forecast-baseline-model/edit
    * Goal: focusing on showing what I have done.
    * here>understand detail + shape of train and test dataset.
        * what is the traning set that is used for LSTM model
        * when is train re-assigned.
    * what are baseline model for regression?
        * here> look at the papers that I have read, what are baselinesi that they used?
        * implement 2-3 more. (should have about 1 hour to complete all) 
            * option 
                * basic baseline
                    * Autoregressive (AR)
                    * here> Moving Average (MA)
                    * Autoregressive Moving Average (ARMA)
                    * Autoregressive Integrated Moving Average (ARIMA)
                    Exponential Smoothing (ES)
                * * deep learning baseline
                    * MLP
                * state of art machine learning 
                    * XGBoost (gradient boosting tree.)
                * statistical basline model
                    * GAM
            * selected: 
                * here> MA
                    * how to use MA to predict linear reegression?
                    * using the price of the previous day
                * MLP
                * XGBoost
                * GAM
    * once finish, with the global dataset work on USA datase
    * should I refer to the paper I read and see what is the next direction i need to do?  
* figure out how to intepret ARIMA and understand the following does
    * https://www.kaggle.com/anakwanna/covid-19-forecast-baseline-model/edit
* learn basic of time series 
    * https://www.youtube.com/watch?v=DeORzP0go5I&list=PLvcbYUQ5t0UHOLnBzl46_Q6QKtFgfMGc3&ab_channel=ritvikmath
        * what are the list of topic I need to know? 
            * https://www.quora.com/What-math-do-you-need-for-time-series-forecasting
            * overview of time sereies forecasting model
                * https://towardsdatascience.com/an-overview-of-time-series-forecasting-models-a2fa7a358fcb
            * introduction to time series
                * https://towardsdatascience.com/time-series-introduction-7484bc25739a
* finish the follwoing excercise within 2 horus 
    * https://www.w3resource.com/python-exercises/pandas/groupby/index.php  
