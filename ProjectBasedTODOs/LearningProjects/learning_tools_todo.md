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

* here> what can visidata do?
    * things I still need to learn
        * basic
            * edit Contents 
            * aggregation
            * Grouping data and sdescriptie statistics
                * https://www.visidata.org/docs/group/
    * what is data toolkit?
    * what is data visualization?
    * Toc
        * basic features 
            * Loading Data
                * 1 file 
                    * specifying a source file
                * multiple file 
                    * Loading multiple dataset simutanaeiously
                    * Accessing other loaded or derived sheets
                    * converting a dataset from one supported filetype into another 
                * pandas
                    * Loading sources upoported by pandas
                * R 
                    * Opening an R data frame with Visidata
            * Navigation
            * Rows
            * Columns
                * basic
                    * how to hide (remove) and unhide (return) columns
                    * how to unhide columns
                    * how to speciy column types
                    * how to format columsn
                    * hwo to split a column
                    * how to substiture text in column
                * advance
                    * how to expands columns that contain nested data
                    * how to create derivative columns
                    * how to condigure multipel columns
            * Editing contents
            * Groiuping data and descriptive statistics 
        * other features 
            * Creating sheets, rows and columns
            * combining dataset
            * Drawing graphs 
            * How to save and replay a visiData session
        * customize
            * Customizing visidata 
            * Plugins - extending Visidata functionality
                * visidata plugins
                    * https://github.com/a
                        * here> vds3
                            * using vd with s3
        gan/visidata-pluginsr advance 
            * Developing a loader 
            * STDOUT pipe/redicrect

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
        * MPI product for deep learning
        * what is Horovod?
    * synthetic cluster
        * testing program that run on cluster
    * Fan and Turbo for heat management Raer laptop
    * apt-fast
    * systemctl
    * OpenMP + MPI + CUDa  + OpenCL
    * pytorch
        * work hands-on the following
            * speed up your algorithm (series)
                * https://towardsdatascience.com/speed-up-your-algorithms-part-1-pytorch-56d8a4ae7051
            * Distributed Deep Learning with Horovod
                * https://towardsdatascience.com/distributed-deep-learning-with-horovod-2d1eea004cb2 
            * pytorch in HPC 
                * https://researchcomputing.princeton.edu/pytorch 
        * read about the following
            * pytorch 
                * distributed training
                    * torch.dist.DistributedParallel
                * multi-GPU training
                    * torch.nn.DataParallel
                * torchscript
            * what is cudNN?
            * what is benchmarking library?
            * Horovod on Ray 
                * https://www.youtube.com/watch?v=rEB3NPUoxMM&ab_channel=anyscale 
            * HPC is dying, and MPI is killing it
                * https://www.dursi.ca/post/hpc-is-dying-and-mpi-is-killing-it.html
            * here> ray with slurm 
                * https://docs.ray.io/en/master/cluster/slurm.html
            * pytorch with lsurm
                * https://www.google.com/search?q=pytorch+with+slurm&rlz=1C1CHBF_enUS941US941&oq=pytorch+with+slurm&aqs=chrome..69i57.4724j0j7&sourceid=chrome&ie=UTF-8
            * pytroch multi processing
                * ref
                    * github
                        * https://github.com/pytorch/examples/tree/master/mnist_hogwild
                    * doc 
                        * multiprocessing best practice
                            * https://pytorch.org/docs/stable/notes/multiprocessing.html
            * CPU threading and torchscript inference
                * ref
                    * https://pytorch.org/docs/stable/notes/cpu_threading_torchscript_inference.html
            * performance tuning
                * https://pytorch.org/tutorials/recipes/recipes/tuning_guide.html
            * doing deep learning in parallel
                * https://esciencegroup.com/2020/01/08/doing-deep-learning-in-parallel-with-pytorch/
            * torch script + pytorch JIT?
                * https://www.youtube.com/watch?v=2awmrMRf0dA&ab_channel=PyTorch
        * parallelism  
            * multi-core, multi-thread
            * GPU
            * 1 computer vs HPC
        * distributed 
            * GPU
            * 1 computer vs HPC

* data visualization
    * spark (sparkline tools)
        * https://github.com/holman/spark/wiki/Wicked-Cool-Usage
            * here> display stock data for S&P500
                * differnet betwen curl and wget? 
                    * https://daniel.haxx.se/docs/curl-vs-wget.html
                        * how to pipe curl
                            * here> https://stackoverflow.com/questions/5427454/how-do-i-pipe-or-redirect-the-output-of-curl-v/5427484
    * termgraph
        * work on the following esxmple 
            * https://github.com/mkaz/termgraph


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
* learning about Autotools
    * here> what is autotools?
        * ref
            * video
                * https://www.youtube.com/watch?v=4q_inV9M_us&ab_channel=DavidA.Wheeler
            * article
                * https://www.gnu.org/software/automake/manual/html_node/Autotools-Introduction.html
                * https://opensource.com/article/19/7/introduction-gnu-autotools
                * https://en.wikipedia.org/wiki/GNU_Autotools
        * hwo to use sh?

* learn grep/awk/sed/ etc from this guy video
    * here> https://www.youtube.com/channel/UCOmCxjmeQrkB5GmCEssbvxg 

# WAITING
# TODO

* what are machine learning on graph library in python ?
    * does all machine learning on graph library support graph database?
    * stellargraph.
        * https://stellargraph.readthedocs.io/en/stable/demos/connector/neo4j/cluster-gcn-on-cora-neo4j-example.html
        * https://stellargraph.readthedocs.io/en/stable/demos/
        * https://www.google.com/search?q=neo4j+gcn&rlz=1C1CHBF_enUS941US941&oq=neo4j+gcn&aqs=chrome..69i57.2186j0j7&sourceid=chrome&ie=UTF-8
    * Graph Nets
    * here> DGL
        * ref
            * DGL + GNN
                * https://www.amazon.science/videos-webinars/learning-graph-neural-networks-with-deep-graph-library

* inside-terminal
    * ref
        * data science at command line .
            * https://www.datascienceatthecommandline.com/1e/chapter-9-modeling-data.html#running-the-experiment
    * speed up run time
        * learn parallel pipelines chapter from "data science at command line"
    * modeling 
        * dimensionality reduction
            * learn tapkee
        * classification
            * learn BigML
        * online learning
            * learn vowpal wabbit 
                * youtube
                    * https://www.youtube.com/watch?v=gyCjancgR9U&ab_channel=YuryKashnitsky
                    * https://www.youtube.com/watch?v=N-x86zHUDaI&ab_channel=MicrosoftResearch
                * article
                    * https://github.com/VowpalWabbit/vowpal_wabbit/wiki
    * tools for graph 
        * data format for graph is in different format standard
            * ref
                * article
                    * convert csv file to graphml
                        * https://qizeresearch.wordpress.com/2013/11/21/converting-csv-file-to-graphml-format-for-graph-mining-for-unweighted-and-undirected-graph/
                * conference talk
                    * why graph database?
                        * https://www.youtube.com/watch?v=GekQqFZm7mA&ab_channel=CodingTech 
            * csv 
            * GraphML
        * [selected] Amazon Neptun
            * note
                * Neptune uses DGL
            * ref
                * article 
                    * tutorial
                        * Neptune ML + GNN
                            * https://julsimon.medium.com/a-primer-on-graph-neural-networks-with-amazon-neptune-and-the-deep-graph-library-5ce64984a276
        * neo4j shell
            * section from a book.
                * https://subscription.packtpub.com/book/big_data_and_business_intelligence/9781783287253/1/ch01lvl1sec14/importing-data-from-the-csv-format-to-neo4j
            * neo4j for data science
                * https://neo4j.com/developer/graph-data-science/node-classification/
    * learn MLOps from tutorial 
        * ref
            * youtube.com/watch?v=UbL7VUpv1Bs
            * learn how to use DVC (Data Versioning Control)
                * https://github.com/iterative/dvc

    * note taking tools base on commandline 
        * zk
            * https://github.com/mkaz/zk
                * the author use the following to syncning between computer using instead
                    of google-drive etc.
                    * https://syncthing.net/ 

    * here> learn gnuplot and feedgnuplot
        * here> work on the following example 
            * here> https://github.com/dkogan/feedgnuplot
        * https://medium.com/introduction-into-bash/gnuplot-plot-albert-einstein-with-terminal-15dd8ea9ae91
        * https://www.youtube.com/watch?v=-jR64x8SHLk&ab_channel=StillpointX
        * find a list of script to do plots
            * https://www.google.com/search?q=gnuplot+script+for+data+science&rlz=1C1CHBF_enUS941US941&oq=gnuplot+script+for+data+science&aqs=chrome..69i57j33i299.10645j0j7&sourceid=chrome&ie=UTF-8
            * see https://github.com/dkogan/feedgnuplot/blob/master/guide/guide.org 
            * here> heat matrix
                * here> gnuplot script
                    * https://stackoverflow.com/questions/17543386/pipe-plot-data-to-gnuplot-script
                    * here> https://riptutorial.com/gnuplot/example/14015/simple-script-file
                * heatmap
                    * http://gnuplot.sourceforge.net/demo_5.2/heatmaps.html 
                        * figure out how to use gnuplot script.
            * histograms
            * bar/pie cahrts
            * scatter/lines plots 
            * tiems siers
            * relationship maps
            * geo maps
            * 3-D plots 
            * higher-ddeminsion plots
            * word clouds

* learn how people use gist?
    * goal 
        * use gist as a snippet storage to use across machine.
            * can I just use s3?
    * ref
        * https://www.liquidweb.com/kb/little-known-ways-to-utilize-github-gists/
* learn Unix programming
    * ref
        * art of unix programming
            * http://catb.org/~esr/writings/taoup/
* here> read https://www.datascienceatthecommandline.com/2e/chapter-7-exploring-data.html#bar-chart 

* learn data science at the command line
    * https://github.com/jeroenjanssens/data-science-at-the-command-line
        * note
            * vnlog for tabular data  
                * it is as flexible as awk, before it is awk's wrapper
            * q for query data
            * xsv for csv
            * miller for tabular
            * jq for jason
            * feedgnuplot and rush for visualization 
                * rush 
                    * https://www.datascienceatthecommandline.com/2e/chapter-7-exploring-data.html#creating-visualizations
            * xmlstarlet for xml
            * Vowpal Wabbit for modeling (vs cmdstan?)
                * using csv with Vowpal Wabbit?
            * Tapkee for dimension reduction 
            * Weka, BigML, SKLL -> Vowpal Wabbit.
        * things to learn 
            * read the following chapter
                * chapter 1 
                    * data science is OSEMN
                    * Intermezzo
                    * Command line 
                    * why data sciecne at commnad line 
                    * a readl-world use case 
                    * further reading 
                * chapter 3 
                    * overview
                        * read and figure out if I need to read the chapter at all
                * chapter 4
                    * converting one-linesr into shell scripts
                    * createing commandl-line tools with python
                * chapter 5: scrubbing data
                * chapter 6: managing your data workflow
                * chapter 7: exploring data
                * chapter 8: parallel pipeline
                * chapter 9: modeling
                * chapter 10: leverage the unix commnad line elsewhere
                * conclusion
        * first vs second edition
            * ref 
                * https://github.com/jeroenjanssens/data-science-at-the-command-line/issues/101 
            * csvkit -> xsv for csv
            * xmlstarlet is used for xml
            * scrape -> pup for HTML
            * Drake -> Make
            * Rio -> littler for R programming
            * Tapkee for dimension reduction 
            * Weka, BigML, SKLL -> Vowpal Wabbit.
        * check out the following tools
            * ref
                * https://github.com/jeroenjanssens/data-science-at-the-command-line/issues/103
            * Rio
            * rio-mds
            * rio-pca
            * rio-scatter
            * arff2csv
            * body
            * cols
            * csv2arff
            * csv2vw
            * drak
            * dseq
            * dumbplot
            * explain
            * pbc
            * scrape
            * servewd
            * trim
            * unpack
            * weka
            * weka-cluster
* read about Data Science Toolbox.
    * ref
        * https://github.com/datasciencetoolbox/datasciencetoolbox 
    * what are the essential tools for data science that I can use in my workflow?


* refactor TODO-MANAGER to use vimwiki
    * ref 
        * youtube
            * Productivity Setup with Vimwiki, Taskwarrior and MDwiki: Part 1
        * article
            * create folder with vimwiki
                * https://www.google.com/search?q=create+folder+with+vimwiki&rlz=1C1CHBF_enUS941US941&oq=create+folder+with+vimwiki&aqs=chrome..69i57.5517j0j7&sourceid=chrome&ie=UTF-8
                * https://www.reddit.com/r/vim/comments/8xzpkz/you_probably_dont_need_vimwiki/
                    * You (probably) don’t need Vimwiki
                        * https://joereynoldsaudio.com/2018/07/07/you-dont-need-vimwiki.html
    * requirment 
        * does it allow for fzf "folder" search.
            * eg 'Example/something/...'
            * if it doesn't, i need to figure it out a way to keep the folder structued of the TODOMANGER 
                and implement additional function of vimwiki.
                * see "Pros"
    * Pros
        * later on when I have lots of meeing, vimwiki have options to create current date and time note with changeable title.
            * this will comes in handy when I start to develope "daily log system"
                * note that 'log' refer to system to take a snapshot of important events, in this example, 
                    it refers to meeting notes.
* productivity setup with vim 
    * ref
        * https://www.youtube.com/watch?v=A1YgbAp5YRc
            * tools
                * tasklib (python api for taskwrrior)
                    * pip3 install tasklib
* figure out how to do space repetition with vim.
    * ref
        * space-repetition algorithm
            * https://github.com/dahu/vim-sm2
    * can't find vim package for this
    * If i can't find any, create my own vim plugin?
* learn how to manage reference 
    * stackoverflow
        * workflow for managing reference
            * https://tex.stackexchange.com/questions/18848/workflow-for-managing-references 
    * citation management workflow with vim 
        * ref
            * https://www.youtube.com/results?search_query=citation.vim
            * Note and citation using vim and pandoc
                * https://www.youtube.com/watch?v=nXgqnYVAzKk 
                * note
                    * it has feature that add "header" of paper when creating notes.
                    * searchable tags system.
                        * tags also have a page that show all paper with this tags.
                * tool
                    * pdf2doi
                    * doi2bib
            * easy academic reference paper on the command line.
                * https://www.youtube.com/watch?v=ksAfmJfdub0
                    * comment 
                        * this video show how to output citation format for research paper (pdf) using command line(pdf) using command line.
                        * "I don't think I said it in the video, but you might need to install `poppler` to get the `pdfinfo` and `pdttotext` commands."
        * what is pdfinfo?
    * reference management software 
        * learn how to use Mandeley
* learn how to use paper search engine.
    * Google scholar
    * how to use arxiv
    * connected paper
        * https://www.connectedpapers.com/main/c2519b12698187baddc889dfac9b1747cf6d2cef/ColaGNN-Crosslocation-Attention-based-Graph-Neural-Networks-for-Longterm-ILI-Prediction/derivative

* compare MLops tools  
    * ref
        * https://www.youtube.com/watch?v=UbL7VUpv1Bs
        * https://medium.com/analytics-and-data/modern-machine-learning-tooling-c1e8689ad6f1
        * https://dagshub.com/blog/how-to-compare-ml-experiment-tracking-tools-to-fit-your-data-science-workflow/

* see his article/tricks and figure out what I can use
    * ref
        * article
            * https://castel.dev/post/lecture-notes-1/
            * https://castel.dev/post/lecture-notes-2/
            * https://castel.dev/post/lecture-notes-3/
        * github 
            * https://github.com/gillescastel/latex-snippets
                * code to his snippet
    * list of snippets I should try
        * environment
            * begin-end
            * math block
            * sub- and superscript
            * fraction
        * Correcting spelling mistake
        * other plugin
            * sympy OR mathematica
            * postfix
 
