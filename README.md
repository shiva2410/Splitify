# Splitify
## Best Fund Splitter, Ever


[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Splitify is a cloud-enabled, mobile-ready, real time fund splitter. It is works smoothly on any platform and has features to notify the user about their share.

## Quick start

Clone repo, then:
- npm install
- npm start


## Features
- It is a cross-platform app which is :
  - Supported with browsers like Google Chrome, Safari, Mozilla Firefox, Microsoft Edge.
  - Supported with iOS and Android.
- Prototype can be scaled to more than 100 users and user can add more than 100 products.
- Split expenses equally, by percentage, or by shares.
- Create multiple groups and add unlimited users.
- Integrates with ZETA’s API.
- Real-time calculation of the inputs done by the user.


## Approach
- The idea is to use Greedy algorithm where at every step, settle all amounts of one person and recur for remaining n-1 persons. 
- To pick the first person, calculate the net amount for every person where net amount is obtained by subtracting all debts (amounts to pay) from all credits (amounts to be paid).
- Once net amount for every person is evaluated, find two persons with maximum and minimum net amounts. These two persons are the most creditors and debtors.
- The person with minimum of two is our first person to be settled and removed from list. Let the minimum of two amounts be x. 
- We pay ‘x’ amount from the maximum debtor to maximum creditor and settle one person. If x is equal to the maximum debit, then maximum debtor is settled, else maximum creditor is settled.
