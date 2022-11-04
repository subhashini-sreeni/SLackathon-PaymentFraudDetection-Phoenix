# SLackathon-PaymentFraudDetection-Phoenix
Payment fraud detection model 

## Contents

- [Short description](#short-description)
  - [What's the problem?](#whats-the-problem)
  - [How can technology help?](#how-can-technology-help)
  - [The idea](#the-idea)
- [Demo video](#demo-video)
- [The architecture and the flow](#the-architecture)
- [Implementation](#implementation)
- [Project roadmap](#project-roadmap)
- [Contributors](#contributors)

## Short description

### What's the problem?

With the current world rapidly adopting digital payment systems, the digital financial frauds that can be committed are increasing exponentially. According to The Nilsson Report, by 2030, when total payment card volume is expected to hit a whopping $79 trillion, the industry will lose an estimated $49 billion to fraud. With the US having a bigger share of the pie in many, by 2030, the US <b>digital fraud losses are expected to increase</b> their share of the pie to $17 billion in a total card volume of nearly $19 trillion. There have been cases reported of auctioning the credit card details of tons of users on ebay and amazon for few dollars.

There is a growing trend around the world to digitalize economic relations, like the concept “Bank-as-a-service” (BAAS) by banks around the world which is increasing the load on the payment systems. <b>The challenge is in being able to detect a fraudulent transaction within seconds of their initiation.</b> At the end of the day the aim is to be able to decline the fraudulent transactions and hence protect the interest of all genuine parties involved like the customer, the credit card holder, the credit card settlement company, the banks, or credit card issuing company etc. 

### How can technology help?
“Justice delayed is justice denied”. A delayed detection of fraud can only help in educating one to a certain extent, hopefully, to gain the knowledge, to be able to recognize it once again if it repeats itself in future. 

With the enormous number of digital transactions that take place per second, it is next to impossible for a human brain to comprehend all of them and detect the fraud within seconds. Technology like Artificial Intelligence, Machine learning and Deep learning can be used to train models that help in detecting the fraudulent transactions with <b> high accuracy and efficiency at a faster pace</b>.

### The idea

The aim is to be able to design a binary classification model that will be able to accurately and efficiently detect fraud that is low on false positives and high on true positives. However, the main challenge in designing such a system is in acquiring quality dataset. The datasets that are freely available on Kaggel and such other websites searched through google are highly imbalanced. Majority of the transactions in the datasets are genuine with very less percentage of fraudulent ones. 

The idea here is to build an inclusive system that not only imbibes the way the fraud detection systems are designed generally, but also build models that are based on <b>behavioural spending patterns of the individual users</b>.

The general design of fraud detection system is to design models based on Logistic regression, Liner SVM, Decision tree, Voting classifier, XGBoost etc., and compare their performances against the accuracy level provided by each model. The high accuracy model will be the desired one. 
We propose to extend this solution further to develop neural networks based on the individual user’s previous transaction behaviour and develop a pattern around the user behaviour. Once a DNN or CNN model is formed, for every transaction that the user performs the pattern can be observed to flag such a transaction as the one which needs further investigation. 

A transaction flagged for further investigation will lead to either 
<ol>
  <li> Detecting as a fraudulent transaction or </li>
  <li>A new pattern for the neural network to learn by way of back propagation.</li>
</ol>

This approach does have a limitation that it is not feasible to come up with a NN (neural network) model for each user. Depending on the requirement of the Bank or Credit card company, such models can be created for users who are in high-risk zones. Classification of the high-risk zone can be based on: 
<ol>
  <li> geographical location of the user </li>
  <li> geographical location of the transaction </li>
  <li> expenditure range or transaction amount and </li>
  <li> time-frame based transactions based on user’s input (like travel timelines) </li>
</ol>
  
  
## Demo video

## The architecture and the flow
![Video transcription/translation app](https://github.com/subhashini-sreeni/SLackathon-PaymentFraudDetection-Phoenix/blob/2ce06e821cb5faeb0a9d45f79562e9e2631c88bc/Prephase%20-%20Generic%20scenario%20model%20selection.png)


![Video transcription/translation app](https://github.com/subhashini-sreeni/SLackathon-PaymentFraudDetection-Phoenix/blob/6891e422d4373dce9b1d7b48141422af5a316040/Prephase%20-%20single%20user%20model%20selection.png)

![Video transcription/translation app](https://github.com/subhashini-sreeni/SLackathon-PaymentFraudDetection-Phoenix/blob/6891e422d4373dce9b1d7b48141422af5a316040/Execution%20Phase.png)

## Implementation
The dataset has been downloaded from kaggle. Reference:- [Credit card fraud detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) <br>
<b>Important points to be noted:-</b>
1. Due to confidentiality issues the data set available online isn't having the actual feature names. Only Time and Amount are readable ones. While Amount is the total transaction amount, the Time column is the number of seconds elapsed between the transaction in consideration and the very first transaction of the dataset. <br>
2. The column Class with value 1 indicate fradulent transaction and with value 0 indicate a legitimate transaction. The data set has 284315 legitimate transactions only 492 fradulent transaction. Hence the fradulent transactions are about 0.17% of the data set resulting in a very imbalanced data set. Given this data set limitation, the model selection has the contraint that the model being suggested after accuracy check might change in real life scenario, with live data. <br>
3. The data set has PCA applied which indicates that the initial stages of data preprocessing wherein the unrequired features, null values, non-categorical values etc., have already been handled. Hence the implementation has code snippets to show how data preprocessing can be handled but as such doesn't add any value to the current data set.

Implementation has been divided into 2 main files. 
1. [FraudDetectionModelSelection_NUsersData.ipynb](https://github.com/subhashini-sreeni/SLackathon-PaymentFraudDetection-Phoenix/blob/54cac2281c0db5c69f3117ed268969676d09db76/implementation/FraudDetectionModelSelection_NUsersData.ipynb) which handles the architectural and flow implementation for scenario that handles 'N' number of users credit card transactions. 
2. FraudDetectionModelSelection_1UserDatum.ipynb which handles the architectural and flow implementation for scenario that handles 'N' number of credit card transactions that a single user performs, mainly to capture the spending pattern of the user. 

## Project roadmap

## Contributors
### Aniruddha Talekar
### Subhashini S

