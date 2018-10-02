### Lecture 18: Feature Selection

#### 1. Introduction
+ Where do instances come from?
  - Examples from real world data
+ Where do attributes come from?
  - (Hopefully) meaningful features of the problem 
  - Anything that might capture regularity in the data
+ Where do models come from?
  - Need to choose a model suitable for our data set


#### 2. How to do ML
+ Process
  - 1 Pick a feature representation
  - 2 Compile data
  - 3 Pick a (suitable) algorithm for building a model
  - 4 Train the model
  - 5 Classify development data, evaluate results
  - 6 Probably: go to (1)

+ the job
  - Choose an algorithm suitable for classifying the data according to the attributes
  - Choose attributes suitable for classifying the data according to the model

#### 3. Feature Selection
##### Wrapper method
  - Choose subset of attributes that give best performance on the development data
+ Advantages:
  - Feature set with optimal performance on development data
+ Disadvantages:
  - Takes a long time

+ Improvement:
  - Greedy approach
    - Train and evaluate model on each single attribute
    - Choose best attribute
    - Until convergence:
      - Train and evaluate model on best attribute(s), plus each remaining single attribute
      - Choose best attribute out of the remaining set
    - Iterate until performance (e.g. accuracy) stops increasing
  - Ablation approach
    - Start with all attributes
      - 依次渐去改动最小的

    - Good: Mostly removes irrelevant attributes (at the start)
    - Bad: still time consuming; assume they are irrelevant

##### Embedded methods


##### Feature filtering
+ Intuition
  - possible to evaluate "goodness" of each feature, seperate from other features

+ filering methods
  - Feature goodness: highly correlated with class

### 1. PMI
+ Pointwise Mutual Information
  - Recall independence:
    - P(A, C) / P(A)P(C) = 1
  - If LHS ∼ 1, attribute and class occur together as often as we would expect from random chance
  - If LHS >> 1, attribute and class occur together much more often than randomly.
  - (If LHS << 1, attribute and class are negatively correlated. More on this later.)

+ PMI = log2(P(A, C) / P(A)P(C))
  - Note: joint P here means both are True (not means that both are same)
  - 1 => strongly correlated
  - 0 => not imformative ; not useful for the feature

+ What makes a single feature good?
  - Well correlated with class
    - A is Y, C is Y
  - Reverse correlated with class
    - A is N, C is Y
  - Well correlated (or reverse correlated) with not class 
    - A is Y, C is N

### 2. MI
+ Mutual information: combine each a, a¯, c, c¯ PMI 
+ Contingency tables: compact representation of these frequency counts
+ MI(A, C) = Ei∈{a,a¯}Ej∈{c,c¯} P(i, j)log2(P(i, j)/P(i)P(j))


#### diff between MI and PMI
+ In MI, we consider all the weights that the class is related to our class
  - positive, negative or ....

### 3. Chi-square


#### Types of Attribute
+ **Biased**
+ MI is sensitive to many values: choose with higher number of values
+ higher number of values ==> smaller subset of each value
  - lower error across each subset

#### multi-class
+ remove bad features

### A2
+ others:
  - there are many stop words due to many of them are not write in English
  - Mutual Information is biased toward rare, uninformative features
