# TODO
* write about "curse of intelligence"
    * the idea is that people are not satisfied with tasks that doesn't challenge their intelligent which left the feeling of unfulfilled life. however, domain that required high intelligent required "a lot more prior knowledge about the fields" (It takes long time to discover and create creative, but it takes alot shorter time for people to "understand" or absorbs this ideas, just enough to expand on this idea.)
        * therefore, intelligent people must compete for this highly competitive space to gain all rewards, the rest of them failed and remain unfullfilled.
* here> read transfer learning 
    * here> read about technique to use in transfer learning 
* transfer learning for forcasting  

* just in case learning vs just in time leanring 
    * just in case leanring 
        * just in case = reasearch/second brain .
        * write about 3 groups of people for just in case learning.
            * content creator
                * extract + deliver + store to second brain 
            * memorizer 
                * extract + deliver + store to second brain + deliver + store to your brain
            * researcher
                * no easy way to extract, 
                * emac 
                    * most people in research use emac to optimize task to be specific to their workflow
                        and specific to their topic research.
                    * emac in do not talk to outside world really well.
                    * high learning curve
                    * niche target 
                * problem
                    * symbolic heavy which pdf or text base can't deal well with it.
                        * common problem as you see there are lots of markdown and latex styles.
    * just in time learning 
        * just in time = enterprineur, engineer, jobs/task with time constraint.
        * https://www.youtube.com/watch?v=Kq1d2kISsNw 

* explore the following channel
    * https://www.youtube.com/watch?v=R8BE6CdEPiY
        * how can I automate notification process when I post content on my blog and upload video on
            youtube.
* write about flashcard in vim
    * just use roam. too many problem with anki + imge + wsl + markdown.

* write about latex.
    * presentation with beamer 
        * ref
            *  youtube.com/watch?v=zEjBCQhND2c
        * ~/Scratches/Examples/Libraries/Latex/Beamer/
    * citation workflow for markdown and latex
        * ref
            * https://www.youtube.com/watch?v=nO4T8JDNYG0
        * autocomplete

* write about content of the following podcast
    * "you can read 10 mins instead of watching 1 hours"
    * ref 
        * https://www.youtube.com/watch?v=zzMbi5IDiyM
* write about how to determine whether time series is stationary. 
    * ref
        * https://www.linkedin.com/pulse/how-use-machine-learning-time-series-forecasting-vegard-flovik-phd-1f/
            * Granger Causality test
                * test casulity vs correlation.
        * https://towardsdatascience.com/why-does-stationarity-matter-in-time-series-analysis-e2fb7be74454
            * transformation process toward stationary time series
                * difference transformation
                * logarithmic transformaiton
                    * note 
                        * logarithmic transformation must always be followed by difference transformation.
            * ADF test
                * null hypothesis = if failed to be rejected, it suggests the time series has a unit root,
                    meaning it is non-stationary.
        * towardsdatascience.com/how-not-to-use-machine-learning-for-time-series-forecasting-avoiding-the-pitfalls-19f9d7adf424
            * plot predict vs real.
                * to see error distribution.
                * alternatively, you can plot distribution of error directly.
            * plot cross correlation
                * to detect, autocorrelation.

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

* explain how to set up ec2 with terraform and ssh-key 
    * note
        * ssh-key is not key fully automated by terraform. I created with aws cli .
* write about my principle of learning 
    * title 'Principles\Princple of Leanring' 
    * inputs 
        * validate qualification of expert 
            * note 
                * this step is to validate quality of info from individual expert.
            * 2 types of experts
                * ref
                    * book
                        * blackswarn
                * categorized by fields
                    * fields with feedback loop
                    * fields without feedbak loop
                        * properties
                            * prediction cannot be 
            * mental checklist
                * is field of a topic 
        * validate creditbility of source
            1. proof by example
            2. proof by transfer of credit from expert 
                * this required you to validate qualifiation of expert.
            3. 
    * outputs

* wrtie about my data science pipeline 
    * status 
        * [[IN PROGRESS]]
    * title 'Workflows\Datascience\'
    * ref
        * how to manage your machine leanring workflwo with DVC, weight nad & biases, and docker?
            * https://towardsdatascience.com/how-to-manage-your-machine-learning-workflow-with-dvc-weights-biases-and-docker-5529ea4e59e0
    * what are its components?
        * logging

* here> finish writing blog about Data science inside-terminal tools
    * add sections about the following
        * tools for graph 
            * graph modeling
                * AWS Neptune
    * here> give example of script to build each plot
        * here> feedgnuplot 
            * here> see ~/Documents/Working/COVID19Prediction/scratch.sh
                * what is the assume data format of feedgnuplot?
                * explain how to use gnuplot scripts.
                * note
                    * it can do what gnuplot can do, but it should be used for 
                        "premade" template plot  including the following
                        * line + dot plot
                        * Utilities/send plot to stdout
                        * Utilities/select column for x-axis with --domain
                        * Utilities/styling 
                        * plot with error bar.
                        * 3D plot
                        * plot stream data and + datetime format
                        * bar plot
                        * histogram
        * R 
            * note 
                * explain simply how to use `rush qplot` and `rush run ggplot2`
                * it simply use ggplot2 including
                    * histogram
                    * density plot 
                    * bar charts
        <!-- * termgraph -->
        <!--     * I think feedgnuplot can do what termgraph do, except heatmap. -->
        <!--         * how hard to do heatmap with R? -->
        <!--     * do i even needs this? --> 
        <!--         * does it support pipeline. -->
        <!--     * what is its assume data? --> 
        <!--     * note -->
        <!--         * use for simple plot including -->
        <!--             * heatmap --> 
