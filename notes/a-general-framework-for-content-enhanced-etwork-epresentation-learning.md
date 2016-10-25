# A General Framework for Content-enhanced Network Representation Learning

The authors proposed content-enchanced network embedding (CENE) to jointly learning the network structure and the content information. The approach integrates text modeling and structure modeling by treating the context as a special kind of node.

## Purpose

- The conventional network embedding only focus on the network structure information (the linkage), while large amount of node-related context text is available. If we can embed such context into vector and use it as an additional info of node. We can get better representation and understand the semantic meaning.

- Jointly learning the network structure and content means proper loss function needed to be designed for computing. It's cover the loss in rebuilding the network and text vectorization.

## Key Points

### Idea

- This work is inspired by ["Network representation learning with rich text information"](http://www.thunlp.org/~lzy/publications/ijcai2015_network.pdf).

- Loss function minimizes both the loss in SP (positive vertex) and SN (negative pair set).

- The framework embeds node-node link and node-content link. Specifically, content is embeded by sentence2vec.

- The paper introduce contents (document) as a special kind of nodes. So, the network is denotes as G=(Vn, Vc, Enn, Enc).

### Methodology

- Node-node link specify ***SP*** as ***Enn***

- In node-content link, use a composition function fe(.) to compute the content representation in order to fully capture the semantics of texts. It uses three model to represent the content: 1. Word Embedding Average, 2. RNN, 3. BiRNN.

## My Notes
