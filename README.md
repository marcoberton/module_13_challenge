# Module 13 Challenge

## Overview & Objectives

The purpose of the models is to use tensorflow and keras to analyze data provided to this venture capital firm in order to assess whether they can be used to accurately predict if future applicants will be successful in the future.  To preprocess the data we will be using various Pandas functions such as Path() and concat(), as well as scikit-learn’s StandardScaler() for the neural network models.  OneHotEncoder will also be used to create an encoded dataframe for these models.  Once preprocessed we will use the train_test_split function to create a testing and training dataset, scaling the data with StandardScaler afterwards. Each neural network model will be a Sequential model as well.  Once trained, tested and run each of the three models were saved to an h5 file.

## Models
All models listed have equal input features to the dataset (or 116 input features)

Original neural network model or nn:
    * Started with 2 hidden layers with the standard relu activation, with 58 nodes and 29 nodes respectively
    * Had one output node using the Sigmoid activation
    * Compiled using Binary_Crossentropy where the metrics were Accuracy 
    * At 50 epochs this model produced a Loss of 55% and Accuracy of 73%

Second neural network model or nn_A1:
    * Started with 3 hidden layers with the standard relu activation, with 80, 40, and 20 nodes respectively
    * Had one output node using the Sigmoid activation
    * Compiled using Binary_Crossentropy but changed the Loss to mse and optimizer to sgd 
    * At 100 epochs this model produced a Loss of 18% and Accuracy of 57%
    
Third neural network model or nn_A2:
    * Started with 3 hidden layers with the standard relu activation, with 58, 29, and 15 nodes respectively
    * Had one output node using the Sigmoid activation
    * Compiler was optimized with sgd and used the mse loss, as well as the CategoricalAccuracy metric 
    * At 50 epochs this model produced a Loss of 18% and Accuracy of 100%
    
## Conclusions
Since we were trying for a binary classification model the best activation for hidden layers seemed to be relu, and the best output activation was also Sigmoid.  More activations were attempted but either broke or threw off the Loss and Accuracy so much they weren't worth putting forth.  The first model had the most basic of parameters but produced far too high of a loss rate.  The third model seems very promising with a great loss rate of 18%, however the 100% Accuracy should be examined further making it tough to reccomend.  In conclusion I would go with the second model nn_A1 since it has the best Loss to Accuracy rate without seeming broken, though more comprehensive tests could reveal a better model.