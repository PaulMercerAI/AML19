# Group Project - AML challenge for maths in business
## Overview

This module provides a simulation of a real task that might be given in business. The specific context is detecting money laundering and has been constructed as a challenge set by BAE Systems Applied Intelligence specialists in this field. It is not expected that you will know all the skills and techniques ahead of the module; the ability to learn on the job is reflective of the tasks you can expect in many business scenarios.

You shall be tasked by a fictitious financial institution, a bank, to take a set of data they provide and identify and  transactions that are most likely to be associated with money laundering. The bank will have manually processed a subset of the data through manual investigation. You shall use the manually processed records that will be marked up with a boolean flag indicating whether or not the transactions are involved in money laundering to create a mathematical model or models that generate a probability of a transaction being involved in money laundering. You shall optionally categorise the behaviour of the money launderers with the manually processed records identifying four of the five types of money laundering activity present in the data. You shall run your model on transactions that have not been manually processed by the bank and submit the transactions most likely to be involved in money laundering for assessment by a scoring mechanism that simulates the processing the bank's financial investigations unit would perform.

We shall use the acronym AML as used in the financial services industry to mean Anti-Money Laundering. Producing systems that detect AML and manage the investigations is a significant part of the portfolio of BAE Systems Applied Intelligence. The same techniques used in this module have been used by BAE in a wide range of applications from identifying tax avoidance to at risk children in the care system.

AML is a huge problem globally as the proceeds of crime are "cleaned" through our financial institutions and used to perpetuate crime of the most serious nature, fund terrorism and reward the instigators/backers of people trafficking, drug and firearms smuggling and so on. A more comprehensive description appears below.

The module will start on 11 November 2019 with a presentation from a BAE manager and data scientist representing the bank's head of compliance and chief data scientist. You shall be able to ask clarification questions at that time. As is typical of customers their time with you shall be limited and controlled. 

There is a [Slack workspace](https://join.slack.com/t/aml19workspace/shared_invite/enQtODIyMjI3NDA5ODk0LTk1M2M4NTFjMDdmYjcxMDMzYzE5MzI1OGQyNDE2ZDQxYjNmMmUxYTgzZDNiOGVhOTg2Y2YwYThkYmRiOTUzNWE) where you will be able to receive scheduled additional information from the data scientist over the course of the module and can report any problems with the course materials. The hints and additional detail from the data scientist is reflective of the ongoing dialog that naturally occurs with a client during the task. Requests for help with the challenge and direct messages are not permitted.
You shall have a specific Q&A slot with the BAE manager and data scientist on 25 November 2019.

## Deliverables
* The top 1000 transaction IDs most likely to be involved in money laundering according to your model and a probability score in the range 0.0 to 1.0 that you have assigned as the likelihood the transaction is involved in laundering activity. Each transaction optionally marked up by category of money laundering behaviour. The code/steps used to produce the model is also required though any intellectual property licence you choose may be applied to the code. You shall the opportunity to submit up to five sets of transactions. Your highest scoring submission shall be used in the final assessment. Each submission shall receive an accuracy scode at or shortly after the time it is submitted.
* A 10 minute presentation on 09 December 2019 where your team shall be expected to explain how the results were obtained and then take 5 minutes of questions. Of interest to your client is the accuracy of your model(s), mathematical comprehensibility of your models (the manager has Maths and Further Maths 'A' levels; you should be prepared to rationalise/explain your approach at this level) and business comprehensibility of why the specific transactions were identified (in order to explain to why a record has been selected for investigation to a client of the bank or a government official).
* Comprehensive mathematical report describing your model and giving a solid justification for the results for assessment by your university tutor.

## Pre-requisites
### Maths
Standard algebra, polynomials, linear equations, graphing functions, logarithms and derivatives are essential or at least valuable.
### Programming
Whilst the example to be provided is written in Python and tested on https://colab.google.com as the platform the challenge itself is language agnostic. The reviewers are happy to accept code submissions in any programming languages. A Python Jupyter (ipynb) notebook will be provided at the launch of the course. The BAE data scientist will walk through the code. The code itself is not sophisticated and is using only simple logic structures in order to call down onto supporting libraries. Python was selected for this course because it is one of the easiest languages to learn and widely used in industry, including for data science. Its popularity means that a great deal of [Python training material is publically available](https://www.dataquest.io/blog/how-to-learn-python-for-data-science-in-5-steps/)

## Optional crash course in Machine Learning
Google has provided a 15 hour crash course in the machine learning topics that underpin this exercise. It is *not* essential to know machine learning in advance, but might provide benefit. [A self-study guide for aspiring machine learning practitioners](https://developers.google.com/machine-learning/crash-course)
In particular supervised learning for prediction and classification are likely areas to investigate, but starting simply looking for correlations and modelling using linear/polynomial methods should not be discounted.

## Out of scope
In an ordinary engagement of this nature a large portion of the time will be spent obtaining and cleaning the data. At the start of the module you will be supplied a clean set of data with no currupt/missing rows or fields and a description of the schema used. In the unlikely event you identify a problem with the integrity of the data you should contact BAE via the Slack workspace. 
There are no information handling requirements in this module since the data is wholly fictitious and the Data Protection Act, GDPR and other such legislation do not apply. Any resemblance between records in the generated data set and real individuals are wholly coincidental.

## Background to Anti-Money Lanundering
According to the UN Office on Drugs and Crime if global money laundering were the econonomy of a country it would be the fifth largest country in the world at about [2.7% of global GDP](https://www.unodc.org/unodc/en/frontpage/2011/October/illicit-money_-how-much-is-out-there.html). The majority of serious crimes committed have a financial aspect to them. When talking about Organised Crime we are generally talking about criminal enterprises that are diverse in their nature and exist for the express purpose of making money. In particular they make a lot of money for the people at the top of these enterprises. These crime bosses are typically well organised and have substantial assets at their disposal in their endeavours to benefit from their activities and "investments" without prosecution. Money laundering is often essential to evading prosecution by both hiding the identity of the ultimate benefactor and in crossing administrative (often national) boudaries.
Governments require special treatment (screening) of people and organisations on watchlists which fall into two categories Politically Exposed Person (PEP) and Sanctions. That is out of scope for this challenge.
Governments provide rules and regulations for how financial institutions look for and prevent money laundering on their systems. Their agencies have been actively issuing "consent orders" to institutions that have been deficient. One merchant bank was both fined and ordered to cease operations, and the fines can be significant even for the biggest institutions. The biggest three single fines add up to $3.5 billion; HSBC having incurred the biggest fine:
> HSBC Holdings Plc agreed to pay a record $1.92 billion in fines to U.S. authorities for allowing itself to be used to launder a river of drug money flowing out of Mexico and other banking lapses. [reuters](https://www.reuters.com/article/us-hsbc-probe/hsbc-to-pay-1-9-billion-u-s-fine-in-money-laundering-case-idUSBRE8BA05M20121211)

It costs the financial institution to investigate every AML alert raised by the systems that monitor their transactions, hence the concern our customers have with the challenge of doing a good job of detecting money laundering without becoming uncompetitive in the market due to the spend necessary to investigate. BAE are a market leader in [detection of money laundering in financial transactions](https://www.baesystems.com/en/cybersecurity/product/aml-transaction-monitoring).
