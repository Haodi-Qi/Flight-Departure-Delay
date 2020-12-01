# Flight-Departure-Delay
Project on U.S. Flight Departure Delay Prediction under SMU OPIM326 Services and Operations Analytics 

Author: Anant MOHAN, Daniel CHIN, Ethan CHEW, CHEN Fangqi, QI Haodi, Kenneth LEE

## Project Description
Given that airline delay will incur compensation cost and damange the brand reputation to the airlines, the goal of the project is to predict potential airline delays so that the airlines can take actions to mitigate the impact or even prevent it if possible.

Instead of the analyzing every airline, we zoomed in to Southwest Airlines (WN) only as it is the largest airline in terms of revenue and flight volume domestically. 

The focus is on departure delay because we discovered the high correlation (~0.94) between departure delay and arrival delay, and therefore reducing departure delay can effectively reduce arrival delay. Moreover, given a new flight, we do not have the data on the actual day of flight, such as duration of taxing in and out. Departure delay is also more likely to cause greater customer unsatisfaction since they have to wait in the longue or the plane.

## Analysis and Techniques
We conducted Descriptive and Predictive analysis on the dataset for the project. 

### Descriptive Analysis
These are the analysis we carried out under Descriptive Analysis to understand the dataset and discover possible insights
<ul>
  <li>Local market share distribution by flight volume</li>
  <li>Correlation between departure delay and arrival delay</li>
  <li>Distribution of departure delay and arrival delay</li>
  <li>Distribution of flight delay per airline</li>
  <li>Hypothesis 1: Busier airports leads to greater delays</li>
  <li>Hypothesis 2: Travelling season leads to greater delays</li>
</ul>

### Predictive Analysis
As the exact number of minutes of the flight departure delay may not be as significant (i.e. 15-min and 18-min delays do not make much a difference), we followed the Federal Aviation Administration (FAA) guideline and classify flights with more than 15-min delay as a delayed flight, and took it as a binary classification problem.

We split the dataset into train, validation and test sets with a ratio of 60:20:20 for model and feature exploration (train set), model and feature selection and tuning (validation) and final model evaluation (test). The evaluation metrics used are AUC, Precision, Recall and F1-score.

The final model selected is Logistic Regression with an AUC of 0.7185. 
