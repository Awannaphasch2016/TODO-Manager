
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

* comment from dr zhu
    * message 1 
        * [[re-writte]] collect list of paper that implement models to utilize various dataset type (as specpfied on the overleaf).
            * For today (03/03), can you collect a set of papers (e.g., 10 papers) which consider using demographics, geographics information for prediction? You can include these papers in your overleaf project.
                Also have a summary in the write-up. 
            * You need to build basis to understand what are the available methods
    * message 2 
        * note 
            * put these 'info' into 'Dataset' section
        * You need to have a clear thought about what are information available to make the prediction.
         One source of information is to use the infection number only (single variant). This is similar to what you are doing now. The training is based on a single time series (a state’s infection), and the learning may use other states (but all states are considered independent).
         Other approaches may use multivariant data, such as social medica data, demographic and geographic data etc. This becomes a multi-variant prediction problem. Again, the states may be considered independent.
         Other approach may consider sites/states are dependent variants. So they are forming a graph or a network. This will be solutions relying on graph neural network etc.
         Further, approaches, may consider states to be related and also to have demographic/content information etc.
        * Having a clear throught will help you organize your survey
        
* here> put each section from my note to latex.
    * ref
        * section of Forecasting Models for Coronavirus Disease (COVID‑19): A Survey of the State‑of‑the‑Art.
            * Big data 
            * Social Media Data
            * Other Communication Media Data
            * Stochastic Theory/Methematical Models
            * Data Science/Machine Leanring Techniques
            * Discussion
            * Challenges

* lets add references 
    * here> hwo to add bib reference?
        * here> bib reference management
            * goal 
                * bib managerment that goes beyond 1 paper.
                    * bib managements that can be used with latex.
            * what is bibtex?
            * here> best way to manage bib?
                * here> how to maintain citation for your reference 
            * strategies specific to AI | CS | math | physics

* deleted my test repo of covid19 survey -> add dr zhu project to github -> clone it locally 
* how to do latext in vim
    * ref
        * https://www.youtube.com/watch?v=wzs1TpFXTkA&ab_channel=PascalBrokmeier)
        * https://www.youtube.com/watch?v=Mphdtdv2_xs&ab_channel=LukeSmith
        * https://www.youtube.com/watch?v=92QapmKKqKg&ab_channel=ChristopherFusting
    * error
        * latex from overleaf cause error on vimtex
    * here> run minimal latex sample on ubuntu
        * here> how to generate latex as pdf from vim
            * ref
                * https://tex.stackexchange.com/questions/334709/how-to-generate-pdf-files-with-vim-latex-suite
            * here> error
                * latexmk is not executable
            * how to enable compile using vimtex?
        * how to enable tex live?
            * is Tex live a compiler?
            * here> how to use it 
        * how to generate 
    * configuration
        * plugins 
            * here> lervag/vimtex
                * read help documentation
                * read about its features
                    * what is helptags?
                * default 
                    * document compilation
                        * latexmk
                    * latext log parsing for quickfix entries 
                    * compilation of selected part of document
                    * suprot for several PDF viewers with forward search
                    * completion of 
                    * decument navigation through 
                    * Easy access to (online) documentaitn of packages
                    * word count 
                    * motion
                    * text objects
                    * improved fold
    * how to upload latext to overleaf from vim

-- 3.40 pm 

* check out Zhabiz paper format and make it fit mine. (survey paper)
    * trying to create draft 

--- 2/24/2021 5 pm 

* read the following paper
    * 2 Steering a Historical Disease Forecasting Model Under a Pandemic: Case of Flu and COVID-19
        * https://arxiv.org/pdf/2009.11407.pdf
    * 3. Incorporating Expert Guidance in Epidemic Forecasting
        * https://arxiv.org/abs/2101.10247
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

