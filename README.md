# README

Dear Reader and Judge, 

This document explains how to run the Protego code and how to access the prototype demo.

## What is going on?

The "Protego_backend_alpha.py" script plays a role in the backend of PROTEGOs dashboard for trend analysis and reputation management.

The prototype demo can be seen at: http://www.robots.ox.ac.uk/~favour/protego

## Machine Learning Algorithm
Method: GradientBoostingClassifier
Why:    It performed the best in our parameter analysis.

Others Tested: AdaBoost, XGBoost
Why Abandoned: The were outperformed by GradientBoostingClassifier on various parameters in our analysis.

Insight:
It is easy to get the performance up to 74% and difficult to get the performance alot higher. It is similarly hard to perform at more than 80% on the training set with the methods we attempted.

Our Assumptions: 
We restricted ourselves to usin the data given.
We restricted ourselves to ML approaches that we can train in a short amount of time, e.g. Deep Learning is too GPU-computation heavy.

## How to run the code
1. Open a python 3 environment with the following libraries installed: tqdm, sklearn, numpy, scipy, nltk

2. Run the python 3 file "Protego_backend_alpha.py" scans through the training data and evaluates on the test data. 

3. This gives a model, which can classify the relationship between the header and the body of texts.


## Our results

|               | agree         | disagree      | discuss       | unrelated     |
|-----------    |-------        |----------     |---------      |-----------    |
|   agree       |    173        |     10        |   1435        |   28          |
| disagree      |    39         |     7         |   413         |   238         |
|  discuss      |    221        |     7         |   3556        |   680         |
| unrelated     |    10         |     3         |   358         |   17978       |
Score: 8761.75 out of 11651.25     (75.20%)


