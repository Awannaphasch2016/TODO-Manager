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

* docker vs sigularity 
    * do i need sigularity at all? ( in which situration would I have to switch from docker to signularity)
        * create singularity container.
            * goal
                * so my project can be run anywhere including
                    * cloud platofrm
                    * HPC 
                        * eg
                            * fau cluster
                    * different workstation.

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

* learn ray auto scaling
    * configuring autoscaler for my use 
        * ref:
            * https://docs.ray.io/en/master/cluster/config.html#cluster-config
        * note
            * docker vs setup_commands
                * use docker to pull existing image.
                * for custom configuration that is not provided by exiting image, we can use setup_commands.
        * head nodes vs worker nodes.
            * what should head nodes have?
        * here> figure out docker image that I can use. (do i even need it)
            * what is docker image for data scientist project?
                * pytroch project?
                * conda project
                * tensorflow project?
                * ray project?
                * 
            * here> try running docker image (practice, so I can distinguish which error is docker and which is from ray autoscaling)
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

* here> build a graph
    * ref
        * visidata
            * video
                * youtube.com/watch?v=Ozap_numsjI&list=PLxu7QdBkC7drrAGfYzatPGVHIpv4Et46W&index=3
            * summarize
                * https://jsvine.github.io/intro-to-visidata/basics/summarizing-data/
            * graph
                * https://www.visidata.org/docs/graph/
    * how to do cluster analysis?
        * apply basic cluster analysis
            * ref
                * dynamic virtual graph significnacne network for predicint influenza
            * way 1 
                1. split each time series into nubmer of windows
                2. for each time series, cluster each window into groups.
                    * create a full table 
                3. for all time series, cluster each window into groups.
                    * rank highest correlation and show top n.
            * way 2
                * the same as way 1, but apply the following model to raw data 
                    * 2 layers mlp (256) with ELU
            * way 3 
                * way 1 and 2, but create tree based on events including the following
                    * policy 
                    * vaccine
            * way 4
                * begin at way 3 
                * For each group, create a mean of each member in a group
                * For each group, create a mean of rolling mean of each member in a group.
        * analyze cluster result to real data/event/trigger.
    * here> lets do data analysis of the dataset.
        * see "interplay.." paper
        * here> inter-temporal correlation.
            * here> n * n matrix
                * here> goal is to group date and state of 7 days and apply correlation.
                    * here> for each week, apply correlation to all states.
                        * ref
                            * see https://stackoverflow.com/questions/54023650/finding-correlation-of-dataset-with-multilevel-column
                        * here> create a linear plot that include variance
                            * here> try to redo the whole workflow using cmd instead of pandas.
                                * here> which one of the command line tools can I used?
                                * save multiindex pandas output into file then use command line to plot
                               * time-seires box plot.
        * intra-temporal correlation.
            * pearson correlation week by week. 
                1. compute correlation for all pair of each week. 
                2. bar plot week by week.
        * correlation between features.

    * what is the best possible way to create a graph?
        * what are dataset availble.

* read about transfer learning
    * what is area of research of transfer learning 
        * transfer learing for regression
        * embsemble transfer learning

* check if I need to fix run set in my report to be aligned with discription?
    * link it to table of content
    * figure out a way to organized experiments log.
        * naming convention?
            * eg Experiment/<point of disscussion>/<model>_<params>/
                * eg <point of discussion> = observations
    * refactor experiments into log dated 3/16/2021
        * does content itself needs to be refactored?
    * does info irrelevant? is it outdated?
        * if yes, remove it
        * if no, add more description/explaination given the run set. 
            * then figure out how to freeze run. (so future result cannot be added)

* how to implment logbook in wandb
    * ToC
        * I should Have table of Content to manay my prefix title .
            * eg. weekly update, report, log.
    * components of each log
        * background
            * what is the goal of the experiment?
                * what is your hypothesis of this experiment?
            * what is the movtivation of the experiment?
                * with references.
        * experimental apparatus and procedures
            * document "how you are doing it" not just "what you are doing"
                * documents all components required to reproduce the current experiment
                    * tools that you have used.
                        * eg. requirements.txt. (this should easily be tracked by going to history log on github)
                    * parameters + hyperparameter + models
                    * dataset
                    * evaluation metrics
        * dates and times
            * write it at the beginning of each log
            * write it at the beginning of important + interesting finding.
        * Data and observations
            * does the data make sense and why?
            * what quality assurance check have you performed to catch possible mistake early?
            * how is data visualized and labeled?
        * data analysis
            * describe step that I used to perform current data analysis.
            * document uncertainties 
                * random uncertainties
                * systematic uncertainties
                * or mistake caused by incorrect code implementation.
        * thought
            * what is your thought on the experiment?
            * future direction?
                * things that you want/need to explore further.
            * challenges?
            * improvement?
            * confusion?
                * things that you don't understand 
                * things that you need learn before you can fully understand your confusion.

* fix other minor error that I see from wandb
    * eg.
        * failed models. 
            * what is qualified as a failed model in wandb?
        * figure out error when running.
            * error
                * sklearn.r2score()
                    * ValueError: Input contains NaN, infinity or a value too large for dtype('float32').
            * parameter that cause error
                * see wandb log 
                    * /home/awannaphasch2016/Documents/Working/COVID19TrendPrediction/wandb/run-20210319_020807-1l9xixtr/logs/debug.log


* figure out XGboost bugs.
    * here> why XGboost have same performance?
        * here> see image in DrZhu/ 


* run all the results ( locally)
    * here> run linear regression and xgboost.

* figure out a way to report performance.  
    * here> evaluation metrics should provide the following information 
        * here> which models is better (aggregate result for all state)
            * here> aggreate mse for all states.
                * here> do in need to normalized it?
                    * here> does performance of all states have high variance?
                        * here> normalized results given each state by factors/features that cause high variance.
* set up 4 gpu + 32 cpu instance and run progam in it 
    * here> figure out how to inspect remote node port 
    * run hyperparameters optimization for all base line

* how to log distribute?
    https://www.datadoghq.com/blog/python-logging-best-practices/

* here> write a report on weight and biases. (and shared link to dr zhu)
    * here> how to freeze chart to the current result.
    * outlineing things to write. make it a separate report.
        * sort result by the following
            * states
            * PredictNextN
            * WindowLengthN
            * PredictNextN
                * models (aggree with PredictNextN ranking?)
            * WindowLengthN
                * models (aggree with WindowLenthN ranking?)
        * data profiling.
                * pearson correlation 
                    * measure pearson correlation between 
                        * current week vs next week 
                        * traning set vs test set

    * here> list all the things I needs to write for report.
        * here> for feedback 
            * what is the current parameters for each baseline models
                * what is the parameters names for the following.
                    * xgboost
                    * linear regression
                    * lstm
                    * mlp
            * which models is the best?
                * aggregate over PredectNextN, WindowLengthN.
            * which states perform best?
            
