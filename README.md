
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

1. Anaconda distribution of Python version 3.6 or later

## Project Motivation<a name="motivation"></a>

Understanding customers is the  key for any business. To understand them well, organizations need to pay attention to their purchase behaviour. One way is to collect and analyze their purchasing behaviour through an app, then identify their needs based on demographics.

The Starbucks [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025) Capstone challenge data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Periodically, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). However, some users might not receive any offer during certain weeks.
Using the data, I aim to :

- Gain understanding of customer demographics and their purchase behaviour
- Find out What offer should be sent to each customer ?
- Predict if a customer will complete an offer given demographics information and offer details

An unsupervised machine learning model with K-Means algorithm is used to cluster the customers. 

A supervised machine learning model with classification to predict if a customer will complete an offer sent by Starbucks


## File Descriptions <a name="files"></a>

### Notebooks
There  are 3 notebooks available:
- part 1 Data Understanding and cleaning
- part 2 Feature Preprocessing and Clustering
- part 3 Customer prediction using supervised machine learning


### Helpers function
There is a `helpers.py` as utilities and also to extract features from the available data.

### Dataset
The dataset is in folder data, contained in three files:

- `portfolio.json` - containing offer ids and meta data about each offer (duration, type, etc.)
- `profile.json` - demographic data for each customer
- `transcript.json` - records for transactions, offers received, offers viewed, and offers completed

The description of data is as follows:
`portfolio.json`
- `id` (string) - offer id
- `offer_type` (string) - type of offer ie BOGO, discount, informational
- `difficulty` (int) - minimum required spend to complete an offer
- `reward` (int) - reward given for completing an offer
- `duration` (int) -
- `channels` (list of strings)

`profile.json`
- `age` (int) - age of the customer
- `became_member_on` (int) - date when customer created an app account
- `gender` (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- `id` (str) - customer id
- `income` (float) - customer's income

`transcript.json`
- `event` (str) - record description (ie transaction, offer received, offer viewed, etc.)
- `person` (str) - customer id
- `time` (int) - time in hours. The data begins at time t=0
- `value` - (dict of strings) - either an offer id or transaction amount depending on the record

