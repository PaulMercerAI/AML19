# Group Project - AML challenge for maths in business
## Overview
The aim of this project is to develop a transaction classification mechanism that identifies Money Laundering activity in a set of fictitious financial transactions. AML is used in the financial services industry to mean Anti-Money Laundering. This is a huge problem globally as the proceeds of crime are "cleaned" through our financial institutions and used to perpetuate crime of the most serious nature, fund terrorism and reward the instigators/backers of people trafficking, drug and firearms smuggling and so on. 

Available for download from this repository are two synthetic data sets containing ficticious financial transactions. Both data sets contain two populations of actor; those engaged in Money Laundering type activity and those that are not. A smaller training dataset will have labels that identify the bad actors, and a larger dataset containing the same patterns of behaviour that does not have labels.

You will train your detection mechanisms using the training data then process the larger dataset. You will identify the top 200 transactions in the larger data dataset you believe are closest fit to money laundering behaviour to submit for processing. The processing is analogous to the real world handover to human investigagtors who have finite capacity; hence the limit of 200 transactions. You will receive back a percentage score of the transactions that were correctly classified as money laundering. Each group may submit up to five submissions with the best score being used in the assessment at the end.

To get you started we have developed a Jupyter Notebook on https://colab.research.google.com

## Background to Anti-Money Lanundering
According to the UN Office on Drugs and Crime if global money laundering were the econonomy of a country it would be the fifth largest country in the world at about [2.7% of global GDP](https://www.unodc.org/unodc/en/frontpage/2011/October/illicit-money_-how-much-is-out-there.html). The majority of serious crimes committed have a financial aspect to them. When talking about Organised Crime we are generally talking about criminal enterprises that are diverse in their nature and exist for the express purpose of making money. In particular they make a lot of money for the people at the top of these enterprises. These crime bosses are typically well organised and have substantial assets at their disposal in their endeavours to benefit from their activities and "investments" without prosecution. Money laundering is often essential to evading prosecution by both hiding the identity of the ultimate benefactor and in crossing administrative (often national) boudaries.
Governments require special treatment (screening) of people and organisations on watchlists which fall into two categories Politically Exposed Person (PEP) and Sanctions. That is out of scope for this challenge.
Governments provide rules and regulations for how financial institutions look for and prevent money laundering on their systems. Their agencies have been actively issuing "consent orders" to institutions that have been deficient. One merchant bank was both fined and ordered to cease operations, and the fines can be significant even for the biggest institutions. The biggest three single fines add up to $3.5 billion; HSBC having incurred the biggest fine:
> HSBC Holdings Plc agreed to pay a record $1.92 billion in fines to U.S. authorities for allowing itself to be used to launder a river of drug money flowing out of Mexico and other banking lapses. [reuters](https://www.reuters.com/article/us-hsbc-probe/hsbc-to-pay-1-9-billion-u-s-fine-in-money-laundering-case-idUSBRE8BA05M20121211)

It costs the financial institution to investigate every AML alert raised by the systems that monitor their transactions, hence the concern our customers have with the challenge of doing a good job of detecting money laundering without becoming uncompetitive in the market due to the spend necessary to investigate. BAE are a market leader in [detection of money laundering in financial transactions](https://www.baesystems.com/en/cybersecurity/product/aml-transaction-monitoring).

## Automated scoring
In order to reflect the real-world constraint of a human investigation team of finite capacity you are only permitted to send a small number (200) of transactions for assessment as suspected money laundering per submission, with a maximum of five submissions per group. You are expected to pick your top 200 transactions that your mechanism determines to be the closest match to money laundering patterns. You must attach the scripts that generated your output to the submission. You may optionally add a textual rationale of up to 255 characters to each transaction describing the detected behaviour to the investigator. Each submission you make will return a count of the money laundering transactions, but no assessment of the textual rationale, those associated with your highest scoring submission will be assessed, along with the scripts, by the scoring panel at a later point.

In practice we operate a Red Amber Green system where Red transactions are automatically stopped and reported to the authorities, Green are considered to be benign and the Amber channel routed to investigators, but that mechanism is out of scope of the activity.

## The data
Animation of a small transaction network. 96 benign accounts (blue), 4 money laundering accounts (red) using the "fan-in" pattern.
![money laundering network animation](https://raw.githubusercontent.com/PaulMercerAI/AML19/master/tx.gif?token=ANNPM7SPOVQ56HD5OWBPYN25TWEKA)

Ranked list of the top 10 relevant/discriminating features.
![top 10 features](https://raw.githubusercontent.com/PaulMercerAI/AML19/master/amlsim_relevance.PNG?token=ANNPM7XS6EVRUXVAHJZ2MIC5TWEWE)

Neural network performance data (90% detection rate)
![model performance](https://raw.githubusercontent.com/PaulMercerAI/AML19/master/AMLSim_neural.PNG?token=ANNPM7XIFKCHGVSD2W4DEW25TWEYC)

## Pre-requisites
### Maths
Standard algebra, polynomials, linear equations, graphing functions, logarithms and derivatives are essential or at least valuable.
### Programming
Whilst the examples provided are written in Python and use colab.google.com as the platform the challenge itself is language agnostic. The reviewers are happy to accept code submissions in other languages. If you look at the Jupyter (ipynb) notebook you will see that the code written is not sophisticated and is using only simple logic structures in order to call down onto supporting libraries.

## Optional crash course in Machine Learning
Google has provided a 15 hour crash course in the machine learning topics that underpin this exercise. It is *not* essential to know machine learning in advance, but might provide benefit. [A self-study guide for aspiring machine learning practitioners](https://developers.google.com/machine-learning/crash-course)

## Hints
Overfitting to the training data can be identified in part by training on half the training data then scoring against the other half.

##TODO
1. Introduce the Jupyter notebook - not displaying on GitHub
1. Describe the data schema
1. Describe the API for submission of models in more detail and provide an example for calling it in the example notebook
1. Describe the importance of classification and type of money laundering behaviour identified with examples.
1. Add red team hints
