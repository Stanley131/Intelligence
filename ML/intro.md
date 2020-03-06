### MLE
  - Probabilite: Knowing paramtres → prediction of outcomes
  - Likelihood: Observation of data → estimation of parameters
  - Prior probability, in Bayesian statistical inference, is the probability 
    of an event before new data is collected. 
  - That revised probability becomes the posterior probability and is 
    calculated using Bayes' theorem.
  - Maximum likelihood estimation is a method that will find the values of μ
    and σ that result in the curve that best fits the data.
  -  Maximum likelihood estimation is a method that will find the values of         parameters to best expain the data. 
 ### Gaussian Distribution
  - mean
  - variance 
 ### Multivariate Distribution 
 ### Classification Methonds 
  - text classification, supervised learning
  - Naive	Bayes	is	Not	So	Naive
 
### P Model 
  - Bernoulli Distribution: 
    - mean: p 
    - variable: p(1-p)
  - binomial distribution: 
    - mean: np 
    - np(1-p)
  - Geometric disteribution: 
    - mean: 1/p
    - variance p / (1 - p)^2
  - multinomial distribution: 
    - n!/(n1! * n2!...) * P1^n1 * p2 ^ n2 
  - Posisson distribution: 
    - a model for a series of discrete event where the average time between events 
      is known, but the exact timeing of events is random. 
    - the arrival of an event is independt of the event. 
    - e^(-u) * mean ^x / x!
    - mean = variance 
### Ginie index vs Entropy 
  - Decision tree algorithms use information gain to split a node. Gini index or entropy is the
    criterion for calculating information gain. 

### parametric vs non
  - The term “non-parametric” might sound a bit confusing at first: non-parametric does not mean that they have NO parameters! On the contrary, non-parametric models (can) become more and more complex with an increasing amount of data.

So, in a parametric model, we have a finite number of parameters, and in nonparametric models, the number of parameters is (potentially) infinite. Or in other words, in nonparametric models, the complexity of the model grows with the number of training data; in parametric models, we have a fixed number of parameters (or a fixed structure if you will).
