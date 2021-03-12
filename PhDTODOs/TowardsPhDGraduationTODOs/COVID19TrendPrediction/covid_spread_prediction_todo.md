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

* multi-worker (multi-threaded) vs multi-processes vs multi-nodes
    * can I used them in combination?
    * when to use multi-worker in keras?

# Waiting

* ask people from fiver for gpu setup help

* learn how to use determined AI
    * here> can this fit in my gpu work flow?
        * here> read determined.ai documentation
            * note
                * each 
            * detemrined cli 
            * determined cluster

* can't use GPU
    * error
        *  Could not load dynamic library 'libcusolver.so.10'; dlerror: libcusolver.so.10: 
        *  Not creating XLA devices, tf_xla_enable_xla_devices not set
    * how to install cuda toolkit?
        * nvidia driver
    * where does added module attached to?

# TODO

* what is /dev/sda1/
    * ref
        * https://superuser.com/questions/558156/what-does-dev-sda-in-linux-mean

* here> how to train keras with 1 gpu?
    * here> login to my aws gpu online. 
        * compared using different strategy
        * here> figure out how to test cpu vs gpu speed of tf.keras.
            * here> is it really alot faster?  if so, by how much?
                * here> create MLP models.
                    * running 100 
                    * here> run 500 (only do it for ec2 cluster)
                        * here> how to turn on progress bar in keras?
                            * here> compare perforamnce of OneDeviceStrategy,MirrorStrategy,CPU. (on ec2)
                        * implement command line to predict only certain states.
                        * only train for 1 state
                            * here> for all predictnextN and windowLengthN. (train on my laptops locally is fine)
                        * do it in laptops then merge to ec2.
                            * read Why My Multi-GPU training is slow?
                                * https://medium.com/@c_61011/why-multi-gpu-training-is-not-faster-f439fe6dd6ec
                            * here> try switching strategy to OneDeviceStrategy.
                                * see if there is any speed up.
                            * here> if optimize for single/multiple gpu doesn't work when using tf.distributed,can I use ray (or horovod) to speed up distributed training.?
                            * error
                                * ade sure that all my datasets (train and val) have auto_shard_policy set to tf.data.experimental.AutoShardPolicy.DATA.
                                    * https://github.com/tensorflow/tensorflow/issues/42146#issuecomment-796802782
                                        * when to use tf.data?
                                            * ref 
                                                * https://www.tensorflow.org/api_docs/python/tf/data/experimental/DistributeOptions
                                            * what is tf.data.Dataset?
                                                * https://www.tensorflow.org/tutorials/distribute/input#tfdistributestrategyexperimental_distribute_dataset
                        * here> implement weight and biases to monitor models 
                        * figure out how to do checkpoint for deep learning model
                    * here> create delta_apply_model_to_all_states()

* goal: speed up my keras code
    * here> read the following 
        * here> tensorflow (tf.keras)
            * here> a distributed traingin with tensorflow
                * here> https://www.tensorflow.org/guide/distributed_training
                    * here> which strategy should I used?
            * multi-gpu and distributed training
                * https://keras.io/guides/distributed_training/ 
            * distributed training in tf.keras with weights & biases.
                * https://towardsdatascience.com/distributed-training-in-tf-keras-with-w-b-ccf021f9322e 
            * learn to optimize tensorflow GPU performance.
                * https://www.tensorflow.org/guide/gpu_performance_analysis
        * pytorch 
            * welcome to weights & biases - introduction walktrhough (2020)
                * https://www.youtube.com/watch?v=91HhNtmb0B4&ab_channel=Weights%26Biases
            * integrate weight * biases with pytorhc
                * https://www.youtube.com/watch?v=G7GH0SeNBMA&ab_channel=Weights%26Biases

* keras gpu vs cpu implementation
    * ref
        * multi-gpu and distributed training 
            * https://keras.io/guides/distributed_training/
    * implement it in Scratch/Example/Libraries/Keras/using_gpu.py
    * implement demo such that it can switch between gpu and cpu 
    * add to my code 

* pytorch gpu vs cpu 
    * implement it in Scratch/Example/Libraries/Pytorch/using_gpu.py
    * implement demo such that it can switch between gpu and cpu 

* add the following naming convesion
    * to distinguish run from 'fau_cluster' and 'laptops'
    * gpu vs cpu 
        * suffix

* try using weight and biases 
    * MLP 
        * which features should I use?
            * experiment tracking  
                * chart
                    * track the folloing 
                        * epoch + evaluation metrics 
                * system metrics
                * model metrics
                * standard out
                * files

* run models
    * run mlp with 2000 epoch

* create singularity container.
    * goal
        * so my project can be run anywhere including
            * cloud platofrm
            * HPC 
                * eg
                    * fau cluster
            * different workstation.

* can I install tensoflwo 2.4.1 on centos?
    * ref
        * fau support ticket
            * https://helpdesk.fau.edu/TDClient/2061/Portal/Requests/TicketRequests/
                * id 17251487
                * keras tensorflow incompatibility
            * ticket response
                * https://mail.google.com/mail/u/0/#search/OIT/FMfcgxwLsmhNDhqWLdHJfrtlNZQjVxfp 
    * how to install conda on centos?
        * error
            * PackageNotInstalledError: Package is not installed in prefix.
              prefix: /mnt/beegfs/home/awannaphasch2016/.conda/envs/py38
              package name: conda
    * here> try to reproduce the result and send list of command to resnick
    * try to use pyenv and pipenv
    * try to upgrade conda
        * if can't upgrade -> submit ticket -> move on to next task
        * if succesfully upgrade, but still can't fix the error -> submit ticket -> move on the next task


-- 3/10/2021 

* run hyperparameters optimization for all base line


* here> how to devleoep tensorflow with gpu and without gpu
    * lets implement lstm with keras and ternsorflow
        * gpu 
        * cpu

* here> how to devleoep pytorch with gpu and without gpu
    * lets implement lstm with keras and ternsorflow
        * gpu 
        * cpu

* run my project on the cloud. 
    * first just make it work
    * use signularity to run ( this way I can run the same thing on HPC cluster)
        * use sigularity to 
            * learn to use 
            * use pipenv and pyend inside singularity ( does this question make sense at all?)
                * learn about pipenv and pyenv

* here> deploy so professor zhu can see it.


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
