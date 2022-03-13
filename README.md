# Language modelling with Markov Models

This project is based on methods proposed by L. Saul and F. Pereira, Aggregate and mixed-order
Markov models for statistical language processing (Second Conference on Empirical Methods in
Natural Language Processing, 1997, https://aclanthology.org/W97-0309). It is concerned
with studying and implementing Markov Chains and two versions of the Expectation-Maximisation
(EM) algorithm proposed in the cited paper.

Markov Chains are seen as the simplest model where
transition probabilities are computed by looking at normalised frequency counts of adjacent word
pairs in the training text, which returns maximum likelihood estimations. Aggregate models introduce
the notion of hidden classes having probabilistic relationships with the observed word sequences
and involve a hidden variable density estimation problem. Mixed-order models do not use hidden
variables but try to exploit and combine probabilistic relationships between non-adjacent words, thus
allowing the model to account for more information coming from a word’s past in the observed
sequence. Two different versions of the EM algorithms were used to implement these last two model
types.

Log-likelihood and perplexity were computed for Aggregate and Mixed-Order models as these
models involved some hyper-parameter tuning, for relative comparisons.

Sample texts used in the Experiments sections were drawn from the Harry Potter and the Philosopher’s Stone novel. The reference paper employs 78 million words as a training text. Only small
samples of no more than 500 words were used in this work due to limited computational resources and
the quadratic time complexity of the EM algorithms. Slightly larger samples (1000, 2000 words) were
used at times for the practical application but the relative models were not analysed systematically.
Overall results are expected to show the same behaviour as those presented in the paper, though will
probably scale down in quality. As an application which is not part of the original paper, models were
used to generate new sentences to test their generative power. Strategies and results will be discussed
in the relative Experiments sections.
Each of the three model types was implemented in a separate Python notebook. All notebooks can be found in this repository.

This work was part of the Natural Language Processing course at the University of Genoa, Italy (Data Science and Engineering MSc, Artificial Intelligence track, 2021/22).
