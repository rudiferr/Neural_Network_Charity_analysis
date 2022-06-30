# "Neural_Network_Charity_analysis" Week 19 Challenge
## Overview
Using machine learning and neural networks, features in the dataset were used to create a binary classifier that will help to predict if prospectant applicants to be funded by the organization Alphabet Soup will be successful. For this analysis we had a dataset containing various measures on 34,000 organizations that had been previously funded by the said charitable entity.

## Results
### Data Preprocessing
1. What variable(s) are considered the target(s) for your model?    
Variables that were marked as successful in the DataFrame were considered, indicating that it had been successfully funded by AlphabetSoup.  

2. What variable(s) are considered to be the features for your model?    
The IS_SUCCESSFUL column is the feature chosen for this dataset.

3. What variable(s) are neither targets nor features, and should be removed from the input data?    
The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency. 

### Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?    
In the optimized model, I started with a layer that had 100 neurons with a relu activation.  It then dropped to 80 neurons and continued with the relu activation.  From there, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).

5. Were you able to achieve the target model performance?   
The target for the model was 75%, but the best the model could produce was 74.17%.

6. What steps did you take to try and increase model performance?   
Columns were reviewed and dropped (e.g. STATUS, SPECIAL_CONSIDERATIONS, etc.) as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the accuracy yielded lower results. The linear activation in the beginning produced the worst accuracy of all. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.

## Summary
Accuracy results fluctuated between 64.32%, 71.25%, and finally 74.17%. Accuracy definitely improved from initial trials, but only improved marginally towards the end. Improvements can include utilizing a random forest classifier as it is less influenced by outliers.