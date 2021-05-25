
#NOTE
* streaming 
    * Finish a survey paper in 2 weeks: day 10/14

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

* here> finish old writing.
    * where did i left off
        * simualtion 
        * put content from paper to the survey
            * here> list all the paper here


* [2021-05-21 15:38:58]
    * mini network
        * summarized interaction of dataset network.
            * types?
            * mechanism?
            * how they interacts.?
    * here> network construction
        * table should provide some answer.
            * what would you want reader to know?
            * what information would be helpful for users?
    * linear programming
        * what are constraints?
            * intuitive explaination of each constraint.s
    * related work
        * what are other survey?
        * why this survey is needed?
            * what content do other surveys not have?
    * pictures
        * example 
            * hand drawing is allowed.
        * picture that cover bigget topics
    * dr zhu review
        * pictures
        * better survey sturcutre


* read the following about mini network
    * here> https://levelup.gitconnected.com/graph-neural-networks-for-binding-affinity-prediction-6e7d9ab9c58b

* [2021-05-14 15:39:55]
    * here> introduction
        * requirment
            * motivatiton
            * here> application
                * micro
                * here> mezzo
                * macro
        * section a
            * reference more types of methods.
                * ref 
                    *
                    https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIRD_model
                    * https://link.springer.com/content/pdf/10.1007%2F978-3-540-78911-6_2.pdf
                    *
                    https://pdf.sciencedirectassets.com/271979/1-s2.0-S0025556410X00050/1-s2.0-S0025556410000143/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEMf%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQDELjujTY8I9ie8UR4EuSuG9Y6i7KwiV8UMzO3ouwpgJgIgDeTzr6E%2BvSLAaEKTI7uuzbt%2FEQkxAq6SEA4WzQdIGP0qtAMIYBADGgwwNTkwMDM1NDY4NjUiDFBeLCOPky%2FOVZ7eEiqRAw3SQ3pwqO%2BaI4GoI6OxH8AFXbZdHlE9rZTKj%2FR84wB7fkbspW%2BjeFAFU6poBEUZ%2FjhBwGlxbdkuuY36oK7ZPfqQ0eAfM9Gh5P4rlBs4LCYCw61V2q20Hcc0kctezAGymvqzR54JL31hb%2BCCY7QBjZQm1HFlCKFl7z8skREUr%2BaKQrBJrT7%2FmhJL6bYsB0dtQv76L6S8bRkn8s0vFwNkyTSvI9Xw6Xir3IqMyO6hCDUPueabZw6uawMsEYwPj1wv421VYq970%2BabT3giFY0KutPZgSEzSymDHdCgOSKAXT%2Ba2w0hUcgT%2FjBaB%2BXEulARxAARRlUUT4ALPirl3dULHIeKLLQ7H%2FaRWrFrdYs2Q3kZsi%2Bvbnbd3LpkD5WpCWA%2FMY4IkaHz%2BAlbUMmUszPoGWWsXX2of
            * read epidemic survey
            * for micro network, mentioned for research field liek SIE, AVRE, ESZR, agent based model.
                * what are command methods used to predict epidemic?
                    * ARIMA
            * task 
                * infection esimtaiton
                * visualiaiont 
                * quanratine
            * explain about approach. why are eg. SIS estimate based on individuals level. 
        * section b 
            * motiation of considering mezzo and macro instead micro
            * micro -> mezzo & macro
                * movtivated by privacy.
                * task 
                    * high level estimation.
                        * esimate cohort district
                        * resource planning
                        * number of beds.
                        * create networks (nodes - idstricts, edges ..) 
                        * risk assessment
        * section C
            * mini network.
                * ref
                    * https://link.springer.com/content/pdf/10.1007/s42600-021-00135-6.pdf
                * what are keywords for this?
                * in additon to micro, mezzo, macro network, reseach also try to achieve other goal by
                    model relationship at somatic items scales.
                    * eg.
                        * gene, disease, drugs, and virus.
                * task
                    * druge repurposeing vs drug discovery?
                    * drug screening?
                    * drug encoder
                    * feature extraction based on circular fingerprint
                * what is fingerprint?

    * here> network construction
        * create tables 
            * row example 
                * ineteraction, PPIs, [what is the interactions.]
            * create for each network.

* read the following paper
    * https://link.springer.com/content/pdf/10.1007/s42600-021-00135-6.pdf

* https://mail.google.com/mail/u/0/#inbox/QgrcJHsBpWgbDwJPGvTfWNZHzXNXsTLKCmQ 
    * "I include some comments (marked in red) in introduction. You can add some content to reflect
    recent work on modeling muzzo and macro networks. This part should be mainly related to the
    recent efforts.

     For the section 3.1 (scale and objectives), please add more work related to the Mini networks.
     There are many work in this catgory (such as protein-protein, protein-disease network etc.
     There are also works related to drug reposising etc.).

      For the node contruction and edge construction, you may also consider separating content with
      respect to the four tier networks (e.g., mini, micro, muzzao, and macro). For example, what
      are edge relationships for mini networks (they are typical interactions between diseasese,
      genes, proteins. The interactions can also be quantified as different context, such as
      citation relationship, e.g., a paper mentioned a disease and a gene, or other relationships).

       When you are writing the first draft, try your very best to add reference."
           * read protein-protein, protein-disease network etc. 


* do the following  
    * network construction in general.
        * here> what are dataset used in all the papers I mentioned?
            * here> read content that I have in mini network, micro network, and network construction, and
                get data from there.
                * here> add citattion for PPIs and drug-target from  "Network medicine framework for identifying
                    drug-repurposing opportunities for COVID-19
                    "
                    * here> read this
                        https://www.pnas.org/content/pnas/suppl/2021/04/27/2025581118.DCSupplemental/pnas.2025581118.sapp.pdf 
                        * here> put content in dataset or node construction
                            * here> take a look into datset
                                * here> read dataset comments, check what i am missing, and add those
                                content
    * here> read + write deep learning + simulation + epidemic. (micro, mezzo, and macro)
        * write 
            * here> fix network construction tables.
                * see picture.
            * mini network 
            * micro network
                * here> put content from the following papre int nodes and edges  construction 
                    * here> "Influenza spread on context-specific networks lifted from interaction-based diary data"
                        * here> make note on SIR section 
                        * put SIR content in the survey
            * mezzo network
                * here> add informaiton from papers that are in gnn.tex file 
        * here> summaried other read paper.
            * here> merge from old content
                * how should I structure it ?
                * here> feature learning model.
                    * cola
                    * here> Spectral temporal graph neural network for multivariate time-series
                        forecasting
                        * here> discussing about result.
                    * Using Mobility Data to Understand and Forecast COVID19 Dynamics
                    * Dynamic Virtual Graph Significance Networks for Predicting Influenza
                * Parameter Estimation model
                * Attention leanring model
                    * should each of these sections have machine learning section?
                * knowledge fusion
        * what is the process of drug repurposing.
        * redo/add content/adjust content of {table:a summary of mini/micro/mezzo and macro network}

* " You need to mention them, because many work in the traditional disease modeling uses such ideal
network (such as random network, where each person is assumed to have each number of
change/opportunity to contact others).
    In real-world (such as social network setting), this is not true. So, you can find that mobility
 network or other networks are created from real=world data.
    We need to highlight the movement of research from such ideal network to a real=world network"
    * here> read about traditional network.
    * what is the motivation of using traditional network?
    * when to choose real network over traditional networks?


* [done] "You need to add details about: what are the major components of pandemics (such
as pathogens, hosts, interactions etc).  How they function together, with
similar networking mechanism. This motivates researchers to consider different
pandemics models."
    * [done] Infectious Disease Epidemiology Transmission Dynamics
        *
        https://nau.edu/wp-content/uploads/sites/79/ID-Epidemiology-Bootcamp-session-1_final-Compatibility-Mode-1.pdf
    * [done] motivation that reseachre consider different pandemics models
        * here> how they fucntions togehter as a network?
            * here> how can drugs effect pathogens?
                * how does antibody works?
            * how can proteins be used by drugs and pathogens?

* put content in the following 
    * related work
        * figure out how survey papers write related work sections
        * put content to create structure to put content from read papers
    * network medicine framwork for identifiying drug-repurpsoing opportunities for COVID-19
        * here> put content from both papers
            * here> scale and objective.
                * mezzo
            * nodes and edges construction 
            * micro network modeling

    * here> Networks for Epidemics and Pandemic Study.
        * here> put content from both papers
            * scale and objective.
            * nodes and edges construction 
            * mezzo network modeling

    * Network Modleing and Anlaytics for Epidmics and Pandemics
        * put content from both paper in
            * scale and objective.
            * nodes and edges construction 
            * mezzo network modeling

* add content as I read
    * add content from "influenza spread on context- specific networks lifetd fro interaction-based
        diary data" to the survey.
        * here> put it in micro graph 
    * here> finished reading + summarized.
        * here> https://www.pnas.org/content/118/19/e2025581118/tab-article-info
            * here> put content into the following
                * related work.
                * mini network modeling.
                * node and edges construction
        * https://www.pnas.org/content/pnas/118/19/e2025581118.full.pdf 
        * https://arxiv.org/pdf/2007.00576.pdf
    * about related work 
        * most of the survey don't consider network scale.
            * network modeling
                * analyze patterns/properties within networks.
                * reveal features of networks.
                * graph theory.
                * social science.
            * network analytics
                * predictive model (this is what I have content on)
            * input network construction 
    * I need to gather information for > 1 scale before I can add content
        * here> try to summarize what I have in introduction and content to the papers

* introduction fixes
    * ref
        * summay of networks typesk, scale table
            *
            https://mail.google.com/mail/u/0/#starred/FMfcgxwLtstGHGvpxpdbcSSPZQjQnJWR?projector=1&messagePartId=0.1
    * https://mail.google.com/mail/u/0/#inbox/QgrcJHrhxnlBBDbfZPTXGVlBgkGCGJzNdcg
        * comment 
            * You need to have a clear logic when writing a survey paper. Work out an
                architecture of the Introduciton in your mind, then carry out the writing. It
                should speak out like a story with logics advancing from one paragraph to
                another paragraph.
        * here> introduction   
            * Explain that networks and interactions are the key for pandemics outbreaks.
                * It also decides the outbreak and spread speed of the pandemics.
                    * For example, explain traditional SIR model, explain that the contact networks was
                        nherentljy assumed.
            * here> what are the major components of pandemics (such as pathogens, hosts, interactions etc).
            * Explain that recent study has advanced networks to more advanced fields (in addition to
                traditional SIR, or ESIR models). Explain what networks can be done to advance pandemics
                study, such as prediction of the infections, study drug repoposing etc.
                * add more content of this to related works too.
            * Explain what are the motivation of this survey (many works have been done in this area.
                This study try to provide a comprehensive survey, caregorize different methods etc).
        * related works 
            * Review the paper about pandemics and networks (rather raditional approach reviewing
                networks for pandemics). Explain different of your paper from those existing work.
        * networks and epidemic models
            * This is the section you will propose four tier network survey architecture.
    * https://mail.google.com/mail/u/0/#inbox/QgrcJHrhxnlBBDbfZPTXGVlBgkGCGJzNdcg 
        * Instead, focus on scientific characteristics of pandemics vs. epidemics
        * I need to add details about: what are the major components of pandemics (such as
            pathogens, hosts, interactions etc).  How they function together, with similar
            networking mechanism. This motivates researchers to consider different pandemics models.
        * Explain that recent study has advanced networks to more advanced fields (in
            addition to traditional SIR, or ESIR models). Explain what networks can be done to
            advance pandemics study, such as prediction of the infections, study drug repoposing
            etc.

* add content from the follwoing paper to the survey
    * "sterring a historical disease forcasting model .."
    * here> "how to stop epidemics: controling grpah dynamics with reinforecment lenaring and graph neurla netowrk"
* read about he following 
    * google the following "deep learning epidemic simulation"
* fix points suggested by dr Zhu.
    * ref
        * emails
            * https://mail.google.com/mail/u/0/#all/FMfcgxwLtGjKrPtVcGlwxftmgsfZtRhL
        * template 
            * https://www.overleaf.com/project/605befa3007f819a13f782bd
    * fix 
        * add plot and figure.
    * here> collect papers from connected papers.
    * refactor process
        * waiting for reply and I can process to add the followiong content
            * here> read network construction and figure out what to refactors.
            * add the following content to modeling section
                * Attention mechanism 
                * spatial dependencies
                    * learning local vs global spatial 
                        * do i have any?
                * temporal dependencies 
                    * multi-scale structural information.
                        * append GNN output from each layer together.
                    * multi-scale temporal information
                        * 1D dilated CNN
                    * intra-dependencies 
                        * if not use GNN
                            * input is a covid case of the past few days
                        * if used GNN
                            * note:
                                * GNN doesn't learn intra dependencies.
                            * SPNN model
                            * feature encoding 
                                * rnn model variances.
                    * inter-dependencies
                        * if not used GNN 
                            * input is a covid case of multiple location per timestep.
                        * all GNN really with time-series features.
                *  writing about transfer learning 
        * refactor other network/edges/nodes construction.

* put the following info to PaperSummary notes then to survey 
    * problem of epidemic forecasting
        1. few data -> models must be good at learning from low number of data
                  eg. transfer learning
        2. few data (from each source) + many data sources (heterogenous data) -> data from each source must be calibrated \ 
        model must be good at learning from hetergenous data + each data sources may contains different types of noise
        3. use similation to get more data -> model must be able to learn from simulated data + simulated data must represent "real data"

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
