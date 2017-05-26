# Implementation of Oridinal Classification Paper using Logistic Regression and SVM  
### Introduction  
In this project, we seek to implement the ordinal classification paper here: http://www.cs.waikato.ac.nz/~eibe/pubs/ordinal_tech_report.pdf. A regular classification would treat each class as not having any order and would miss the inherent information that comes with ordering and this paper suggests a method to overcome this disadvantage.  

### Existing Work
Python has a package called *mord* which performs multiclass ordinal classification.  

### General Idea
The general idea is to build *k* - 1 classification models each predicting the probability of a data point being greater than a class value. 

### Implementation Details
We create a 1/0 field for all but final class and assign the value 1 if the class label is greater than the class of current column. We then go on to build classification models that predict the probabilty of 1/0. Once we have the probabilities, we derive the probabilities of current data point as belonging to each class. The class which has highest probability is assigned to the data point.

### Dataset
We use the winetesting dataset from UCI Machine learning repository: https://archive.ics.uci.edu/ml/datasets/Wine+Quality  


Proceed [here](ordinal-classification.html) for the analysis