# NOTE
* streaming 
    * Finish implementing and writing new research idea in 2 weeks: day 1/14

# references
* first gcn paper 
    * https://arxiv.org/pdf/1609.02907.pdf
* first lstm paper
    * 

# Experimental LOG
*  experiment 1: testing visibility graph on stock market and straight line 
    * observation 
        * I applied visibility graph to time series with/without normalized, it doesn't seem like embedding helps learning at all.
            * note that no hyperparameters are tuned at this point
            * the model cannot fit straight line.
    * future direction 
        * figure out why the model cannot fit straight line.
            * why is this the case?
                * could this be due to node2vec?
                    * what is the node2vec embedding of straight line?


*  experiment 2: visualize node2vec embedding on straight line. 
        * read node2vec paper to be more sure of what node2vec is capable of then decide whether ndoe2vec is appropiate for this usecase.
            * shoudl I implement GCN version?
    * goal 
        * to figure out if node2vec of all straight line.

* experiment 3: run ndoe2vec on weighted visiblity graph

* experiment 4: evaluate good scheme "good embedding" for next time step prediction.
    * requirement 
        * here> what are the property of dynamic graph with fixed nodes and constantly changes edges?
            * what kind of embedding should this be used?
            * here> how can I evaluate quality of node embedding?
                * here> Given the current visibility graph within a given time windows, nodes embedding should be able to predict its edges pairs of the next visibility graph.
                    * should node embedding of the current timestep predict next or current edges of visibility graph?
                    * here> can node embedding do this?

# TODO

* here> compare performance of purposed methods to the baseline methods  
    * implement lstm and GRU baseline
        * here> baseline is GRU on stock prediction
            * herE> https://medium.com/swlh/stock-price-prediction-with-pytorch-37f52ae84632#:~:text=Stock%20market%20prediction%20is%20the,value%20of%20a%20company%20stock.&text=Here%20we%20are%20going%20to,terms%20of%20time%20and%20efficiency.

    * here> implement purposed model  
        * how to do multivariate lstm
            * https://stackoverflow.com/questions/56858924/multivariate-input-lstm-in-pytorch
                * here> implement lstm and separate price and features
        * note
            * node2vec doesn't really work.
        * try experiment 4 (see experimental log)
        * figure out a way to extends node2vec to GCN.
            * see example of how other paper add GCN in their 
                * cola gnn 
                    * here> figure out how Message Passing part is implemented.
                    * https://github.com/amy-deng/colagnn
            * once finished implementing GCN, I can start 
