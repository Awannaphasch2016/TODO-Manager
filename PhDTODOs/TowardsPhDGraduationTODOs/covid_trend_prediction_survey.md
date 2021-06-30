 #+TITLE:  covid_trend_prediction_survey

#NOTE
* something
- streaming 
  - Finish a survey paper in 2 weeks: day 20/14

- survey format
  - Zhabiz
    - introduction
    - advertising eco-system & user response
    - Features for User response prediction
    - user response prediction framework
    - Conclusion
  - Forecasting Models for Coronavirus Disease (COVID-19): A Survey of the State-of-the-Art
    - introduction
    - Forcasting Techniques
    - Big Data
    - Social Media Data/Other Communication media Data
    - Stochastic Theory/methametical Models
    - Data Science/Machine Leanring Techniques
    - Challenges of Forcasting models
    - Recommendation
    - Conclusion

- comment from dr zhu
  - here> message 1
    - [[re-writte]] collect all papers using demographics, geographics information.
      - For today (03/03), can you collect a set of papers (e.g., 10 papers) which consider using demographics, geographics information for prediction? You can include these papers in your overleaf project.
          Also have a summary in the write-up.
      - You need to build basis to understand what are the available methods
  - message 2
    - note
      - put these 'info' into 'Dataset' section
    - [[re-written]] multi-variate data, single variate data. Model on each state (no info of other state), Model train on all states (include model of all states).
      - You need to have a clear thought about what are information available to make the prediction.
       One source of information is to use the infection number only (single variant). This is similar to what you are doing now. The training is based on a single time series (a state’s infection), and the learning may use other states (but all states are considered independent).
       Other approaches may use multivariant data, such as social medica data, demographic and geographic data etc. This becomes a multi-variant prediction problem. Again, the states may be considered independent.
       Other approach may consider sites/states are dependent variants. So they are forming a graph or a network. This will be solutions relying on graph neural network etc.
       Further, approaches, may consider states to be related and also to have demographic/content information etc.
      - Having a clear throught will help you organize your survey
  - message 3
    - You also need to report results in a more scientific way.
    Adding training day range (e.g., using five days to train, and predict future days. Then expand the window to using 10 days to train and predict future days). In this way, you can understand how does trend impact on the results.
    Adding a longer future days to predict. Short prediction (next day, next 5, or 7days are fairly straightforward. You can expand to next week, next 2 week, 3, week, 4 week prediction).
    Please oraganize the results in a summarized form. Currently, I had to use average to the excel file to compare them.
    - It would be good, if you can put all such data together.


- collecting paper to fill in Graph Modeling section 
    - paper discovery 
        - from paper that use Graph Neural Network (or graph construction), see their next research. (
            - list of paper 
        - keywords
            - transfer learning + GNN 
            - dynamic graph 
        - what is the state of the art of the folloing task
            - ILI prediction?
            - spatio temporal forcasting
            - pandemic prediction
            - viral content prediction

#RESOURCES

#REFERENCE

- more paper to read 
    - goal 
        - gather more information about epidemic network simulation
    - paper 
        - simulation 
            - Epidemic Random Network Simulations in a Distributed Computing Environment
            - Using a real-world network to model localized COVID-19 control strategies
            - A High Resolution Realistic Social Contact
            Network Construction 
    - book 
        - https://oxford.universitypressscholarship.com/view/10.1093/0199269017.001.0001/acprof-9780199269013
    - survey 
        - Analysis and Control of Epidemics: A Survey of Spreading Processes on Complex Networks 
            - file:///C:/Users/terng/Downloads/jp07%20(1).pdf
    - search
        - epidemic newtork simulation survey
            - https://www.google.com/search?q=epidemic+network+simulation+survey&rlz=1C1CHBF_enUS941US941&oq=epidemic+network+simulation+survey+&aqs=chrome..69i57j33i160l2.5371j0j4&sourceid=chrome&ie=UTF-8

#WAITING

- here> how to organize latex
    - ref
        - https://tex.stackexchange.com/questions/21904/input-and-absolute-paths
        - how to work with large projects
            - https://tex.stackexchange.com/questions/64199/how-to-work-with-large-projects
        - hwo to organize large documents in small nested folders
            - https://tex.stackexchange.com/questions/227650/how-to-organize-large-documents-in-small-nested-folders
    - error
    - here> how does command works in latex?
        - how to use include
        - here> try to use \newcommand in overleaf 
            - Are output behavior the same?

#OPTIMIZATION


- here> practice hotkeys for vim-tex 
    - requirements
        - (do not overly custermised, use things that can alwasy be used forever)
- read LatexCheatSheet
    - Goal
        - understand basic Latex 

- epidemic + graph + modeling  survey 
    - here> create and send picture (to be added) to dr zhu. 
        - add "types of contact sequence edges labeling" 
            - explains "contact sequence" 
                - why are there two types of edge representation .
            - create picture of "continouse" (no intra-layer edges) and "discrete" (no inter-layer edges) temporal network.
                - ever expanding graph
        - create a picture showing how snapshot of dynamic graph can be taken.
    - after I finish list of things that I send to dr zhu, read the following and fill out content accrodingly
        - dynamic network analysis
            - http://www.casos.cs.cmu.edu/projects/book/DNA-Book_Draft.pdf 
        - The dynamic nature of contact networks in
        infectious disease epidemiology
            - https://www.tandfonline.com/doi/pdf/10.1080/17513758.2010.503376

* other things to model
    * immunity 
        * herd immunity
            * does graph protection care about herd immunity?
        * here> how to models cross immunity?
            * ref 
                * https://www.sciencedirect.com/science/article/pii/S1755436514000176
#TODO

* create website for the group.
* manage file in discord.
    * create google drive.

* add definition of temporal network in temporal network section.
    * I somehow forget to define temporal network.
* [2021-06-25 15:32:17]
    * here> work on related work section.
        * note
            * I may consider making paragraph instead of full subsection
        * here> lets read graph embeding.
            * here> read the following sections
                * here> Is there a concept from dynamic graph embedding paper that I can generalized in my paper
                    * here> look for node/edge ranking related tasks
                        * can graph reconstruction be useful in graph protection?
                            * how is the ranking mechanism actually works?
                            * include graph embedding that are for graph protections
                    * the paper doesn't mention reachability graph, line graph, and tranmission graph
                    * It doesn't cover embedding that could apply to tmeporal network construction and multilayer network construction 
                * research on node ranking in general
                    *  a surveys on network node ranking algorithms
                        * https://link.springer.com/article/10.1007/s11431-020-1683-2
                    * embedding on node ranking
                        * https://arxiv.org/abs/1902.03964
        * combine related work section with micro/mezzo/macro network modelling.
        * Survey on Temporal Network
            * here> what are types of temporal network?
            * when is this paper published?
            * what is it oobjective?
            * why is it necessayr to have publish this paper?

        * take a look at the following paper 
            *  ref
                * google search
                    * https://www.google.com/search?q=heterogenous+networks+survey+%5D&rlz=1C1CHBF_enUS941US941&oq=heterogenous+networks+survey+%5D&aqs=chrome..69i57j0i22i30j0i8i13i30.19562j0j7&sourceid=chrome&ie=UTF-8
                        * found the following paper 
                            * A Survey of Heterogeneous Information Network Analysis - arXiv

        * Survey on Analysis, Prediction, and Control of Epidemic
            * I need to read these paper first.
        * Survey on Network Embedding
        * Survey on Related Applications

    * ways to put pictures
        * show concept of somthign in detilas
            * use picture when its hard to explains in text.
        * show details comparisons of multiple models 
            * be clear of what you want to compare.
                * avoid showing adhoc.
    * fix 
        * fig 2 
            * try draw example with draw.io.
        * idealized network
            * add scale free networks.
        * 6.3.2
            * avoid append paper one by one.
    * tools
        * try using viso professional. (is it good enough?)
    * tips
        * list question for each sections, and let it guide the writing.


* try to make introduction fill 1 page.
* focus on introduction and related work.
* lets focus on generate figure first. 
    * learn to use new visualized 

* here> Goal: by 6/25/2021, I want to finish introduction and network construction. +
    include all relevant paper into related works section
    - Analysis, Prediction, and Control of Epidemics: A
    Survey from Scalar to Dynamic Network Models
        - here> https://arxiv.org/pdf/2103.00181.pdf
            * here> 1.2 read extension and limitation
    * here> fill out tables (as I go) the following tables.
        * refactors network types, fill up mezzo
            networks (multilayer), and fix macro network.

        * simulation 
            * types of agent base network? () 
                * here> EPISIM from eubank2004modelling
            * here> mezzo simulation network table.
                * here> read the following section.
                    * here> simulation section
                        * expands content of halloran2002containing
                        * finish reading and fill out the tables.
                    * multilayer section
                    * temporal section

        * categorized multilayer network and temporal network into tables.
    * about pictures.
        * add more picture.
        * here> check if any picture needs to be redraw.
        * check label of pictures.
    * rewrite equations to not exceed its boundary
    * node and edges construction stuff
        * add textbf comment to node and edges construction.
            * here> add more content to it
    * refactor related work page.
    - add section about social-connection (social network and collaboration network)
        * note
            - all real network + social-connection can be put in edges of micro network because micro network ignore node features.
        * lets read survey papers on this.
    * mention about Theoritical Guided Data Science (TGDS) in introduction.
        * TGDS -> use information that we learn from epidemic to choose types of tranmission dynamic + types of network + deep learning architecture design.
    - summary wang and deng.
        - here> finish the following sections.
            - here> network construction
                - node construction
                    - here> micro network 
                        - here> summarized it from micro network section
                    - mezzo network 
                - here> edges construction 
                    - here> micro network
                        - here> summarized it from micro network section
                            - collect paper.
                            - here> rewrite the existing paragraph to focus on edges.
                                - check if the followin paper explain dataset that they use 
                                    - read "Sexually Transmitted Diseases and Sexual Behavior: Insights from Mathematical
                                    Models"
                    - check if mezzo network needs to be refactors.
            - macro network/Predict Infected Cases and infected distribution
        - include infecting network, tracing network, and daily base network image.
    - add double graph network that author use to disprove previous assumption about epidemic spread  from meirom2020stop
    * read graph embedding survey :)
    * create new tabes 
        * how should I classify micro/mezzo/macro nodes and edges into tables?
        * how should I classify graph embedding into tables? 
    * lets draw table properly


* goal: finish modeling 
    - summarize macro_network section (merge it with the old content)
    * explore VAE, encoder-decoder architecture on graph 
    * add the following to main content
        - read the following 
            - here> paper
                - here> seed_reading(DEFSI paper)
                    - goal
                        - complete guideline of simulation sections.
                            - what are methods 
                    - review networks and epidemic models 
                        - did they cover EPIFAST or alike in their simulation
                        - network-based simulation are limited 
                    - read about EPIFAST
                        - goal 
                            - to understand how model-based network simulated works.
                            - to collect content and add them to ~/network construction/simulation/micro network
                        - here> read section 2 
                        - read section 3
                    - a paper that use climate information
                        - goal 
                            - to learn how climate information can be used in Simulation.
    - refactors note from macro GNN. 
        - remove feature learning section.
        - here> create new section section called "constructing network from node or edges embedding" in Network/Node/Edges construction.
            - 
    - read and rewrite the following section 
        - here> Predict Infected Cases and infected distribution
            - add content to mezzo/Balancing trade off caused by epidemic/DECURLA.
                - reading
                    - here> read RL section and Flow GNN
                - writing 
                    - mention about rl-rward requirements.
            - add comment to mezzo section in location where I want to add more content
            - merge old contents of macro model + deep learning.
            - here> fix introduction, add content to related work and conclustion 
                - here> continoing fixing introduction
            - check if i mentioned multilayer graph construction in the survye
            - the paper talk about "testing" what are those?
    - create tables for micro, mezzo, macro network using words
        - note
            - here> "A framework for identifying regional outbreak and spread of COVID-19 from one-minute population-wide surveys"
        - table 1  
            - notes
                - cells in last columns are list of papers.
            - columns
                - graph type 
            - rows
                - objectives 
        - table 2 
            - columns  
                - dataset 
                    - large vs small 
                    - graph types 
                        - large vs small
                        - theoritical vs practical entwork 
                        - simutation vs real 
                            - simultated real vs simulated theoritical
                            - real data of small cohort vs real data representing the whole population. 
                        - multiplex network (a type of multilayer network) vs single layer network
                        - homogeneous nodes vs heterogeneous nodes 
                        - homogeneous edges vs heterogeneous edges 
            - rows
                - objectives?
    - add information of the following paper
        - 'scalable vaccine distribution in large graphs given uncertain data'
        - how to stop epidemic

* content to improve precision of details.
    * read more on data preprocessing on graph.
        * how do they due with noise, uncertainty etc.
            * smoothing data
            * calibration for forecasting
            * remove some data to control for noise
    * check out dataset.tex. if enough dataset can be used. then no more reading on data
        - get list of dataset from here 
            - Epidemic spreading over social networks using large-scale
            biosensors: a Survey 
                - https://pdf.sciencedirectassets.com/282073/1-s2.0-S2212017312X00069/1-s2.0-S2212017312005336/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEPn%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQDjm3SvjmGPfPWAU2RgEsxXq9XAycBBHCw8ej3DmmbQYgIgGdp85ik0xTrGywrM1UARM5AnDjIrlUTLc5FwhnEiHZQqgwQIwv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAEGgwwNTkwMDM1NDY4NjUiDHJtJKftu8Q3kyuvoSrXAwSsXl62CvuFCy9p1Dde6nH9rQ4cpbvsVK6oL7lVU2kTM50FtThEiRn4UqrrzojSkOXDUi2C9%2FP5CuuyvVtPVx8vyrYIsEkesjvnnkPIad1JzjRBYydjPTwZGwhPhMvuQPy%2BWICL6unf%2FegR%2FUgg2uOXaArPVFVjjWIoZ6LU%2FGZvLr53So2iXhaoC7QfZNIeRjYQo0WwiTPnS3izehn2V%2Bap5VEVxqJTQOGnRjbbJLeVTsMYwV5YB7UGGz2aIz23qn8IFfkXFzDwhyYnehjySHvgvRa99iy4TsMmYGH%2B8aOU%2F9lwC4ja6ekXNwlQTORjEQh7R6gWOT2TbNhGrQozYsxzKzmBVc3XIdP5pyYGwueC1zl8KO4JPeXv5Isn56RZszKC2WuiTWStu3HJtrWslbE8KaN%2BXy%2F26Eq628rLiAmhtO5nr55d0Rm5gCFtc4eAhRqP53aDpZhM3QCfCjAyiTZ2%2BYRqs7A6yezfPfaRXSbpYRVEXcDPvx0iaLtNcVmhU6szJpwvTevnywWxengkoTmifh9x7RfKGGv8%2F3ahzXDO39yRp66VEuCpdKlcX%2B1Ya%2BRUIy6zYpx1K9Wfu1VRGfL0unYrcmRZ22PfrvandgI3kZYf%2BSBIajDE%2BsKGBjqlAXAObEsRlOW5taQqz0%2B68koHbEPU%2F%2B2bYEUqKAktRvgfE%2B%2F0zq183HRlR32nUta7bY%2FfsXrtTlrn2FK50HoNnIaawG5RDAFMmriAjZn1A%2FZ9otfkLVuWnrdQxcxuGhNLl86rmqxNTBfYefnQqcTAeOrMwNG7U8xP%2FuaBy9jteiR%2BluLkkeep37GYGmMHH4It6YiWx6sEL569mvL6QAu5crJFu84WEQ%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20210621T173009Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYVEL5WSOH%2F20210621%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=fdb7f14f05ca090b0dc7f80e99a61b93838590ecbebe34e7143992527be90743&hash=de23b99a718824ce1dca8ffaf9506706d48a4e1bd1b2536f104a0e62bd3ac216&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S2212017312005336&tid=spdf-834bff9c-2f0b-4e05-8148-2f689cb36c64&sid=ce7a034c4ac1c94bdf2a5d20e299d262ae01gxrqa&type=client

- read the following 
    - 'Systematic comparison between methods for the detection of influential spreaders in complex
    networks'
    - https://dl.acm.org/doi/pdf/10.1145/2588555.2593668
        - construction of uncertain graph
            - figure out if I  can add these contents in my surveys.

- finish old writing.
    - picture of graph protection
    - picture of epidmeic threshold?
        - https://roamresearch.com/#/app/AdaptiveGraphStucture/page/lWzz1KSL7
    - where did i left off
        - finish merging?
        - add types of network
        - put content from paper to the survey
            - mezzo network 
                - here> Reinforced Epidemic Control: Saving Both Lives and Economy
                    - here> finish making notes in [[Architecture]], [[Challenges]], Experiment, Data, and Evaluation sections 
                        - then summarized content.
            - macro network 
            - micro network 
                - Scalable vaccine distribution in large graphs given uncertain data
                - TDEFSI: theory-guided deep learning-based epidemic forecasting with synthetic
                    information
        - mini netowrk  
            - graphDelta: MPNN scoring function for the affinity prediction of protein--ligand complexes
        - create tables categorized by data construction, methods, objectives. 

- read the following 
    - A study on graph-structured recurrent neural networks and sparsification with application to
        epidemic forecasting.
    - early detection
        - loclaized epidemic detection in networks with overwhileming noise.
    - spread control
        -  Optimizing influenza vaccine distribution
            - note
                - don't read if it doens't use graph.
    - generalize design on dynamic graph
        - Towards explainable representation of time-evolving graphs via spatialtemporal graph
            attention networks.
        - Temporal
            graph networks for deep learning on dynamic graphs
        -  Towards fine-grained temporal network representation via time-reinforced random walk
        - EvolveGCN: Evolving Graph Convolutional Networks for
        Dynamic Graphs.
    - survey
        - Representation Learning for Dynamic Graphs.
            - note
                - doesn't focus on epidemic dynamic graph.
                    - only 1 matching words were found.
            - https://arxiv.org/pdf/1905.11485.pdf
        - firefighter survey
            - The Firefighter Problem: A survey of results, directions and
            questions
                - identify bottleneck
                    - Targeted Pandemic
                    Containment Through Identifying Local Contact Network Bottlenecks.
                - allocating resource
                    - Optimal Containment of Epidemics in Temporal and Adaptive
                    Networks


- [2021-05-21 15:38:58]
    - mini network
        - summarized interaction of dataset network.
            - types?
            - mechanism?
            - how they interacts.?
    - here> network construction
        - table should provide some answer.
            - what would you want reader to know?
            - what information would be helpful for users?
    - linear programming
        - what are constraints?
            - intuitive explaination of each constraint.s
    - related work
        - what are other survey?
        - why this survey is needed?
            - what content do other surveys not have?
    - pictures
        - example 
            - hand drawing is allowed.
        - picture that cover bigget topics
    - dr zhu review
        - pictures
        - better survey sturcutre


- read the following about mini network
    - here> https://levelup.gitconnected.com/graph-neural-networks-for-binding-affinity-prediction-6e7d9ab9c58b

- [2021-05-14 15:39:55]
    - here> introduction
        - requirment
            - motivatiton
            - here> application
                - micro
                - here> mezzo
                - macro
        - section a
            - reference more types of methods.
                - ref 
                    -
                    https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIRD_model
                    - https://link.springer.com/content/pdf/10.1007%2F978-3-540-78911-6_2.pdf
                    -
                    https://pdf.sciencedirectassets.com/271979/1-s2.0-S0025556410X00050/1-s2.0-S0025556410000143/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEMf%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQDELjujTY8I9ie8UR4EuSuG9Y6i7KwiV8UMzO3ouwpgJgIgDeTzr6E%2BvSLAaEKTI7uuzbt%2FEQkxAq6SEA4WzQdIGP0qtAMIYBADGgwwNTkwMDM1NDY4NjUiDFBeLCOPky%2FOVZ7eEiqRAw3SQ3pwqO%2BaI4GoI6OxH8AFXbZdHlE9rZTKj%2FR84wB7fkbspW%2BjeFAFU6poBEUZ%2FjhBwGlxbdkuuY36oK7ZPfqQ0eAfM9Gh5P4rlBs4LCYCw61V2q20Hcc0kctezAGymvqzR54JL31hb%2BCCY7QBjZQm1HFlCKFl7z8skREUr%2BaKQrBJrT7%2FmhJL6bYsB0dtQv76L6S8bRkn8s0vFwNkyTSvI9Xw6Xir3IqMyO6hCDUPueabZw6uawMsEYwPj1wv421VYq970%2BabT3giFY0KutPZgSEzSymDHdCgOSKAXT%2Ba2w0hUcgT%2FjBaB%2BXEulARxAARRlUUT4ALPirl3dULHIeKLLQ7H%2FaRWrFrdYs2Q3kZsi%2Bvbnbd3LpkD5WpCWA%2FMY4IkaHz%2BAlbUMmUszPoGWWsXX2of
            - read epidemic survey
            - for micro network, mentioned for research field liek SIE, AVRE, ESZR, agent based model.
                - what are command methods used to predict epidemic?
                    - ARIMA
            - task 
                - infection esimtaiton
                - visualiaiont 
                - quanratine
            - explain about approach. why are eg. SIS estimate based on individuals level. 
        - section b 
            - motiation of considering mezzo and macro instead micro
            - micro -> mezzo & macro
                - movtivated by privacy.
                - task 
                    - high level estimation.
                        - esimate cohort district
                        - resource planning
                        - number of beds.
                        - create networks (nodes - idstricts, edges ..) 
                        - risk assessment
        - section C
            - mini network.
                - ref
                    - https://link.springer.com/content/pdf/10.1007/s42600-021-00135-6.pdf
                - what are keywords for this?
                - in additon to micro, mezzo, macro network, reseach also try to achieve other goal by
                    model relationship at somatic items scales.
                    - eg.
                        - gene, disease, drugs, and virus.
                - task
                    - druge repurposeing vs drug discovery?
                    - drug screening?
                    - drug encoder
                    - feature extraction based on circular fingerprint
                - what is fingerprint?

    - here> network construction
        - create tables 
            - row example 
                - ineteraction, PPIs, [what is the interactions.]
            - create for each network.

- read the following paper
    - https://link.springer.com/content/pdf/10.1007/s42600-021-00135-6.pdf

- https://mail.google.com/mail/u/0/#inbox/QgrcJHsBpWgbDwJPGvTfWNZHzXNXsTLKCmQ 
    - "I include some comments (marked in red) in introduction. You can add some content to reflect
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
           - read protein-protein, protein-disease network etc. 


- do the following  
    - network construction in general.
        - here> what are dataset used in all the papers I mentioned?
            - here> read content that I have in mini network, micro network, and network construction, and
                get data from there.
                - here> add citattion for PPIs and drug-target from  "Network medicine framework for identifying
                    drug-repurposing opportunities for COVID-19
                    "
                    - here> read this
                        https://www.pnas.org/content/pnas/suppl/2021/04/27/2025581118.DCSupplemental/pnas.2025581118.sapp.pdf 
                        - here> put content in dataset or node construction
                            - here> take a look into datset
                                - here> read dataset comments, check what i am missing, and add those
                                content
    - here> read + write deep learning + simulation + epidemic. (micro, mezzo, and macro)
        - write 
            - here> fix network construction tables.
                - see picture.
            - mini network 
            - micro network
                - here> put content from the following papre int nodes and edges  construction 
                    - here> "Influenza spread on context-specific networks lifted from interaction-based diary data"
                        - here> make note on SIR section 
                        - put SIR content in the survey
            - mezzo network
                - here> add informaiton from papers that are in gnn.tex file 
        - here> summaried other read paper.
            - here> merge from old content
                - how should I structure it ?
                - here> feature learning model.
                    - cola
                    - here> Spectral temporal graph neural network for multivariate time-series
                        forecasting
                        - here> discussing about result.
                    - Using Mobility Data to Understand and Forecast COVID19 Dynamics
                    - Dynamic Virtual Graph Significance Networks for Predicting Influenza
                - Parameter Estimation model
                - Attention leanring model
                    - should each of these sections have machine learning section?
                - knowledge fusion
        - what is the process of drug repurposing.
        - redo/add content/adjust content of {table:a summary of mini/micro/mezzo and macro network}

- " You need to mention them, because many work in the traditional disease modeling uses such ideal
network (such as random network, where each person is assumed to have each number of
change/opportunity to contact others).
    In real-world (such as social network setting), this is not true. So, you can find that mobility
 network or other networks are created from real=world data.
    We need to highlight the movement of research from such ideal network to a real=world network"
    - here> read about traditional network.
    - what is the motivation of using traditional network?
    - when to choose real network over traditional networks?


- [done] "You need to add details about: what are the major components of pandemics (such
as pathogens, hosts, interactions etc).  How they function together, with
similar networking mechanism. This motivates researchers to consider different
pandemics models."
    - [done] Infectious Disease Epidemiology Transmission Dynamics
        -
        https://nau.edu/wp-content/uploads/sites/79/ID-Epidemiology-Bootcamp-session-1_final-Compatibility-Mode-1.pdf
    - [done] motivation that reseachre consider different pandemics models
        - here> how they fucntions togehter as a network?
            - here> how can drugs effect pathogens?
                - how does antibody works?
            - how can proteins be used by drugs and pathogens?

- put content in the following 
    - related work
        - figure out how survey papers write related work sections
        - put content to create structure to put content from read papers
    - network medicine framwork for identifiying drug-repurpsoing opportunities for COVID-19
        - here> put content from both papers
            - here> scale and objective.
                - mezzo
            - nodes and edges construction 
            - micro network modeling

    - here> Networks for Epidemics and Pandemic Study.
        - here> put content from both papers
            - scale and objective.
            - nodes and edges construction 
            - mezzo network modeling

    - Network Modleing and Anlaytics for Epidmics and Pandemics
        - put content from both paper in
            - scale and objective.
            - nodes and edges construction 
            - mezzo network modeling

- add content as I read
    - add content from "influenza spread on context- specific networks lifetd fro interaction-based
        diary data" to the survey.
        - here> put it in micro graph 
    - here> finished reading + summarized.
        - here> https://www.pnas.org/content/118/19/e2025581118/tab-article-info
            - here> put content into the following
                - related work.
                - mini network modeling.
                - node and edges construction
        - https://www.pnas.org/content/pnas/118/19/e2025581118.full.pdf 
        - https://arxiv.org/pdf/2007.00576.pdf
    - about related work 
        - most of the survey don't consider network scale.
            - network modeling
                - analyze patterns/properties within networks.
                - reveal features of networks.
                - graph theory.
                - social science.
            - network analytics
                - predictive model (this is what I have content on)
            - input network construction 
    - I need to gather information for > 1 scale before I can add content
        - here> try to summarize what I have in introduction and content to the papers

- introduction fixes
    - ref
        - summay of networks typesk, scale table
            -
            https://mail.google.com/mail/u/0/#starred/FMfcgxwLtstGHGvpxpdbcSSPZQjQnJWR?projector=1&messagePartId=0.1
    - https://mail.google.com/mail/u/0/#inbox/QgrcJHrhxnlBBDbfZPTXGVlBgkGCGJzNdcg
        - comment 
            - You need to have a clear logic when writing a survey paper. Work out an
                architecture of the Introduciton in your mind, then carry out the writing. It
                should speak out like a story with logics advancing from one paragraph to
                another paragraph.
        - here> introduction   
            - Explain that networks and interactions are the key for pandemics outbreaks.
                - It also decides the outbreak and spread speed of the pandemics.
                    - For example, explain traditional SIR model, explain that the contact networks was
                        nherentljy assumed.
            - here> what are the major components of pandemics (such as pathogens, hosts, interactions etc).
            - Explain that recent study has advanced networks to more advanced fields (in addition to
                traditional SIR, or ESIR models). Explain what networks can be done to advance pandemics
                study, such as prediction of the infections, study drug repoposing etc.
                - add more content of this to related works too.
            - Explain what are the motivation of this survey (many works have been done in this area.
                This study try to provide a comprehensive survey, caregorize different methods etc).
        - related works 
            - Review the paper about pandemics and networks (rather raditional approach reviewing
                networks for pandemics). Explain different of your paper from those existing work.
        - networks and epidemic models
            - This is the section you will propose four tier network survey architecture.
    - https://mail.google.com/mail/u/0/#inbox/QgrcJHrhxnlBBDbfZPTXGVlBgkGCGJzNdcg 
        - Instead, focus on scientific characteristics of pandemics vs. epidemics
        - I need to add details about: what are the major components of pandemics (such as
            pathogens, hosts, interactions etc).  How they function together, with similar
            networking mechanism. This motivates researchers to consider different pandemics models.
        - Explain that recent study has advanced networks to more advanced fields (in
            addition to traditional SIR, or ESIR models). Explain what networks can be done to
            advance pandemics study, such as prediction of the infections, study drug repoposing
            etc.

- add content from the follwoing paper to the survey
    - "sterring a historical disease forcasting model .."
    - here> "how to stop epidemics: controling grpah dynamics with reinforecment lenaring and graph neurla netowrk"
- read about he following 
    - google the following "deep learning epidemic simulation"
- fix points suggested by dr Zhu.
    - ref
        - emails
            - https://mail.google.com/mail/u/0/#all/FMfcgxwLtGjKrPtVcGlwxftmgsfZtRhL
        - template 
            - https://www.overleaf.com/project/605befa3007f819a13f782bd
    - fix 
        - add plot and figure.
    - here> collect papers from connected papers.
    - refactor process
        - waiting for reply and I can process to add the followiong content
            - here> read network construction and figure out what to refactors.
            - add the following content to modeling section
                - Attention mechanism 
                - spatial dependencies
                    - learning local vs global spatial 
                        - do i have any?
                - temporal dependencies 
                    - multi-scale structural information.
                        - append GNN output from each layer together.
                    - multi-scale temporal information
                        - 1D dilated CNN
                    - intra-dependencies 
                        - if not use GNN
                            - input is a covid case of the past few days
                        - if used GNN
                            - note:
                                - GNN doesn't learn intra dependencies.
                            - SPNN model
                            - feature encoding 
                                - rnn model variances.
                    - inter-dependencies
                        - if not used GNN 
                            - input is a covid case of multiple location per timestep.
                        - all GNN really with time-series features.
                -  writing about transfer learning 
        - refactor other network/edges/nodes construction.

- put the following info to PaperSummary notes then to survey 
    - problem of epidemic forecasting
        1. few data -> models must be good at learning from low number of data
                  eg. transfer learning
        2. few data (from each source) + many data sources (heterogenous data) -> data from each source must be calibrated \ 
        model must be good at learning from hetergenous data + each data sources may contains different types of noise
        3. use similation to get more data -> model must be able to learn from simulated data + simulated data must represent "real data"

- look into the following topics. 
    - transfer learning
        - what are the types of transfer learning model?
    - transformer
    - embedding 
        - time seires embeding 
        - pandemic (viral) embedding
    - heterogenous input
    - limited dataset (low volume of dataset)
    - knowledge distillation
