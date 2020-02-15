# Fairness in ML 
 
### Intro
  - it is getting really hot fields
  - 2018 2/5 awarding papers about fairness in ICML

### Motivation 
  - recommandAations 
  - the data provided by human can be highly biased, hehe
  - examples: 
    - COMPAS, the algorithm used for recidivism prediction produces much higher false  
      positive rate for black people than white people. 
    - XING, a job platform similar to Linked-in, was found to rank less qualified male   
       candidates higher than more qualified female candidates
    - Publicly available commercial face recognition online services provided by Microsoft,
      Face++, and IBM respectively are found to suffer from achieving much lower accuracy 
      on females with darker skin color. 
  - Bias in ML has been almost ubiquitous when the application is involved in people and it   
    has already hurt the benefit of people in minority groups or historically disadvantageous   
    groups. 
 
### Cause 
  - Tainted examples: Any ML system keeps the bias existing in the old data
    caused by human bias. 
  - bad data in general 

### Fairness Definition 
  - Unawareness
  - Demographic Parity
  - Equalized Odds
  - Predictive Rate Parity
  - Individual Fairness
  - Counterfactual fairness
  - Demographic Parity, Equalized Odds, and Predictive Rate Parity
  
### Unawareness 
  - disparate treatment: disparate treatment if its decisions are (partly) based on the subject’s   
    sensitive attribute, and it has disparate impact
  - disparate impact: it has disparate impact if its outcomes disproportionately hurt (or benefit)   
     people with certain sensitive attribute values (e.g., females, blacks) 
  - simply ignore senstive attribute 
  - Intuitive, easy to use and legal support(disparate treatment).
  - Flaws: highly correlated features(e.g. neighborhood) that are proxies of the sensitive attribute(

### Demographic Parity
  - C is independent of A: P₀ [C = c] = P₁ [C = c] ∀ c ∈ {0,1}
  - this means the acceptance rates of the applicants from the two groups must be equal.
  - Flaws: This definition ignores any possible correlation between Y and A. In particular, it
    rules out perfect predictor C=Y when base rates are different (i.e. P₀ [Y=1] ≠ P₁ [Y=1])
###  Equalized odds
  - Equalized odds, also called Separation, Positive Rate Parity,
  - In our example, this is to say we should hire equal proportion of individuals 
     from the qualified fraction of each group. 
  - Equality of Opportunity
### Predictive Rate Parity
  - Predictive Rate Parity, also called Sufficiency 
  - In our example, this is to say that if the score returned from a prediction algorithm   
    (used to determine the candidate’s eligibility of the job) for a candidate should  
    reflect the candidate’s real capability of doing this job. It is consistent with the  
    employer’s benefit.  
  - Flaw: The flaw is similar to the flaw of equality of opportunities: it may not help 
     closing the gap between two groups. The reasoning is similar as before.
### Individual Fairness
  - The notion of individual fairness emphasizes on that: similar individuals should be treated similarly.
  - FLAW: It is hard to determine what is an appropriate metric function to measure the similarity of two inputs. 
  - In our case, it is hard to quantify the difference between two job candidates. 

### Counterfactual fairness
  - A counterfactual value replaces the original value of the sensitive attribute.
  - The counterfactual value propagates “downstream” the causal graph(see Fig6 for an example) via some 
     structural equations. 
  - Everything else that are not descendant of the sensitive attribute remains the same.
  - Counterfactual fairness provides a way to check the possible impact of replacing
     only the sensitive attribute.
  - The idea is very ideal. In practice, it is hard to reach a consensus in terms of what
    the causal graph should look like and it is even harder to decide which features to use
     even if we have such a graph (we may suffer large loss on accuracy if we eliminate all 
     the correlated features).
  
### Trade-off between fairness and accuracy
  - The impact of imposing the above constraints on the accuracy truly depends on the
  dataset, the fairness definition used as well as the algorithms used. In general, however,
  fairness hurts accuracy because it diverts the objective from accuracy only to both 
   accuracy and fairness. 
   
### H0W ?
  - There are many algorithms that claim to help improve fairness. Most of them fall into    
    three categories: preprocessing, optimization at training time, and post-processing.
  - Preprocessing:  
     - The idea is that we want to learn a new representation Z such that it removes the
       information correlated to the sensitive attribute A and preserves the information of 
       X as  much as possible
  - Optimization at Training Time: 
     - The most intuitive idea is to add a constraint or a regularization term to the 
     existing optimization objective. 
  - Post-processing: 
     - Such methods attempt to edit posteriors in a way that satisfies fairness constraints.
       It can be used to optimize most fairness definitions(except counterfactual fairness).
    
  
  
  
  
  
  
  
  
  
  
  
  
