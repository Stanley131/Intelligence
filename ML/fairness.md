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
  - 
  
  
  
