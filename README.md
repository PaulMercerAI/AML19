# Group Project - AML challenge for maths in business
## Overview
The aim of this project is to develop a _transaction filtering_ mechanism that identifies Money Laundering activity in a set of fictitious financial transactions. AML is used in the financial services industry to mean Anti-Money Laundering. This is a huge problem globally as the proceeds of crime are "cleaned" through our financial institutions and used to perpetuate crime of the most serious nature, fund terrorism and reward the instigators/backers of people trafficking, drug and firearms smuggling and so on. 

Available for download from this repository are two synthetic data sets containing ficticious financial transactions. Both data sets contain two populations of actor; those engaged in Money Laundering type activity and those that are not. A smaller training dataset will have labels that identify the bad actors, and a larger dataset containing the same patterns of behaviour that does not have labels.

You will train your detection mechanisms using the training data then process the larger dataset. You will identify the top 200 transactions in the larger data dataset you believe are closest fit to money laundering behaviour to submit for processing. The processing is analogous to the real world handover to human investigagtors who have finite capacity; hence the limit of 200 transactions. You will receive back a percentage score of the transactions that were correctly classified as money laundering. Each group may submit up to five submissions with the best score being used in the assessment at the end.

To get you started we have developed a Jupyter Notebook on https://colab.research.google.com

## Background to Anti-Money Lanundering
According to the UN Office on Drugs and Crime if global money laundering were the econonomy of a country it would be the fifth largest country in the world at about [2.7% of global GDP](https://www.unodc.org/unodc/en/frontpage/2011/October/illicit-money_-how-much-is-out-there.html). The majority of serious crimes committed have a financial aspect to them. When talking about Organised Crime we are generally talking about criminal enterprises that are diverse in their nature and exist for the express purpose of making money. In particular they make a lot of money for the people at the top of these enterprises. These crime bosses are typically well organised and have substantial assets at their disposal in their endeavours to benefit from their activities and "investments" without prosecution. Money laundering is often essential to evading prosecution by both hiding the identity of the ultimate benefactor and in crossing administrative (often national) boudaries.
Governments require special treatment (screening) of people and organisations on watchlists which fall into two categories Politically Exposed Person (PEP) and Sanctions. That is out of scope for this challenge.
Governments provide rules and regulations for how financial institutions look for and prevent money laundering on their systems, and can impose significant fines if an organisation lapes:
> HSBC Holdings Plc agreed to pay a record $1.92 billion in fines to U.S. authorities for allowing itself to be used to launder a river of drug money flowing out of Mexico and other banking lapses. [reuters](https://www.reuters.com/article/us-hsbc-probe/hsbc-to-pay-1-9-billion-u-s-fine-in-money-laundering-case-idUSBRE8BA05M20121211)
It costs the financial institution to investigate every AML alert raised by the systems that monitor their transactions, hence the concern our customers have with the challenge of doing a good job of detecting money laundering without becoming uncompetitive in the market due to the spend necessary to investigate. BAE are a market leader in [detection of money laundering in financial transactions](https://www.baesystems.com/en/cybersecurity/product/aml-transaction-monitoring).

##TODO
Include the NetworkX graphs showing the bad actor data
Introduce the Jupyter notebook
Describe the API for submission of models
Describe the scoring, including the importance of classification and type of money laundering behaviour identified.

## Hints
Overfitting to the training data can be identified in part by training on half the training data then scoring against the other half.
