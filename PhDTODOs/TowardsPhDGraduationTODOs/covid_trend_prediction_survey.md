
#NOTE
* survey format
    * Zhabiz
        * introduction
        * advertising eco-system & user response
        * Features for User response prediction 
        * user response prediction framework 
        * Conclusion
    * Forecasting Models for Coronavirus Disease (COVID-19): A Survey of the State-of-the-Art
        * introduction 
        * Forcasting Techniques
        * Big Data 
        * Social Media Data/Other Communication media Data
        * Stochastic Theory/methametical Models
        * Data Science/Machine Leanring Techniques
        * Challenges of Forcasting models
        * Recommendation
        * Conclusion

* comment from dr zhu
    * here> message 1 
        * [[re-writte]] collect all papers using demographics, geographics information.
            * For today (03/03), can you collect a set of papers (e.g., 10 papers) which consider using demographics, geographics information for prediction? You can include these papers in your overleaf project.
                Also have a summary in the write-up. 
            * You need to build basis to understand what are the available methods
    * message 2 
        * note 
            * put these 'info' into 'Dataset' section
        * [[re-written]] multi-variate data, single variate data. Model on each state (no info of other state), Model train on all states (include model of all states).
            * You need to have a clear thought about what are information available to make the prediction.
             One source of information is to use the infection number only (single variant). This is similar to what you are doing now. The training is based on a single time series (a state’s infection), and the learning may use other states (but all states are considered independent).
             Other approaches may use multivariant data, such as social medica data, demographic and geographic data etc. This becomes a multi-variant prediction problem. Again, the states may be considered independent.
             Other approach may consider sites/states are dependent variants. So they are forming a graph or a network. This will be solutions relying on graph neural network etc.
             Further, approaches, may consider states to be related and also to have demographic/content information etc.
            * Having a clear throught will help you organize your survey
    * message 3
        * You also need to report results in a more scientific way.
        Adding training day range (e.g., using five days to train, and predict future days. Then expand the window to using 10 days to train and predict future days). In this way, you can understand how does trend impact on the results.
        Adding a longer future days to predict. Short prediction (next day, next 5, or 7days are fairly straightforward. You can expand to next week, next 2 week, 3, week, 4 week prediction).
        Please oraganize the results in a summarized form. Currently, I had to use average to the excel file to compare them.
        * It would be good, if you can put all such data together.


* collecting paper to fill in Graph Modeling section 
    * paper discovery 
        * from paper that use Graph Neural Network (or graph construction), see their next research. (
            * list of paper 
        * keywords
            * transfer learning + GNN 
            * dynamic graph 
        * what is the state of the art of the folloing task
            * ILI prediction?
            * spatio temporal forcasting
            * pandemic prediction
            * viral content prediction
#RESOURCES

#QUESTION

#WAITING

* here> how to organize latex
    * ref
        * https://tex.stackexchange.com/questions/21904/input-and-absolute-paths
        * how to work with large projects
            * https://tex.stackexchange.com/questions/64199/how-to-work-with-large-projects
        * hwo to organize large documents in small nested folders
            * https://tex.stackexchange.com/questions/227650/how-to-organize-large-documents-in-small-nested-folders
    * error
    * here> how does command works in latex?
        * how to use include
        * here> try to use \newcommand in overleaf 
            * Are output behavior the same?

#OPTIMIZATION

* here> practice hotkeys for vim-tex 
    * requirements
        * (do not overly custermised, use things that can alwasy be used forever)
* read LatexCheatSheet
    * Goal
        * understand basic Latex 

#TODO

* here> finished "edges" section -> finished "nodes" section -> finished 'table'
    * here> finish summarizing "Cola-Gnn" first
        * vim line limit?
        * figure out latex link length limit 
            * here> requirement
                * (add line break automatically so 1 line in latex = 1 line in vim).
                * (fit into a half a screen)
        * figure out markdown line length as well (same requirement as latex line length limit)
            * requirement
                * (add line break automatically so 1 line in latex = 1 line in vim).
                * (fit into a half a screen)

* here> refactor papers
    * use table to summarized.
        * 3 pages per meeting.
        * collect the following for all papers
            * note
                * finished old papers first then move on to unread one. (do a quick scan rather than throughout reading)
            * here> for graph construction.
                * how to create nodes in graph  
                * how to create edges in graph

* put the following info to PaperSummary notes then to survey 
    * problem of epidemic forecasting
        1. few data -> models must be good at learning from low number of data
                  eg. transfer learning
        2. few data (from each source) + many data sources (heterogenous data) -> data from each source must be calibrated \ 
        model must be good at learning from hetergenous data + each data sources may contains different types of noise
        3. use similation to get more data -> model must be able to learn from simulated data + simulated data must represent "real data"
-- 3/17/2021

* look into the following topics. 
    * transfer learning
        * what are the types of transfer learning model?
    * transformer
    * embedding 
        * time seires embeding 
        * pandemic (viral) embedding
    * heterogenous input
    * limited dataset (low volume of dataset)
    * knowledge distillation
