# Starbucks Data Clustering Analysis

## Project Introduction

The dataset of this project comes from an simulated experiment created by Starbucks. It includes 17000 customers who are delivered different kinds of promotional offers randomly, and these offers belong to three types — bogo (buy-one-get-one), discount and informational(no rewards, just provide information of products). Every 6 hours these customers’ purchasing activities were recorded and the whole experiment lasted about a month. The target of this project is to explore the dataset and find which customer groups are most responsive to each type of offer.

You can read details of this project in my medium blog: https://harold-zeng.medium.com/which-kind-of-promotional-offer-do-you-like-analysis-for-starbucks-customer-groups-17a4fd640c81

### Dataset

The dataset contains three files:

- **portfolio.json** - including full descriptions to 10 kinds of  promotional offers coming from three types(bogo, discount and informational).
- **profile.json** - including 17000 customers' id and their detailed information.
- **transcript.json** - including 306534 data that records purchasing activity of those 17000 customers in 30 days.

### Target

It can be considered as an unsupervising learning problem. Therefore, I use **kmeans** clustering method to divide customers into three groups: a group including people who like bogo offers most, a group including people who like discount offers most and a group including people who like informational offers most.

### Method

I used following steps to do data clustering analysis.

1. **Explore the dataset and do som data visualization.**
2. **Preprocessing data, find suitable features to describe each user and create users dataframe**
3. **Use kmeans to clustering users into three groups, analyze characteristics of each group and find which group are most responsive to each type of offer.**

### Result Analysis

After clustering, I divide all customers into three groups: group 0 is most responsive to informational offers, group 1 is most responsive to discount offers, and group 2 is most responsive to bogo offers. Characteristics of each group I found are as following.

#### Group 0:

- Most customers are **under 60**.
- almost **one-third** are **unwilling to provide** their **personal information**.
- income of most users is **not more than $70000**.
- most are **new user** who became members in Starbucks for **less than 1 year**.

#### Group 1:

- **mean** age is **60**.
- just **a little part** of them are **unwilling to provide** their **personal information**.
- **more male** customers.
- **mean** income is **not more than $70000**.
- **most** have became members for **1 or 2 years**.

#### Group 2:

- **mean** age is **60**.
- almost all customers are **willing to provide** their **personal information**.
- number of **female** and **male** customers are **almost the same**.
- **mean** income is about **$70000**.
- **most** have became members for **more than 1 year**.

### Conclusion

In summary, for those young, lower income, information unknown and new customers, they may more interested in informational offers, and for rest customers, there are not clear boundaries between group 1 and group 2, delivering them bogo offers and discount offers are all good choice. What’s more, customers with high income might be more responsive to bogo offers.

## Libraries

All libraries I used in this project are as following:

- numpy
- pandas
- matplotlib
- seaborn
- sklearn
- warnings

## Description of each file

- data, including three files.

> - portfolio.json
> - profile.json
> - transcript.json

- Exploring.ipynb - code used to explore the dataset and do some data preprocessing.
- Clustering.ipynb - code used to create users dataframe, clustering users into three groups and visualize the clustering results.

## Acknowledgement

Data Source - Starbucks dataset.





