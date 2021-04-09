# TODO
* figure out how to embed gist inside of markdown
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
