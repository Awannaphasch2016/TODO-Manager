# TODO

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
