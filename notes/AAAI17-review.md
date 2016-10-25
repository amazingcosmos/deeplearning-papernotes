# Interaction Content Aware Network Embedding via Co-embedding of Vertices and Edges

## Purpose

- By co-embedding the vertices and edges to realize the idea of interaction content
 aware network embedding (ICANE).

- Overcome the shortcoming of conventional network embedding methods that only
 preserve the linkage information but ignore the interaction content.

## Key Points

**Ideas**

- Interaction content can be observed in various networks. Such as the picture you
 two both comment or like, the paper you are co-authors, the news you both reading.
 
- The content contains the vertex interaction preferences, which distinguish different
 types of edges in detail.

- There are two flavor of ICANE, ICANE-N and ICANE-R. The ICANE-N further construct a
 k-nearest neighbor (KNN) network of the edge, while ICANE-R regularize the edge 
 embedding by incorporating the interaction content into latent space.
 
**Methodology**

- Network is denoted as G(V, E, C), where C is the set of content associated with edges.

- Clossness of vertices is defined by implying the sigmoid function to inner-multiple of
 two vertex embeddings.

- ICANE-N preserve 1. the clossness of connected vertices, 2. the clossness of vertex
 and its edges, 3. the clossness of two edges if they are close in KNN network.

- Penalty is designed by the negative natural logarithmic funcion, which penalize small
 probability of (vertex, vertex) pair if there exist links.
 
- To calculate all the combinations of vertices/edges is impractical, the author use
 negative ratio to set the amount of random combination as several times larger than
 real ones.

- For ICANE-R, a projection matrix M to be estimated. So, they minimize the difference
 of **EM** and **C**, where E is the edge embedding matrix and C is the term frequence
 matrix.
 
- Optimizing the loss function by *iterative iptimization algorithm*, in which a joint
 optimization problem is solved with respect to one of the variables with other variables
 fixed.
 
- Pre-training was performed on *V* and *E* in ICANE-N and *E* in ICANE-R.

- Learning rates are obtained by *backtracking line search*.
 
**Evaluation**

- Evaluate the latent features on common data mining tasks including visualization, 
 multi-label classification, multi-class classification and link prediction.
 
- Embedding dimension is set as **128**.

- Similarity between papers is quantified by the cosine similarity on the **paper abstract**.
 

## My Notes

- The paper mentioned that in co-authors problem, the authors with multiple interests
 may mislead the learning of their co-authors' location. But, how the proposed method
 can overcome this misleading problem?
 
- If ICANE-R can better understand the content, why ICANE-N cannot? Both model try to
 catch the semantic meaning in content, while ICANE-R is like BOW and ICANE-N is KNN
 of edges. Does BOW perform better than KNN?
 
- 





















