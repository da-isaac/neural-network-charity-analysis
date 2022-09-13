# neural-network-charity-analysis

## Overview
The purpose of this project was to help the company, Alphabet Soup, predict whether giving certain organizations donations would result in them utilizing the funds effectively to help fight to change the world for the better. The task was to determine if machine learning models would be a good predictor at this and be way for the company to analyze future orgs to donate to.

## Results
* Data Preprocessing
    * What variable(s) are considered the target(s) for your model?
        "IS_SUCCESSFUL" - the value that displays whether an org uses funding appropriately
    * What variable(s) are considered the feature(s) for your model?
        APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
    * What variable(s) are neither targets nor features, and should be removed from the input data?
        NAME, EIN
* Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
        The model I decided to stick with used "relu" activation function for the two hidden layers and ended with the "sigmoid" activation function. The first hidden layer contained 8 neurons and the second hidden layer contained 5. Compared to other neurons/layers that I tested, this combination resulted in the highest accuracy at 0.7256.
    * Were you able to achieve the target model performance?
        Despite multiple tests, I failed to reach a minimum 75% accuracy in model performance. 
    * What steps did you take to try and increase model performance?
        To try achieving the 75% accuracy score, I tested adding more neurons in each hidden layer (10 and 6 respectively), adding another hidden layer (with 3 neurons), and changing the output activation function to "tanh". None of these changes resulted in any increase - in fact, each of them saw slight (less than a thousandth) decrease in accuracy.

## Summary
Overall, the machine learning model still provides a decent guess at whether or not an organization will utilize its funding effectively (much better than a 50/50 random chance). However, because we already know the target variable, it may be possible that other supervised models are more appropriately suited to determine an org's success at using funds than this neural network model.