# Starbucks Capstone

## Project Motivation

This project is an anlysis of the Starbucks rewards mobile app data. Data is collected on different aspects of the mobile app usage. The marketing team at Starbucks wants to know the demographics of the users who complete an offer so that they can come up with marketing campaigns that can target those customers. This can help increase the efficiency of marketing campaigns by targeting customers who are more likely to complete an offer rather than targeting customers who are less likely. To help the marketing team we will be looking at the following questions:

1) What is the gender, age, income and member_since data of the users who complete an offer?
2) What is the channel distribution of users who complete offers?
3) Build a model to predict if a customer would complete an offer based on the demographics.

## Data

To answer these questions we will look at the following files:

1) portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
   Columns:
   - id (string) - offer id
   - offer_type (string) - type of offer ie BOGO, discount, informational
   - difficulty (int) - minimum required spend to complete an offer
   - reward (int) - reward given for completing an offer
   - duration (int) - time for offer to be open, in days
   - channels (list of strings)
   
2) profile.json - demographic data for each customer
   Columns:
   - age (int) - age of the customer
   - became_member_on (int) - date when customer created an app account
   - gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
   - id (str) - customer id
   - income (float) - customer's income
   
3) transcript.json - records for transactions, offers received, offers viewed, and offers completed
   Columns:
   - event (str) - record description (ie transaction, offer received, offer viewed, etc.)
   - person (str) - customer id
   - time (int) - time in hours since start of test. The data begins at time t=0
   - value - (dict of strings) - either an offer id or transaction amount depending on the record
   
## Libraries

To analyse the data we will be using Python 3.0 with the following libraries: numpy, pandas, matplotlib, seaborn and sklearn.

## Summary

About the same percentage of customers (49.2%) of males and females complete a BOGO (Buy One Get One) offer.
Customers who are less than 500 days are more likely to complete a BOGO offer which might suggest customers sign up just to redeem BOGO offers.
Mobile is the preferred channel through which customers who completed an offer received the offer.

## Acknowledgement

I would like to thank Udacity and Starbucks for providing the data for this project.
