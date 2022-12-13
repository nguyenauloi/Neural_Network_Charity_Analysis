# Neural_Network_Charity_Analysis
Module 19

# Project Overview

Our charity.csv dataset contains metadata from more than 34,000 organizations that have received a collective 20 Billion in funding from AlphabetSoup. The aim of this project is to analyze the impact of each donation by developing a deep learning neural network capable of reviewing large datasets via tensorflow.

# Results

## Data Preprocessing

In order to make sure our dataset had meaningful information we chose to drop the 'EIN' and 'NAME' columns as they neither features nor targets and were deemed unnecessary to use for prediction. This left us with the following:
 - APPLICATION_TYPE
 - AFFILIATION
 - CLASSIFICATION
 - USE_CASE
 - ORGANIZATION
 - STATUS
 - INCOME_AMT
 - SPECIAL_CONSIDERATIONS
 - ASK_AMT
 - IS_SUCCESSFUL

We determined to use the 'IS_SUCCESSFUL' column as our target and was later dropped after splitting our data. Also, to make things easier, many of these columns had their information converted into numerical format. 

## Compiling, Training, and Evaluating the Model

In our original iteration of the model we used the following:

<img src="<link>" width="300">

Through this model we were only able to achieve an accuracy of 68.7%
Subsequent training of this model were only able to achieve an accuracy score of 73%, just shy of the 75% goal. The additional training iterations included the following:
 - Epochs
    - 100 -> 50. The model reached an apex around 50 and it was deemed unnecessary to have any additional training beyond that
 - Hidden layers
    - The addition of a third hidden layer did not produce significant change and, at times, reduced the accuracy
    - Nodes were changed from 80 -> 100 -> 8 and 40 -> 60 -> 5 with little change
 - Increasing/Decreasing the bin value had inconsistent results


# Summary

Deep learning neural networks are able to produce useful insight into the viability of producing funding/aid to a project/organization with, mostly, reliable results. This sort of information would be invaluable in the decision making capability of AlphabetSoup's future endeavors. Our model was able to achieve an accuracy score close to, but not able to cross the threshold of, 75%. Additional exploration into dropping additional, unnecessary, columns could result in a higher score. Additionally, it would be important to recommend that a system like this needs a refresh or some sort of amendment every few years as the landscape of what projects/organizations requesting funding will change as needs are met or otherwise.