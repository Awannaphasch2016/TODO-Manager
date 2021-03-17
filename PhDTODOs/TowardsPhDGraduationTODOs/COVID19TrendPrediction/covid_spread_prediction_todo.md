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

* finished the following
    * Ray: A Distributed Execution Framework for AI | SciPy 2018 | Robert Nishihara
        * https://www.youtube.com/watch?v=D_oz7E4v-U0&ab_channel=Enthought 
    * Tutorial: Scalable model training with Ray Tune
        * https://www.youtube.com/watch?v=eAWUZJe571Y&ab_channel=SoftwareUnderground
    * Ray: A System for Scalable Python and ML |SciPy 2020| Robert Nishihara
        * https://www.youtube.com/watch?v=XIu8ZF7RSkw&ab_channel=Enthought
    * A Glimpse into the Ray Autoscaler by Ameer Haj Ali
        * https://www.youtube.com/watch?v=BJ06eJasdu4&ab_channel=anyscale
    * Distributed Deep Learning with Horovod on Ray - Travis Addair, Uber 
        * https://www.youtube.com/watch?v=rEB3NPUoxMM&ab_channel=anyscale

* what is /dev/sda1/
    * ref
        * https://superuser.com/questions/558156/what-does-dev-sda-in-linux-mean

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

# Waiting


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

# TODO

* learn ray auto scaling
    * configuring autoscaler for my use 
        * ref:
            * https://docs.ray.io/en/master/cluster/config.html#cluster-config
        * head nodes vs worker nodes.
            * what should head nodes have?
* run all the results
    * here> run linear regression and xgboost.

* figure out how to inspect remote node port 
* write a report on weight and biases. (and shared link to dr zhu)
    * here> list all the things I needs to write for report.
        * here> for feedback 
            * what is the current parameters for each baseline models
            * which models is the best?
            * data profiling.
                * pearson correlation 
                    * measure pearson correlation between 
                        * current week vs next week 
                        * traning set vs test set
            * explain how training and test work. 
                * make sure that I summarized how walk_forward_validation is done. 
                    * how do I separated traingig, test. 
                        * with the exact number of data nad length, ... etc.
        * further explains what I have done 
            * explains why distributed training + experiment tracking is needed 
                * explains about how I can use distributed training
                    * for any number of gpu and cpu.
                * explains that experiment tracking will be tracked on W&B.

* figure out XGboost bugs.
    * why XGboost have same performance?
        * see image in DrZhu/ 
* run hyperparameters optimization for all base line
* goal: speed up my keras code
    * figure out how to use ray autoscaler.
* create singularity container.
    * goal
        * so my project can be run anywhere including
            * cloud platofrm
            * HPC 
                * eg
                    * fau cluster
            * different workstation.


* learn ray autoscaler.
    * 

* figure out if i need to implement more baseline or not
    * eg
        * tgnn (transfer learning)
        * here> lstm
            * here>lstm with window sliding validation
            * send code to be trained in FAU HPC ()
        * gam
            * here> see pyGAM
                * read https://tomkealy.github.io/blog/time-series-with-gams/
        * arima
