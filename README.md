# Neural_Network_Charity_Analysis

## Overview of Analysis
"Alphabet Soup" is a non-profit philanthropic foundation. The charity has raised and donated over $10 billion over the past 20 years.  The purpose of this analysis is to examine the impact of each donation to help decide which organizations are worth donating to and which are too "high risk".  The goal is to create a mathematical data driven solution that can do this accurately.  Because of the complexity of this analysis, a "deep-learning" neural network seems like the best approach. The python Tensor-Flow library was used to design and train these models.

## Results
### Data Preprocessing
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
After the optimaization, only "EIN" was dropped
    
### Compiling, Training, and Evaluating the Model