# FAQs

* how do i know if graph embedding learn about graph structure?
    * what defined structure of a graph?

# NOTE
* streaming 
    * Finish implementing and writing new research idea in 2 weeks: day 1/14

# references
* first gcn paper 
    * https://arxiv.org/pdf/1609.02907.pdf
* first lstm paper
    * 

# Experimental LOG
* [DONE] experiment 1: testing visibility graph on stock market and straight line 
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

* experiment 5: get performance of the model but using graph2vec embedding as the graph embedding components.
    * faqs
        * should I use static or dynamic graph2vec?
    * 

* experiment 6: apply graph cluster to graph2vec.
    * goal 
        * goal is to observe whether similar graph embedded is generated from time series window with similar properties?
            * expectation
                * I expect to see a smoothing shift of graph embedding as time windows slides forward
    * note
        * After graph2vec is applied to all ts data, apply

    * system requirement 
        * graph needs to be smoothly change as time increases.
            * possible solution
                * here> I can stack up visibility graph embedding from multiple time steps. 
                * try dynamic graph embedding (embedding graph from multiple time step) 
            * I need to convert time series to graph such as graph is not dramatically changed in the next time step. 
                * currently visibility graph doesn't have this properties
                    * for example 
                        * here> a local peak "peak" dramatically block "view" of the immediate next time step.  
    * todo 
        * investigate again what graph looks like before and after peak.
            * is there a scenario where all nodes are disconnected? (value at time step right after peak.)
                * if there are, how do we solve this problem? 
                * can "inverse visibility graph" be used for this?

* experiment 7: for node2vec embedding, calculate stability dynamic network embedding.
    * ref
        * https://roamresearch.com/#/app/AdaptiveGraphStucture/page/bbxs1fqN7 

# TODO

* write dr zhu about this experiments.
    * write purposed model.
        * hand writting it

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
        * here> try experiment 6 
        * figure out a way to extends node2vec to GCN.
            * see example of how other paper add GCN in their 
                * cola gnn 
                    * here> figure out how Message Passing part is implemented.
                    * https://github.com/amy-deng/colagnn
            * once finished implementing GCN, I can start 
