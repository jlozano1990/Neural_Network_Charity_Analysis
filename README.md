# Neural_Network_Charity_Analysis

## Overview of the Analysis
In this analysis we are tasked to create a deep learning neural network model. We used information from a CSV file from AlphabetSoup which contained 34,000 organizations that received funding. We are using the dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results
- Data Preprocessing
    - The variable considered the target for our model is the IS_SUCCESSFUL column in our dataset because we are trying to create a neural network model that can predict that specific attribute.
    - The variables considered to be the features for our model are all the other columns of our dataset. That includes APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATION, and ASK_AMT.
    - The variables that are neither targets nor features are the EIN and NAME columns. Those should be removed from our data.

- Compiling, Training, and Evaluating the Model
    - I created 4 neural network models to attempt to reach a 75% accuracy. In the first model, I ran everything the same as our original neural network model, except I removed the special considerations columns to see if it would affect the result. There was no significant difference. In the second model, I used all the original data but I changed the activation functions for each layer. For the hidden layers, I applied the sigmoid function and for the activation layer, I applied the relu function. Changing the activation functions in this case made my neural network a lot worse. The loss for this model increased to 8.22 and the accuracy dropped to 46%. For the third model I created, I added more neurons to the 2 hidden layers we had(Hidden Layer 1 = 100 and Hidden Layer 2 = 50) and I added a 3rd hidden layer with 25 neurons. I used the same activation functions as our original neural network, but added 150 epochs so the model would run 250 epochs total. With this model, there were no significant increases. Our accuracy was about 72.6%. With the 4th and final model I created, I changed the number of neurons and used 2 hidden layers. I ran this model through 200 epochs but changed all the activations for each layer to Sigmoid. With this model, I was still not able to achieve over 75% accuracy. The result for this modelwas 72.7%.
    - I was not able to achieve the target model performance.
    - I took a couple of different things to increase my model's accuracy. I increased the number of neurons in some models to see if that would help classify the data better. Also, I checked if I added a third hidden layer if that was able to increase accuracy. Also, I changed the training features and changed the activation function from relu to sigmoid to see if that helped with accuracy.

## Summary
Using the deep learning model, the highest accuracy that I could achieve was 72% even though I changed various things, such as activation functions, number of neurons, and layers. Another option to predict the results of this dataset could be using an SVM model because it is not as prone to overfitting and works well with tabular data.
