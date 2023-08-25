

Overview: 
Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. With knowledge of machine learning and neural networks, we must use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
-----------------------------------------------
Results:
We initiated the data processing by removing any irrelevant information. We excluded the 'EIN' and 'NAME' columns, considering the remaining columns as features for the model. Later, the 'NAME' column was reintroduced in the second optimization phase for the purpose of binning. The dataset was then divided into separate training and testing sets.

The target variable for the model was designated as "IS_SUCCESSFUL." In this binary classification scenario, it takes the value of 1 to represent 'yes' and 0 to represent 'no.' We analyzed the APPLICATION data and specifically utilized the 'CLASSIFICATION' value for the purpose of binning. To consolidate infrequent variables, we applied a cutoff threshold and grouped them together, assigning a new category label of "Other" to each unique value.

For handling categorical variables, we employed the get_dummies() function after confirming the success of the binning process. This allowed us to appropriately encode categorical features into numerical form for the model's input.
-----------------------------------------------
Compiling, Training, and Evaluating the Model:
There were two layers total for each model after applying Neural Networks. The number of hidden nodes were dictated by the number of features.

2207 parameters were created by a two-layer training model. The first attempt was just over 70% accuracy which was under a desired 75% but not too far off.

Unfortunately, in other attempts to add another hidden layer, more neurons and removing neurons my results faired less than the initial 70%

Optimization:
The second attempt with the “NAME” column in the dataset, achieved an accuracy of almost 79%. This is almost 4% over the target 75% with 3,298 parameters.
-----------------------------------------------
Summary:
The deep learning model achieved the desired performance of 78.72% accuracy in predicting the success of Alphabet Soup-funded organizations. Several attempts were made to optimize the model through data preprocessing and neural network structure adjustments, ultimately leading to this improved performance.

A Random Forest Classifier could be used to solve this classification problem. It would have the potential to provide better accuracy and generalization without being as prone to overfitting as deep learning models. Further exploration of this alternative model may lead to even better performance in predicting the success of funded organizations.