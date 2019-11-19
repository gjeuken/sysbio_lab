# From knowledge to network

1. In the article they mention that some systems are so large we have not yet fully mapped them, for example neurons within the human brain. However, I feel like there are a lot of examples where we might miss some interactions, for example in gene regulatory networks. Are there any thumb rules for when to accept a system "fully mapped"? Are there any tools for trying to predict if a connection or relationship is missing?

> When buiding a model, it is good to keep in mind the old adage "everything should be made as simple as possible, but no simpler." There are always things left out from your model, and at some point including more deltails on your model will detract from your ability to make inferences on that model, instead of helping.


2. Since many pathways in a cell are codependent on each other, is it possible to have a network of pathways? 

> Yes, it is absolutely possible, but before constructing such network, you have to ask yourself how you will study it and whether it will help you attack the problem you want to study.

3. In the readings, they state "Most networks of scientific interest are weighted, but we can not always measure the appropriate weights. Consequently we often approximate these networks with an unweighted graph. "

Does this mean that there is a way of measuring the weights of the links? If so, how?

> Usually, this is done the other way around. You have some phenomena that connects two things and you might want to use the strenght of that phenomena as the weight of the link between them.



# Networks in biology

1. Networks are a nice way to visualize interactions, but what conclusion can you draw from network analysis in a biological context beyond visualization?

> This is a very broad question, but I will point you to the fields of Systems Biology (!) and Network Medicine as good examples on where you might find your answer.


# Network properties

1. The concept of connected components was not very clearly described in the video. If you have 2 or more separated entities (each entity itself may consist of nodes that are linked via edges) that are not connected with each other, why are those not 2 independent “networks”. I don’t understand how a network can consists of multiple connected components, even though these are not connected (no common links) accordning to the youtube video.

> If a network is defined as a collection of nodes and links, there is nothing on that definition that states all nodes should be connected. You are correct that each of the connected components are also (sub)networks, but so is the original one.
It again depends largely on what you are modelling with the network.

2. In a bipartite network, wouldn't projection potentially make the interactions harder to interpret? As an example (not sure how correct it is), if looking at cancer diseases and genes, TP53 would be linked to many cancers (>50% of them according to Wikipedia), so projecting to get a disease graph would link lots of cancers due to TP53 even if they are otherwise not at all related (even if the fact that TP53 conncets them could be interesting in itself). 

> This again depends on different cases. You are (probably) correct that all cancers would be linked by TP53, but depending on how you construct the network, you might find other unexpected ways on which they are connected. The tool is only as your reason for using it.


# Network algorithms

1. In the jupyter notebook, the two graph traversal algorithms generate tree objects. What exactly do these depict/tell us?

> They represent all the nodes reached, connected by only the links used by the algorithm. If you remember, the algorithm never visits a node that has already been previously visited, therefore, there will be no cycles, and a network without cycles is a tree.

2. Is it the pathway analysis a part of network analysis or these two are totally different concepts? If they are different, could you clarify their differences, especially their usefulness in terms of situation?

> They are mostly separate methods. The most common pathway analysis methods only consider a pathway as a set of genes, and not a network.
