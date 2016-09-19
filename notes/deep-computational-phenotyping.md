# Deep Computational Phenotyping

The authors proposed a deep learning framework that can learn richer, data-driven descriptions of illness. They focus on two modifications to standard neural network 1) introduce prior knowledge to regularize parameter, 2) a incrimental training procedure to learn a various of model to infer phenotype.

## purpose

1. learning robust representation of human physiology.

2. overcome the shortcoming of DHR(digital health record) that each class only links to few records for neural network traning.

3. apply exsiting medical knowledge into computation.

## Key Points

- Construct the clinical record into time series data with P variables(medical, procedure, labtest ? see below) and length T. Then, use a simple mapping that stack all T columns into one vector x. They also pretrain each hidden layer as a denosing autoencoder(DAE). The network architecture is a general framework, which use fully connected layers and **sigmoid** nonlinearities.

- Apply Graph Laplacian-based regularization to utilize relational information like tree-based prior and represent any pairwise relationships between parameters.

- There are two varieties of prior: structured domain knowledge and data-driven similarity. The paper using ICD-9 codes as labels and treat their ontological structure as prior knowledge. 

- Laplacian regularization also incorporate empirical priors, in the form of similarity matrics, estimated from data.

- Add regularity into loss function.

- Incrimental training accelerate the training of new network parameters by utilizing the old (shorter input) network. In experiment, they train a series of neural networks designed to model and detect patterns of lengths(12, 16, 20, 24) to evaluate the efficacy 

## My Notes

- How to define the variable in the input matrix. Is it the medication or clinical procedure or lab test?

- What is the *K* binary labels? Disease or medication?



















