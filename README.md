# deep-learning-challenge

## Neural Network Model Report

### Overview
The purpose of this analysis is to determine which applicants have the best chance of success as ventures if funded by Alphabet Soup. The dataset contains more than 34,000 organizations that received funding by Alphabet soup. This data analysis uses deep learning / neural networks for the machine learning model and is trying to find the best optimized model for this dataset in determining the objective. 

### Reults
#### Data Preprocessing
What variable(s) are the target(s) for your model?
- The target of the model is the IS_SUCCESSFUL variable.
What variable(s) are the features for your model?
- The features of the model are "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION","STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT."
What variable(s) should be removed from the input data because they are neither targets nor features?
- "EIN" and "NAME" columns were removed because they were neither targets or features.
#### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- For my best model, AlphabetSoupCharity_Optimization3.ipynb, I have the following:
- Number of neurons and layers:
- First hidden layer: hidden_nodes_layer1 = 60 neurons with the tanh activation function.
- Second hidden layer: hidden_nodes_layer2 = 15 neurons with the tanh activation function.
- Third hidden layer: hidden_nodes_layer3 = 5 neurons with the relu activation function.
- I chose these layers and activation functions to create a neural network model that can handle the complexity of the classification problem in the dataset. By using multiple hidden layers with varying numbers of neurons, the model can learn intricate patterns and representations from the data. The `tanh` activation function in the first two hidden layers allows the model to capture non-linear relationships, while the `relu` activation function in the third hidden layer helps in efficiently handling sparse and negative data. This configuration aims to strike a balance between model complexity and performance, but further experimentation and tuning might be required to find the optimal configuration for the given task.
Were you able to achieve the target model performance?
- No. the target model performance was 75% accuracy.
What steps did you take in your attempts to increase model performance?
- I tried to increase teh accuracy by changing the amount of layers, activation functions, and adjusting the number of neurons. I looked at the training loss and training accuracy to determine what epoch numbers I should have.




### Summary
- The deep learning model achieved a training loss of approximately 56.05% and a testing accuracy of about 72.48%. To potentially improve performance, I recommend trying a Random Forest classifier as an alternative model. Random Forest can handle non-linearity, is less prone to overfitting, and provides feature importance, making it a suitable option for this classification problem.
