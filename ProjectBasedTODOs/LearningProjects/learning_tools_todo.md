# NOTES
* workflow of data science project
    1. Discovery (25%)
    2. Exploration ( 10%)
    3. Model dev & productionalization ( 40%)
    4. Visualizaiton & communication (10%)

* data discovery + metadata engine
    * Amundsen
    * data discover at facebook

* pandas profiling
    * here> learn how to read pandas profiling report
        * here> can I pipeline output to filter out time series data for each state?
            * here> consider using pandas profiling with other tools such as 
                * here> grep/sed/awk, visidata, pandasshell
                    * here> use sed to filter for match column -> to an tmp filde (tmp/tmp.csv) -> pandasprofiling
                    * use visidata to filter only states data from florida
                    * use pandasshell
    * ToC
        * basic 
            * type, unique value, missing value
            * most freq value
            * type inference
        * stats
            * quantile stats
            * descriptive stats
            * correlations
        * visualization 
            * histogram
        * analysis
            * missing values
            * text analysis
            * file and image analysis
        * hyper parameters

* data exploreation 
    * pandasGUI?
    * visidata vs pandashell
        * how are they different?
            * pandashell focus on combining basic command including awk, sed, grep
        * visidata
            * ref: https://www.visidata.org/docs/
                * loading data 
        * pandashell
            * ref: https://github.com/robdmc/pandashells
            * ToC
                * Tool description
                * dataframe manipulation
                * join files on key fields
                * visualization tools
                * Spectral estimation
                * linear regression
                * profiling utilities

# REFERENCES
# REQUIREMENTS

* here> get overview of ways taht people implement streamlit 
    * here> create streamlit app.
        * here> to replace jupyter notebook workflow
            * note:
                * example of possible workflows
                    * Run long running backtest/ simulation and save results to file(s).
                    * Let user select file(s) and validate input/ output if needed.
                    * Let user select file(s) and provide interactive analytics to end user based on simulation results.
            * for general use case (can this be imeplemneted as separated github repo? microservice approach?)
            * here> streamlit + pandas profiling + sweetviz
                * note: 
                * requirements:
                    * user requirement
                        * user can use it to explore data
                        * user can use it to visualize data
                        * here> user can share app among team member
                            * here> use Streamlit Sharing
                                * reference:
                                    * https://blog.streamlit.io/deploying-streamlit-apps-using-streamlit-sharing/
                                    * https://medium.com/@thom.e.lane/streamlit-on-aws-a-fully-featured-solution-for-streamlit-deployments-ba32a81c7460
                                * here> figure out a way for data to be viualized/epxlore once it is deployed online
                                    * pull data from cloud service S3
                                        * call bucket 'streamlitdata'
                    * system requirements 
                        * same profiling of individual dataframe or comparison between dataframe should be downloaded once.
                            * note: 
                                * before implement this requirement, make sure that generating delay is large enough to be cumbersome to work with.
                            * program must be able to detect whether profile of the input data already exists.
                                * how can this be done?
                                    * each generated profile should have metadata attached.
                                        * detect file name suffix/prefix
                                            * doesn't garantee its content
                                        * detect number of columns + number of rows
                                            * doesn't garantee data indexed by (row, columns) position
                                        * compare dataframe directly
                                            * faster or slower than generated another html?
                                            * use DataFrame equals()
                        * the system can show analysis for each states
                            * Given a selected state, one can inspect features
                            * Given a selected state, one can compare features.


# OPTIMIZATION
* what is sysmtemd ?
    * tragidy of sysmtemd?
        * https://www.youtube.com/watch?v=o_AIw9bGogo&ab_channel=linux.conf.au 
# WAITING
# TODO
* setting workstation
    * You could access by using Docker when using WSL 2.
        * ref
            * https://docs.nvidia.com/cuda/wsl-user-guide/index.html#setting-containers
    * update my BIOS
        * hardware driver 
            * bios
                * ref
                    * http://drivers.razersupport.com//index.php?_m=downloads&_a=viewdownload&downloaditemid=4073&nav=0,350,992,1004
    * here> check 'pyenv'+ 'pipenv'
        * comment from franciscojossol
            * >  # Normally you have to use Pyenv in order to install all the versions you need for your local environments
            * ❯ # Then, you could setup local environments just by creating a Pipfile in a folder and
            * ❯ # Using pipenv for completing its configuration, selecting the Python version you want to use.
            * ❯ # Maybe you want to use Python 3.8 in a folder and Python 3.5 at the other.
            * ❯ # Tensorflow is not compatible with all of them.
    * Choco package manager for windows
    * rCUDA
        * remote CUDA
        * using a remote GPU by providing a DLL to connect to remote GPU.
        * example 
            * You have a powrfule GPU i nFrance, but you use a Huawei laptop in Russia. then you would liek to use your GPU (hwich you ahvei n fRAnce) form russia as if it was installed on your laptop
    * MPI
        * similar to determined AI
    * synthetic cluster
        * testing program that run on cluster
    * Fan and Turbo for heat management Raer laptop
    * apt-fast
    * systemctl
    * OpenMP + MPI + CUDa  + OpenCL
    * mult
