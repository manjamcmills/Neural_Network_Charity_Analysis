# Neural_Network_Charity_Analysis

## Overview of Analysis
"Alphabet Soup" is a non-profit philanthropic foundation. The charity has raised and donated over $10 billion over the past 20 years.  The purpose of this analysis is to examine the impact of each donation to help decide which organizations are worth donating to and which are too "high risk".  The goal is to create a mathematical data driven solution that can do this accurately.  Because of the complexity of this analysis, a "deep-learning" neural network seems like the best approach. The python Tensor-Flow library was used to design and train these models.

## Results
### <b> Data Preprocessing </b>
The was only one TARGET for the model: 
* IS_SUCCESSFUL—Was the money used effectively?

The following variables were the FEATURES for the model: 
1. EIN and NAME—Identification columns
2. APPLICATION_TYPE—Alphabet Soup application type
3. AFFILIATION—Affiliated sector of industry
4. CLASSIFICATION—Government organization classification
5. USE_CASE—Use case for funding
6. ORGANIZATION—Organization type
7. STATUS—Active status
8. INCOME_AMT—Income classification
9. SPECIAL_CONSIDERATIONS—Special consideration for application
10. ASK_AMT—Funding amount requested

Before the optimization, "EIN" and "NAME" were dropped
After the optimization, only "EIN" was dropped
    
### <b> Compiling, Training, and Evaluating the Model </b> <br> 

#### Neurons, Layers, and Activation Functions
* I ended up with 2  hidden layers, with the 1st hidden layer having 80 neurons and the 2nd hidden layer having 30 neurons. This was the same as in Deliverable 1 & 2. I tried other combinations, but this worked best for me.
  
* I used the RELU activation for both hidden layers since our data ranged from 0 to really large numbers.
  
* I used the SIGMOID activation for the output layer since we wanted a "1" for successful or "0" for unsucessful.

#### <b>Target Model Performance</b>

I was able to surpass a target predictive accuracy higher than 75%, with 78.97% accuaracy.  I tried several different variations. Here are some of the steps that I took:

<b>ORGINIGAL MODEL --> accuarcy =64.37% </b>
   *  "EIN" and "NAME" columns were DROPPED
   *  APPLICATION_TYPE was grouped to "other" with value_counts < 528
   *  CLASS_COUNTS was grouped to "other" with value_counts < 1883
  
<b> OPTIMIZATION #1 --> accuarcy = 70.01%   </b>
   * UN-drop the NAME column. I grouped all of the NAME columns that had a value_count < 500 to "other"<br>
  
<b> OPTIMIZATION #2 --> accuarcy = 78.97%   </b>
* I found out that 54.7% of the NAME columns were equal to 1. &nbsp;  I grouped all of the NAME columns that had a value_count < 2 to "other"


<b> OPTIMIZATION #3 --> accuarcy = 76.20%   </b>

* APPLICATION_TYPE was grouped to "other" with value_counts < 16. 


## SUMMARY
