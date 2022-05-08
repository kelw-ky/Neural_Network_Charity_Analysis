# Neural_Network_Charity_Analysis

## Overview
Using deep-learning neural networks with TensorFlow to analyze and classify the sucess of charitable data. The methods used for this analysis: preprocess the data for the neural network model, compile, train, evaluate the model, and optimize the model. 

## Results 
### Data Processing 
- Column "IS_SUCESSFUL" contains binary data [1 = sucessful, 0 = not successful]; this represents if the charity donation was helpful. This is the target variable. 
- Coloums "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", and "SPECIAL_CONSIDERATIONS" are the features of the model. 
- Columns "EIN" and "NAME" were revmoved from the inout data as they are non-beneficial IDs (neither targets nor features).

### Compiling, Training, and Evaluating the Model
- There are two hidden layers with 75 and 30 neurons respectively. We used the activation fuction ````ReLU```` as the hidden layers and ````Sigmoid```` as the outer layer to speed up the training process. To compile the model, we used "binary_crossentropy" as the loss, "adam" as the optimizer and the metrics is "[accuracy]"

![Training Model](/Resources/Images/nn_model.png)

- The model accuracy is under 75%, hence it does not satisfy the performance to predict the outcome of the charity donations.  
- The first try in the model, we added an extra hidden layer. In the second try, we changed the first ````ReLU```` to ````tanh````. In the third try, we added up to 5 layers. 

![Training Model](/Resources/Images/model_training.png)

## Summary 
As this model only reached 72.9% and failed to reach the target percentage of 75%. This is not a reliable model to predict the charity donations. To improve the model, we would need more data to train. 