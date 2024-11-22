# Neural Network Model Report

## Overview

The nonprofit foundation Alphabet Soup wants a tool that can help it select applicants for funding with the best chance of success in their ventures. Provided with a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years, the purpose of this analysis is to use features in the provided datset to create a binary classifer that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results

### Data Preprocessing:

* Target Variable:
  * **IS_SUCCESSFUL** —Was the money used effectively
* Feature Variables:
  * **APPLICATION_TYPE** —Alphabet Soup application type
  * **AFFILIATION** —Affiliated sector of industry
  * **CLASSIFICATION** —Government organization classification
  * **USE_CASE** —Use case for funding
  * **ORGANIZATION** —Organization type
  * **STATUS** —Active status
  * **INCOME_AMT** —Income classification
  * **SPECIAL_CONSIDERATIONS** —Special considerations for application
  * **ASK_AMT** —Funding amount requested
* Non-beneficial Variables to Remove:
  * **EIN** and  **NAME** —Identification columns

### Compiling, Training, and Evaluating the Model

* Number of neurons, layers, and type of activation functions selected for neural network model:
  * The first hidden layer used the relu activation function, and consisted of 80 neurons which is higher than the number of input features due to the presumed complexity of the data.
  * The second hidden layer also used the relu activation function, and consisted of 30 neurons which is lower than the first hidden layer to help reduce complexity, encourage generalization, improve computational efficiency, perform dimensionality reduction, and maintain training stability.
  * The output layer used the sigmoid activation function.
* Model evaluation: Were you able to achieve the target model performance?
  * After three optimization attempts, the target model performance of an accuracy score of 75% or above was not achieved.
* Steps taken in attempts to increase model performance
  * First Attempt:
    * Added a third hidden layer, using the relu activation function, with 10 neurons
  * Second Attempt:
    * Removed "STATUS" and "SPECIAL_CONSIDERATIONS" features / columns
  * Third Attempt:
    * Increased epoch count from 100 to 150

## Summary

### Summary of Overall Results

The results of the initial model (without optimization attempts) are as follows:

* Loss: 0.5566800832748413,
* Accuracy: 0.7282798886299133

The best results were achieved in the second optimization attempt which included the following optimization methods:

* Added a third hidden layer, using the relu activation function, with 10 neurons
* Removed "STATUS" and "SPECIAL_CONSIDERATIONS" features / columns

Second attempt model evaluation:

* Loss: 0.5640788078308105,
* Accuracy: 0.7290962338447571

### Reconmmendation

A model is only as good as the inputs fed into it. As such, further initial steps should be taken for data cleanup so that the feature data provided is more relevant to the consequent target variable.
