# NLP_Project
NLP Project
How to run
Put the ipynb file in the colab or vscode and click to run all the parts

Description
The project is about the development of an evi- dence retrieval module to identify relevant evi- dence passages from a corpus, and a label clas- sification module to categorize claims based on the retrieved evidences. Various techniques like TF-IDF filtering, transformer encoder models, and recurrent neural networks (LSTM, RNN, GRU) are explored. Experiments reveal limi- tations in both modules leading to suboptimal performance, and highlighting the need for fur- ther improvements in areas such as data quality, model architectures, and training strategies

DataSet
[train-claims,dev-claims].json: JSON files for the labelled training and development set;

[test-claims-unlabelled].json: JSON file for the unlabelled test set;

evidence.json: JSON file containing a large number of evidence passages (i.e. the “knowledge source”);

dev-claims-baseline.json: JSON file containing predictions of a baseline system on the development set;

eval.py: Python script to evaluate system performance (see “Evaluation” below for more details).

Methods
Evidence Retrieval Module: The word2v will have a pre-trained vector representation of each word in the word bank, and then the semantic and contextual information of the word can be captured through these vectors, and finally the embedding vectors are fed into the Transformer encoder. The next step is to process these embedding vectors directly with the Transformer encoder, and finally further capture the long distance dependencies and complex semantic information in the text, and then further narrow down the evidences with top-k 3.

Transformer Encoder Models: Leverages transformer architectures for enhanced context understanding.

Recurrent Neural Networks: Explores LSTM, RNN, and GRU networks for sequence modeling.

Experiments and Results

LSTM: Evidence Retrieval F-score (F) = 0.09831478045763758 Claim Classification Accuracy (A) = 0.6038961038961039 Harmonic Mean of F and A = 0.16909995044696377

RNN: Evidence Retrieval F-score (F) = 0.0983147804576375 Claim Classification Accuracy (A) = 0.461038961038961 Harmonic Mean of F and A = 0.16206897665755013

GRU: Evidence Retrieval F-score (F) = 0.0983147804576375 Claim Classification Accuracy (A) = 0.44805194805194803 Harmonic Mean of F and A = 0.16124747942286635

Future Work
Data Expansion: Increase training data to improve model robustness. Avoid overfitting with careful data handling.

Hardware Upgrade: Utilize higher-performance hardware for broader parameter testing and optimization.

Technology Integration: Explore advanced deep-learning models and larger-scale pre-trained models. Implement efficient optimization algorithms and enhanced regularization techniques.
